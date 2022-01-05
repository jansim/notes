# ACID Transactions: Atomicity, Consistency, Isolation, Durability

## Atomicity
Either the Transaction happens completely or it doesn't, there's nothing in between

## Consistency
The database remains constistent before and after the transaction. Transactions that would violate consistency will fail.

## Isolation
Transaction occur in isolation, they are not aware of each other and changes are only visible once committed.

## Durability
Once commited, the transaction's changes will remain even if the system shuts down => they are written to disk.