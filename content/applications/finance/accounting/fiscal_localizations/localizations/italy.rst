=====
Italy
=====

Configuration
=============
The first necessary step to carry out accounting transactions in Italy is the
:guilabel:`Italy - Accounting`. Once this module is installed you can start managing your accounting
in Odoo. For all B2B transactions, Italy requires electronic invoicing, the use of specific formats and the
transmission of invoices on **SDI** platform.

Odoo modules allow to:

- Generate electronic invoices in **FatturaPA's** format.
- Send and receive electronic invoicing through SDIcoop.
- Use the **Codice Destinatario** `K95IV18`.

.. warning::
   Once this module is installed, it's no longer possible to send invoices via :ref:`PEC mails
   <italy/pec>`.

Company information
-------------------

The company information is the first necessary configuration to ensure the proper set up of your
**Accounting** database. To do so, go to :menuselection:`Configuration --> Settings -->
General Settings --> Update info`. In this menu, make sure to have at least the following:

- the company address
- :guilabel:`GSTIN` code
- :guilabel:`Codice Fiscale`
- :guilabel:`Tax System`
- :guilabel:`PEC address email`

PEC
---
The PEC email is a specific type of certified email providing a legal equivalent to the traditional
registered mail. The PEC email of the main company must be the same as the one registered by the
Agenzia delle Entrate authorities.

SDICoop
-------

To receive invoices and notifications from third parties, you need to inform the FatturaPA service
that Odoo is the allowed party to process files for you. To do so, you must set up Odoo's **Codice
Destinatario** on the FatturaPA portal.

#. Go to https://ivaservizi.agenziaentrate.gov.it/portale/ and authenticate.
#. Go to section :menuselection:`Fatture e Corrispettivi`.
#. Set the user as Legal Party for the VAT number you wish to configure the electronic address.
#. In :menuselection:`Servizi Disponibili --> Fatturazione Elettronica --> Registrazione
   dell’indirizzo telematico dove ricevere tutte le fatture elettroniche`, insert Odoo's Codice
   Destinatario (`K95IV18`), then confirm.

Give Odoo permission to process files
-------------------------------------

Since the files are transmitted through Odoo's server before being sent to SDICoop or received by
your database, you need to authorize Odoo to process your files from your database.

To do so, go to :menuselection:`Accounting --> Configuration --> Settings --> Electronic
Document Invoicing`. In the :guilabel:`Electronic Document Invoicing`, you can see three different
modes:
- Demo
- Test (experimental)
- Official (production)

Choosing the right mode
-----------------------
- :guilabel:`Demo` mode in Odoo is a simulation environment where all invoices created are **not**
  automatically sent to the government. In such mode, the invoices need to be manually downloaded
  as xml files and you then have to upload them on the Agenzia dell'Entrate website.
- :guilabel:`Test` mode sends invoices to a non-production service.
- :guilabel:`Official` is a production mode that sends your invoices directly to the Agenzia
  dell'Entrate.

.. warning::
   Once in :guilabel:`Official` mode it is not possible to get back to the :guilabel:`Test` and
   :guilabel:`Demo`.

After having selected the right mode, you need to accept the terms and conditions right below the
mode selection. Once you have :guilabel:`Saved` the mode you want, you can start recording your
Accounting transactions in Odoo.

Issue invoices
==============

The **FatturaPA** feature is automatically active, you can check it in :menuselection:`Configuration
--> Journals --> Customer Invoices -->  Advanced Settings`
You can create a new invoice by going to :menuselection:`Accounting dashboard --> New invoice`, once
confirmed the e-invoice will be generated and sent.


.. warning::
   The e-invoice is only sent to the government if you are in :guilabel:`Official` mode.

You can check the current status of your customer invoice under the :guilabel:`Electronic invoicing`
field. The xml file is accessible in the chatter of the invoice.

.. image:: italy/processing.png
   :align: center
   :alt: Electronic invoicing status (waiting for confirmation)

Vendor bills
============



