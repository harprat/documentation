====
Tips
====

Tipping is customary in multiple countries. Point of Sale allows tipping in
:doc:`shops<../overview/getting_started>`, :doc:`bars<../restaurant>` or
:doc:`restaurants<../restaurant>`

.. _configuration:

Configuration
=============

To allow tipping in your POS, activate the :guilabel:`Tips` feature in :menuselection:`Point of Sale
--> Configuration --> Settings`. At the top of the page, select the POS in which you wish to allow
**tipping**, scroll down to the :guilabel:`Payment` section and check :guilabel:`Tips`. Once
enabled, add a :guilabel:`Tip Product` in the corresponding field, and save. The referred product
will be used as a reference on customers' receipts.

.. image:: tips/tips-setup.png
   :align: center
   :alt: enable tips in a POS

.. note::
   - If you use an :doc:`Adyen <../payment/adyen>` payment terminal and wish to enable **tips**
     using the terminal, check :guilabel:`Add tip through payment terminal (Adyen)`.
   - If your POS is a bar or a restaurant, you can enable :guilabel:`Add tip after payment (North
     America specific)`. Doing so generates a bill to complete manually with the tip value the
     customer chooses to give after the payment. Print the bill, click the desired percentage
     (:guilabel:`15%`, :guilabel:`20%` or :guilabel:`25%`), :guilabel:`No Tip` if you do not want to
     tip, or enter the amount. Then, click :guilabel:`Settle` to move to the next order.

Tip products
------------

You can use any product as **tip products**. However, we suggest you create one specifically for
this purpose.

To do so, create a product by going to :menuselection:`Point of Sale --> Products --> Products -->
Create`. Add a :guilabel:`Name` of your choice and leave the **product type** as
:guilabel:`Consumable` to avoid unnecessary inventory movements.

.. future: remove 1st sentence and add
   :ref:`create a product <product_creation>`

You can also create a product on-the-spot. To do so, enter a product's name in the
:ref:`Tip Product <configuration>` field and click :guilabel:`Create`. The product is automatically
configured to be used as a tip, but you can click :guilabel:`Create and edit...` to open the product
creation form and set it up manually.

.. note::
   - If you use an :doc:`Adyen <../payment/adyen>` payment terminal and wish to enable **tips**
     using the terminal, check :guilabel:`Add tip through payment terminal (Adyen)`.
   - If you create a tip product on-the-spot, the **Available in POS** feature is not activated.
     Thus, the product will not appear in a POS session. If you want to select the product in POS,
     tick the :guilabel:`Available in POS` checkbox in the :guilabel:`Sales` tab and click
     :guilabel:`Save & Close`.
   - You can only select one tip product per POS, but you can choose a different tip product for
     each POS.

Add tips
========

To add a tip to your order, you can add the **tip product** to the cart or click :guilabel:`Payment`
to access the payment screen. Then, click :guilabel:`♥ Tip`, enter the amount and click
:guilabel:`Confirm` to validate, and process to the payment.

When adding the tip product to the cart, it is automatically set as a tip and its default value
equals its **Sales Price**. You can still modify that amount during the order by clicking
:guilabel:`Price` and entering the amount on the keypad, or, at the payment screen, by clicking
:guilabel:`♥ Tip` and entering the desired amount.

.. image:: tips/add-tip.png
   :align: center
   :alt: tip popup window
