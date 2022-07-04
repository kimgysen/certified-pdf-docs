===================
Source verification
===================

There are different phishing techniques that allow insincere attackers to trick clients into paying wrongful invoices; through fake emails, redirects to malicious website url’s and misleading domains.
If not for the reason of security, the practise is confusing and all-round annoying for the receiving client.
Spam filters allow black lists against insincere emails, but managing blacklists is not a clean solution to the problem.

For each receiving client, our api creates a default client smart contract upon user registration, which maintains a whitelist filter of supplier IBAN numbers.
The set is empty per default, which implies that clients are themselves responsible for composing their own whitelist.
They should be the only ones to decide who is allowed to send them an invoice, without requiring to declare who is not (blacklist).
The same contract whitelist is then used by our server to verify whether an invoice pushed by a supplier is allowed to be transferred to, or requested by the client.
