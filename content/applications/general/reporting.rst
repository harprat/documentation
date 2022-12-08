=========
Reporting
=========

You can find under the :guilabel:`Reporting` menu of most apps several reports that let you analyze
and visualize your records' data.

.. _reporting/views:

Selecting a view
================

Depending on the report, Odoo can display the data in a variety of ways. Sometimes, a unique view
fully tailored to the report is available, while for others, several views are available. Two
generic views are dedicated to reporting however: the graph and pivot views.

.. _reporting/views/graph:

Graph view
----------

The :ref:`graph view <reporting/graph>` is used to visualize your records' data, helping you
identify patterns and trends. The view is often found under the :guilabel:`Reporting` menu of apps
but can be found in other places. Click the **graph view button** located at the top right to access
it.

.. image:: reporting/graph-button.png
   :align: center
   :alt: Selecting the graph view

.. _reporting/views/pivot:

Pivot view
----------

The :ref:`pivot view <reporting/pivot>` is used to aggregate your records' data and break it down
for analysis. The view is often found under the :guilabel:`Reporting` menu of apps but can be found
in other places. Click the **pivot view button** located at the top right to access it.

.. image:: reporting/pivot-button.png
   :align: center
   :alt: Selecting the pivot view

.. _reporting/choosing-measures:

Choosing measures
=================

After selecting a view, you should ensure only the relevant records are :doc:`filtered <search>`.
Next, you should choose what is measured. By default, a measure is always selected. If you wish to
edit it, click :guilabel:`Measures` and select one or, only for pivots, multiple measures.

.. example::
   You could add the :guilabel:`Margin` and :guilabel:`Count` measures to the Sales Analysis report,
   which only displays the :guilabel:`Untaxed Amount` by default.

   .. image:: reporting/measures.png
      :align: center
      :alt: Selecting different measures on the Sales Analysis report

.. note::
   When you select a measure, Odoo aggregates the values recorded on that field for the filtered
   records. Only numerical fields (:ref:`integer <studio/fields/simple-fields/integer>`,
   :ref:`decimal <studio/fields/simple-fields/decimal>`, :ref:`monetary
   <studio/fields/simple-fields/monetary>`) can be measured. In addition, the :guilabel:`Count`
   option is used to count the total number of filtered records.

After choosing what you want to measure, you can define how the data should be :ref:`grouped
<search/group>` depending on the dimension you want to analyze. A typical default group is *Date >
Month*, which is used to analyze the evolution of a measure over the months.

.. example::
   You could divide the measures by the :guilabel:`Product Category` group at the level of rows on
   the previous Sales Analysis report example.

   .. image:: reporting/single-group.png
      :align: center
      :alt: Adding a group on the Sales Analysis report

.. tip::
   When you filter a single time period, the option to compare it against another one appears.

   .. image:: reporting/comparison.png
      :align: center
      :alt: Using the comparison option

.. _reporting/pivot:

Using the pivot view
====================

Grouping data is quintessential to the pivot view. It enables to drill down the data to gain deeper
insights. While you can you can use the :guilabel:`Group By` option to quickly add a group at the
level of rows as shown in the example above, you can also click the plus button (:guilabel:`➕`)
next to the :guilabel:`Total` header at the level of rows *and* columns, and then select one of the
**preconfigured groups**. To remove one, click the minus button (:guilabel:`➖`).

Once you have added a group, you can add new ones one on the opposite axis or on one of the newly
created subgroups.

.. example::
   You could further divide the measures on the previous Sales Analysis report example by the
   :guilabel:`Salesperson` group at the level of columns and by the :guilabel:`Order Date > Month`
   group on the :guilabel:`All / Saleable / Office Furniture` product category.

   .. image:: reporting/multiple-groups.png
      :align: center
      :alt: Adding multiple groups on the Sales Analysis report

.. tip::
   - Switch the rows and columns' groups by clicking the flip axis button (:guilabel:`⇄`).
   - Click on a measure's label to sort the values by ascending (⏶) or descending (⏷) order.
   - Download a `.xlsx` version of the pivot by clicking the download button (:guilabel:`⭳`).

.. _reporting/graph:

Using the graph view
====================

Three graphs are available, the bar, line, and pie charts.

**Bar charts** are used to show the distribution or a comparison of several categories. They are
especially useful as they can deal with larger data sets.

.. image:: reporting/bar.png
   :align: center
   :alt: Viewing the Sales Analysis report as a bar chart

**Line charts** are useful to show changing time series and trends over time.

.. image:: reporting/line.png
   :align: center
   :alt: Viewing the Sales Analysis report as a line chart

**Pie charts** can be used to show the distribution or a comparison of a small number of categories
when they form a meaningful whole.

.. image:: reporting/line.png
   :align: center
   :alt: Viewing the Sales Analysis report as a pie chart

.. tip::
   For bar and line charts, you can use the stacked option when you have at least two groups, which
   then appear on top of each other instead of next to each other.

   .. tabs::

      .. tab:: Stacked bar chart

         .. image:: reporting/stacked.png
            :align: center
            :alt: Stacked bar chart example

      .. tab:: Regular bar chart

         .. image:: reporting/non-stacked.png
            :align: center
            :alt: Non-stacked bar chart example

   For line charts, you can use the cumulative option to sum values, which is especially useful to
   show the change in growth over a time period.

   .. tabs::

      .. tab:: Cumulative line chart

         .. image:: reporting/cumulative.png
            :align: center
            :alt: Cumulative line chart example

      .. tab:: Regular line chart

         .. image:: reporting/non-cumulative.png
            :align: center
            :alt: Regular line chart example
