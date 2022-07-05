==================
Immutable invoices
==================

All supplier invoices entering the system are stored as encrypted binary files in MongoDb, along with metadata about the invoice that is needed for further processing.

We protect our database against tampering by hashing database documents with a secret and storing them on a Hedera topic.
Whenever we request data from the database, we can verify whether the document has been tampered with by verifying the hash.

.. warning::

    We have yet to consider how to handle the case of tampering gracefully, in case it occurs.
    Since invoices can never be updated, rolling back to a previous version would be a viable option.
