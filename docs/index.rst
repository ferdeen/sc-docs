.. Stratis Smart Contracts documentation master file, created by
   sphinx-quickstart on Thu Mar  8 23:40:26 2018.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Stratis Smart Contracts
===================================================

.. image:: strat.svg
    :width: 250px
    :alt: Solidity logo
    :align: center

    Stratis Smart Contracts are immutable blocks of code that can be deployed on a Stratis blockchain to enable the development of decentralised applications. Written in C# with some constraints applied, Stratis Smart Contracts execute in real .NET and allow on-chain processing, data storage and fund transfers.
    Writing a smart contract in C# with Stratis is just like building any other .NET application, with the ability to develop, debug and test in Visual Studio. If you’re coming from an object-oriented background, you can think of a smart contract as a kind of immutable on-chain singleton.
    
    You can use smart contracts to create tokens, wagers, auctions and other complex financial instruments.

.. warning::
    The Stratis Smart Contract platform is currently in an open alpha stage. Things may break, and aspects of the development process are subject to change. Please don’t use the alpha version of Stratis Smart Contracts for production applications.

Contents
========

.. toctree::
   :maxdepth: 2

   getting-started.rst
   determinism.rst
   opcodes-and-serialization.rst
