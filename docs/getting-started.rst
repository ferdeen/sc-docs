###############################
Getting Started
###############################

.. note::
    This section assumes a Windows development environment. Stratis Smart Contracts can be developed on other platforms - documentation is coming soon.

What You'll Need
----------------

* `Visual Studio <https://www.visualstudio.com/downloads/>`_
    The standard IDE for C# development. The Community Edition is available for free.
* `Stratis Smart Contract Visual Studio Solution Template <https://www.visualstudio.com/downloads/>`_
    A template .NET Core solution with a sample contract project and sample unit testing project.
* `Stratis' Command Line Smart Contract Tool <https://www.visualstudio.com/downloads/>`_
    To validate your contracts, and more easily compile and deploy them.

Your First Contract
-------------------

Once the template has been installed, in Visual Studio you can navigate to File > New > Project… and create a new ‘Stratis SmartContract Project’ under ‘Visual C#’.

This will generate a completely new solution with a sample contract - an auction, and a project with some sample unit tests.

You'll notice the class Auction in Auction.cs is just a C# class. If you're not a C# developer you may want to firstly delve into the `basics of C# development <https://docs.microsoft.com/en-us/dotnet/csharp/>`_. This tutorial will focus on the smart contact-specific parts of the code.

::

    pragma solidity ^0.4.0;

    contract SimpleStorage {
        uint storedData;

        function set(uint x) public {
            storedData = x;
        }

        function get() public constant returns (uint) {
            return storedData;
        }
    }
