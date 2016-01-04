Calibration Plot
================

.. figure:: icons/calibration-plot.png

Shows the match between classifiers’ probability predictions and actual
class probabilities.

Signals
-------

**Inputs**:

-  **Evaluation Results**

Results of testing classification algorithms.

**Outputs**:

-  None

Description
-----------

`Calibration
Plot <https://en.wikipedia.org/wiki/Calibration_curve>`__ plots class
probabilities against those predicted by the classifier(s).

.. figure:: images/CalibrationPlot-stamped.png

1. Select the desired target class from the drop down menu.

2. Choose which classifiers to plot.

The diagonal represents the optimal behaviour; the closer the
classifier's curve gets, the more accurate its prediction probabilities
are. Thus we would use this widget to see whether a classifier is overly
optimistic (gives predominantly positive results) or pesimitistic (gives
predominantly negative results).

3. If *Show rug* is enabled, ticks are displayed at the bottom and the
   top of the graph, which represent negative and positive examples
   (respectively). Their position corresponds to classifier’s
   probability prediction and the color shows the classifier. On the
   bottom of the graph, the points to the left are those which are
   (correctly) assigned a low probability of the target class, and those
   to the right are incorrectly assigned high probabilities. On the top
   of the graph, the instances to the right are correctly assigned high
   probabilities and vice versa.

Example
-------

At the moment, the only widget which gives the right type of signal
needed by the **Calibration Plot** is :doc:`Test&Score<../evaluation/testlearners>`. Calibration
Plot will hence always follow Test&Score and, since it has no
outputs, no other widgets follow it.

Here is a typical example, where we compare three classifiers (namely
:doc:`Naive Bayes<../classify/naivebayes>`, :doc:`Classification Tree<../classify/classificationtree>` and :doc:`Majority<../classify/majority>`) and input
them into :doc:`Test&Score<../evaluation/testlearners>`. Test&Score then displays evaluation
results for each classifier. Then we draw **Calibration Plot** and :doc:`ROC
Analysis<../evaluation/rocanalysis>` widgets from Test&Score to further analyze the performance
of classifiers. Calibration Plot enables you to see prediction accuracy
of class probabilities in a plot.

.. figure:: images/CalibrationPlot-example.png