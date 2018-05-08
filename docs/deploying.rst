###############################
Deploying and Calling Contracts
###############################

Running a Node
--------------

To start interacting on a test smart contract network you'll need to clone the `sc-alpha` branch of the `Full Node <https://github.com/stratisproject/StratisBitcoinFullNode>`_ locally.

The smart contract daemon is located in the ``src/Stratis.StratisSmartContractsD`` folder. With the command line open in this directory, you can run the following command to start a node and join our test network:

::

  dotnet run -- connect=20.190.57.145

.. warning::
  The smart contract test network will break. We provide no guarantee of its uptime and may reset the network as deemed necessary. For the most up-to-date information, join us on Discord: :ref:`support_and_community`.


Contract Deployment
-------------------

A contract must be deployed before it can be used. A Stratis smart contract deployment involves several steps:

* Compilation of the contract
* Validation of the contract
* Creating a transaction with the contract’s code
* Broadcasting the transaction to the network

The command line tool ``sct`` combines these steps and simplifies the process.

Deployment of a C# source file
--------------------

Command line tool
'''''''''''
The command line tool is available in the smart contracts source code repository. To run the tool from the command line, you first need to change into its directory:

::

  cd src/Stratis.SmartContracts.Tools.Sct

Deployment
''''
A smart contract can be deployed from the command line tool using a sub-command, deploy. This will compile the contract, validate its bytecode, create a transaction and broadcast it to a node.

A contract can only be deployed to a node running locally, using a local wallet, account, and password. These must be provided to the deployment tool, as well as the name of the file to deploy.

::

  dotnet run -- deploy Contract.cs http://localhost:38220 -wallet mywallet -account "account 0" -password password -fee 1000 -gasprice 1 -gaslimit 30000

Deployment with constructor params
'''''''
If the contract you are deploying accepts constructor params, you can additionally pass these in to the command line tool via the ``params`` argument.

Success
'''''''
If the contract was deployed successfully, the tool will return the address of the contract.

Calling Contracts
-----------------
