Welcome to Certified PDF documentation!
===================================

 | V1 of our **Certified PDF Api** provides the certified distribution of invoices from supplier to client.
 | It installs an intermediary verification layer that fulfils a double purpose:


* **Verified source**:
 | Clients can declare a whitelist of suppliers through a smart contract, from whom they receive periodical invoices as a measure of protection against phishing.
 | The smart contract filters invoices based on their supplier IBAN, and therefore decides whether or not an invoice transfer is allowed.

* **Immutable invoices**:
 | All invoices are stored as encrypted PDF files in MongoDb, after which we generate and store hashes for each document on a Hedera topic to prevent tampering.
 | Once the invoice is stored, it is immutable and cannot be changed without being noticed.

 | This documentation site describes our process flows and technical api architecture.
 | We rely heavily on multiple rounds of security analysis to determine and eliminate potential security vulnerabilities.

.. note::

   This project is under active development.

Contents
--------

.. toctree::
    :caption: Intro
    :maxdepth: 2

    intro/verified_source
    intro/immutable_invoices

.. toctree::
    :caption: Registration
    :maxdepth: 1

    registration/client
    registration/supplier

.. toctree::
   :caption: Example rst

   usage
   api
