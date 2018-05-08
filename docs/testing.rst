###############################
Testing
###############################

With Stratis Smart Contracts, your tests can be developed and debugged using C# inside Visual Studio. The tests as described here verify that your smart contract logic executes as intended, before you deploy it to a live network.

.. note::
  Testing of Stratis Smart Contracts is still primitive. Future versions of smart contracts will enable testing with the resource tracking code injected, and on top of a local test blockchain.

The Basics
----------

This section will again reference the `Visual Studio Template <https://www.visualstudio.com/downloads/>`_. If you're not using the template, the testing code can be found `here <https://www.visualstudio.com/downloads/>_`.

The tests inside the template use the ``Microsoft.VisualStudio.TestTools.UnitTesting`` library, so may be familiar to C# developers.

- ``[TestClass]`` defines a class in which tests are defined.
- ``[TestInitialize]`` is used to mark a method to be run before tests execute, most commonly to set up some testing context.
- ``[TestMethod]`` marks the actual tests to be run.
- The static class ``Assert`` provides access to a range of methods to validate the results of whatever execution you perform inside your tests.

To run all of the tests together, in Visual Studio right click on ``[TestClass]`` and select `Run Tests`. To run tests individually, right click on the individual method and select `Run Tests`. Once clicked, the solution will take a couple of seconds to build and then the `Test Explorer` will open. You should see your tests listed in the `Test Explorer`, next to a green tick indicating they've passed.

DEBUG.

Describe method of injecting smart contract state.

Awesome, you're ready to put your contract on a live Stratis network!
