GenLayer Intelligent Contract Example
Finalized Error Handling with Optimistic Democracy
This repository contains an example of a Python-based Intelligent Contract executed on GenLayer.
The purpose of this project is to demonstrate how GenLayer handles non‑deterministic execution 
and execution errors using the Optimistic Democracy consensus mechanism.

Overview
The contract implements a simple betting workflow that attempts to resolve a bet using external data.
Because external data is involved, execution may result in an error.
This repository shows that such an outcome is still:

* independently recomputed by validators
* agreed upon through consensus
* finalized on-chain


Key Concepts Demonstrated

* Python Intelligent Contracts
* Non‑deterministic execution
* Write method execution under Full Consensus
* Execution errors as valid consensus outcomes
* Optimistic Democracy finalization
* Safe contract state preservation


Contract Behavior

1. The contract is deployed to the network.
2. Initial state is readable through view methods.
3. A write method (resolve_bet) is executed.
4. The execution attempts to use external data.
5. The execution results in an ERROR.
6. Validators recompute the execution independently.
7. Majority agreement is reached.
8. The transaction is finalized.


Final Outcome
The write transaction completes with the following properties:

* The transaction is FINALIZED
* The execution result is ERROR
* The outcome is approved by validator consensus
* The contract state remains valid and unchanged

In GenLayer, an execution error does not represent a failure.
It represents a consensus‑approved and finalized result.

Why This Matters
Traditional smart contracts require strict determinism.
GenLayer introduces a model where contracts can:

* interact with real‑world data
* tolerate execution uncertainty
* preserve correctness through validator agreement

This enables intelligent, data‑aware, and AI‑driven contract logic.

Notes

* Execution errors in this example are expected.
* The project is intended for educational and demonstrational purposes.
* Finalized transaction data is the source of truth.


Conclusion
This repository demonstrates that GenLayer safely finalizes contract execution even when execution fails.
By treating errors as valid outcomes and finalizing them through Optimistic Democracy, 
GenLayer enables a new class of intelligent contracts without sacrificing trust.
