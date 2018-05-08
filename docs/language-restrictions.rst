###############################
Language Restrictions
###############################

Blockchain-based smart contracts need to be restricted at some level to ensure they execute deterministically. This is crucial so that regardless of nodes' underlying architecture, operating system, location, time, or any other factors, they will always execute the contract the same way and thus the network of nodes can reach consensus.

As Stratis smart contracts execute in native .NET bytecode on the CLR, this restriction needs to happen at the code level. Only certain code is permitted to execute inside smart contracts and nodes validate smart contracts' code before they are deployed.

Furthermore, there are some patterns that need to be followed in order for nodes to recognise your contract as valid.

Format
------

To be written.
