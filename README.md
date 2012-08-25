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

 Bitcoin Network Sniffer v0.0.2
 -------------------------------------------------------------------------
 Connecting to Bitcoin Node IP # 173.242.112.53:8333
 Connected & Sniffing :)

- Valid TX: b5d7c8cc5928cf9eb1d2b1707bea117b068ced9cf658ad720390078c4e393c4c

     16PMf9Yi1hy9C1nCiWfiXNoPNaHaC6ipBK for 12.33436000
     1AimQmFs6dkd1dFPopcZ8VC7Sc5HJGYfKk for 0.00016000

 - Valid TX: 81cf6efd753db1a1695297f95262838804aa9124da52a1000d4d0456bbd84654

     1J9G5VnQyShSzetZNmE9bFFSWmnTfedb3q for 1.54410000
     1LdXRVAATSYRVuherLi3gB7HpmPaPTpLh7 for 0.01560000

 - Valid TX: cd62bdabe87f4bfed98f1de6fc78a0f273e23aafc3ff89d7fccf5891fe4ad4e3

     1K4y7R89JzhWe42uH6cubAJ8A8APk9mCqE for 34.99941317
     1BRyszipKLfwj44r85wEVRW7BUCrgofbgd for 3.00000000

 - Valid Block: 00000000000003f57d766770ac6015a661542d5b7ba34b84d89aa80da5d2f294

 - Valid TX: c75be564867cb0aa2d9c7ba8628f28fe0e9c05938d39336007c2a18aa91a0f6e

     1FBqPQg3VsybSTLw5gpNhTg4N1jikSRW4X for 47.28058819
     1KXarmngRew1kr3tHj4RnBJNpcEtJxiBZL for 0.06800000

 - Valid TX: 66a3afd0a246a42d780e245e8eab9c4314c2919dcccbef1f90bff62b4fcfd4c4

     1MUjNPQVk3eztHXbkwCwuD249P1CjQL7Hc for 0.01008070
     1KRSKQb4zAn2WoYrNpHUChbaJB1MuK3gMj for 0.00022020
     1DgT9ugHk5rXvg53osVKFJxyt9Mijw6QYF for 0.00100000
     1CZ1voXst65eWxisDgoEKwCJ37opnDHG3d for 0.00061325
     1C28Zz49eYJrrweQNC33nBVFrEUb23kiyP for 0.00013165
```

Use Case Examples
-----------------

You can use BTC Sniffer to easily:

1. Push notifications to an external messaging server ( Amazon SNS, ZeroMQ, RabbitMQ, etc )
2. Store real time transactions on any database format you want ( MySQL, MongoDB, etc )
3. Use sockets to display real time stream of network events on your website
4. Create a real time charts and statistics

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