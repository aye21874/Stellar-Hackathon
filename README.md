# Stellar-Hackathon

Stellar is an open-source network that is intended to enhance the existing financial system by unlocking the world's economic potential by making money more fluid, markets more open and people more empowered. Stellar is a decentralized system that's great for trading any kind of money in a transparent and efficient way. Stellar doesn't privilege any particular currency. It's specifically designed to make traditional forms of money--the money people have been spending and saving for centuries--more useful and accessible.

At the lowest level, Stellar is a system for tracking ownership. It does so through the use of a ledger, which stores two important things about every account holder: what they own (balances, like "100 pesos tokens" or "5000 lumens") and what they want to do with what they own (operations, like "sell 10 dollar tokens for 50 lumens" or "send 100 peso tokens to a specific account"). Every five seconds, all the balances and all the operations are broadcast to the entire network and resolved in what is called a ledger block.

Ledger blocks consist of transactions, which are defined as bundles of operations that can be applied to an account. Transactions include anywhere from 1 to 100 operations per transaction. For example, an account holder can pay multiple entities in a single transaction by submitting payment operations for each entity in that one transaction.

To submit a transaction on the Stellar Blockchain Network, a small fee is required to prevent spam and maintain efficiency. The fee for a given transaction is equal to the number of operations the transaction contains multiplied by the base fee of the ledger. The current base fee is 100 stroops (0.00001 XLM), which is the native currency of the Stellar Network.

Transaction fee = # of operations * base fee

Note: in cases of Fee Bump transactions, the fee calculation changes to

Fee Bump Transaction Fee = ( # of operations + 1 ) * base fee

When network activity exceeds capacity (1,000 operations per ledger block), the network enters surge pricing, which uses market dynamics to decide which transactions should be successfully submitted to the ledger. Essentially, submissions that offer a higher fee per operation make it onto the ledger first. Once the network enters surge pricing, it can take a while for pricing to stabilize and return to base fee pricing for transactions.

Your goal is to build a model that predicts when the network will enter surge pricing. Specifically, your model should be able to estimate the fee charged a given transaction based on past ledger dynamics. This way users can get an accurate estimate on their max fee allowance with reasonable guarantee that the transaction is successfully submitted.
