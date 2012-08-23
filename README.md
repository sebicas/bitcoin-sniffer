Bitcoin P2P Network Sniffer v0.0.1
===============================================

BTC Sniffer is a Python script based on an easy version of jgarzik / pynode ( https://github.com/jgarzik/pynode ) that connects to any node on the Bitcoin Network and triggers the folloing events:

* **new_block_event(block)**: Triggers when a **Block** is found
* **new_tx_event(tx)**: Triggers when a **Transactions** is found

The purpose of BTC Sniffer is the add an easy way to listen to Bitcoin Network events and facilitate extensions without having to alter bitcoind's code itself, making it easy to upgrade you bitcoind node without having to rewrite your extensions.

The best possible scenario is having BTC Sniffer listening to a local bitcoind node, since we can assume you can trust your own node. But tecnicly, it can connect to any node on the network ( http://blockchain.info/connected-nodes )

**IMPORTANT**: BTC Sniffer doesn't do any validation, it just trust the node it connects for that, so if you use it on production, make sure you connect to a node you trust.

See how it works
----------------

Here is an example of the script output:

```
MacBook-Pro:bitcoin-sniffer sebicas$ ./sniffer.py

 Bitcoin Network Sniffer v0.0.1
 -------------------------------------------------------------------------
 Connecting to Bitcoin Node IP # 173.242.112.53:8333
 Connected & Sniffing :)

 - Valid TX: 68ca213684e40a673dba7bbcb1d9bebb2c696eb8da92f8e8d853cab772e92f52
 - Valid TX: 8192c04854d635755184f0f5a6444becba051750ef1ab8bf39967785f377d89e
 - Valid TX: 433b0f7f8b343d0ce25c0ad1e22b42fc57526cfa9ecc86511440d2d5f63961ec
 - Valid TX: 3839d9a481606105ae9f0513e66305cdb6e18149f8c7ae7aea0550d77b443f56
 - Valid TX: 12afb272778079c36f0e35ad9d147b37c9e34f42b12133efca6f57d68a68e548

 - Valid Block: 0000000000000408f197ce13e2271edc889b6ef3109036ce6ff2e30f2e9023df

 - Valid TX: 4649725078f30f4b18099a6ede4c991c16c16887e4ff860b33cb7fa8d6c01c3a
 - Valid TX: 712419473ed2a429de1757030d8551f6ee5d360fdfc9648f5647fbd6f166ed2b
 - Valid TX: 17546dea9122dc13c81fc177c2fba0eda30674fbc29619f24b556095a52efdc3
 - Valid TX: da2621f6ef147e78dfe210e3d3718fb620dc9c8bfbbebd3b1e7e49645e20c53f
 - Valid TX: ddc70dc5119150d2731f6b4193522ad22cbe3800164022a34b94b2c2e899cc1c
```

You can easyly 

Use Case Examples
-----------------

You can use BTC Sniffer to easily:

1) Push notifications to an external messaging server ( Amazon SNS, ZeroMQ, RabbitMQ, etc )
2) Store real time transactions on any database format you want ( MySQL, MongoDB, etc )
3) Use sockets to display real time stream of network events on your website
4) Create a real time charts and statistics

And anything else you can think of. :)

Aditional Resources
-------------------

* [bitcoind](https://github.com/bitcoin/bitcoin)
* [pynode](https://github.com/jgarzik/pynode)

Contributing
------------

1. Fork it.
2. Create a branch (`git checkout -b my_markup`)
3. Commit your changes (`git commit -am "Added Snarkdown"`)
4. Push to the branch (`git push origin my_markup`)
5. Create an [Issue][1] with a link to your branch
6. Enjoy a refreshing orange juice and wait

Colaborators
------------

Thanks to the following colaborators:

* [sebicas](https://github.com/sebicas)