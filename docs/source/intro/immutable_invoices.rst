==================
Immutable invoices
==================

All supplier invoices entering the system are stored as encrypted binary files in MongoDb, along with metadata about the invoice that is needed for further processing.

We protect our database against tampering by hashing the database's content according to a Merkle tree algorithm (root hash).
These hashes are stored on a Hedera network topic when generating the proof, making them persistent and immutable.
We must generate a new hash for every new document that we store in our database, which will result in a newly added path to the Merkle tree.

Hence, whenever we request data from the database, we can verify whether the document has been tampered with by verifying the hash.

.. warning::

    We have yet to consider how to handle the case of tampering gracefully, in case it occurs>.
