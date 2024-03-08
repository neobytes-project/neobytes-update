NeoBytes Core version 0.12.1 is now available from:

  <https://github.com/neobytes-project/neobytes/releases>

This is a new minor version release, bringing various bugfixes and other
improvements.

Please report bugs using the issue tracker at github:

  <https://github.com/neobytes-project/neobytes/issues>


Upgrading and downgrading
=========================

How to Upgrade
--------------
If you are running an older version, shut it down. Wait until it has completely
shut down (which might take a few minutes for older versions), then run the
installer (on Windows) or just copy over /Applications/Desire-Qt (on Mac) or
desired/desire-qt (on Linux). Because of the per-UTXO fix (see below) there is a
one-time database upgrade operation, so expect a slightly longer startup time on
the first run.

Downgrade warning
-----------------

Compatibility
==============

Notable changes
===============

(Developers: add your notes here as part of your pull requests whenever possible)

0.12.1 Change log
=================

Detailed release notes follow. This overview includes changes that affect
behavior, not code moves, refactors and string updates. For convenience in locating
the code changes and accompanying discussion, both the pull request and
git merge commit are mentioned.

### RPC and REST

Asm script outputs replacements for OP_NOP2 and OP_NOP3
-------------------------------------------------------

OP_NOP2 has been renamed to OP_CHECKLOCKTIMEVERIFY by [BIP 
65](https://github.com/bitcoin/bips/blob/master/bip-0065.mediawiki)

OP_NOP3 has been renamed to OP_CHECKSEQUENCEVERIFY by [BIP 
112](https://github.com/bitcoin/bips/blob/master/bip-0112.mediawiki)

The following outputs are affected by this change:
- RPC `getrawtransaction` (in verbose mode)
- RPC `decoderawtransaction`
- RPC `decodescript`
- REST `/rest/tx/` (JSON format)
- REST `/rest/block/` (JSON format when including extended tx details)
- `bitcoin-tx -json`

### ZMQ

Each ZMQ notification now contains an up-counting sequence number that allows
listeners to detect lost notifications.
The sequence number is always the last element in a multi-part ZMQ notification and
therefore backward compatible.
Each message type has its own counter.
(https://github.com/bitcoin/bitcoin/pull/7762)

### Configuration and command-line options

### Block and transaction handling

### P2P protocol and network code

### Validation

### Build system

### Wallet

### GUI

### Tests and QA

### Miscellaneous

Credits
=======

Thanks to everyone who directly contributed to this release:


As well as everyone that helped translating.

NeoBytes Core tree 0.12.x was a fork of Dash Core tree 0.12.x