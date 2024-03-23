NeoBytes core v0.12.1.3
=======================

https://www.neobytes.network


## What is NeoBytes?

NeoBytes is an experimental new digital currency that enables anonymous, instant payments to anyone, anywhere in the world. NeoBytes uses peer-to-peer technology to operate with no central authority: managing transactions and issuing money are carried out collectively by the network. NeoBytes Core is the name of the open source software which enables the use of this currency.

NeoBytes uses a hash algorithm NeoScrypt. Based on a total Proof of Work and Masternode system, it is accesible to everyone, it ensures a fair and stable return of investment for the Graphics Processing Units (GPUs) miners and the Masternode holders.

For more information, as well as an immediately useable, binary version of the NeoBytes Core software, see <https://www.neobytes.network>

## NeoBytes FAQ

**Launch Date**: June 1, 2021

**Blockchain Type**: Decentralized

**Ticker Symbol**: NBY

**Genesis Block Hash**: "NeoBytes Genesis born on June 1, 2021"

**Mining Algorithm**: NeoScrypt


## License
NeoBytes Core is released under the terms of the MIT license. See [COPYING](COPYING) for more information or see <https://opensource.org/licenses/MIT>.

## Development Process
The `develop` branch is regularly built and tested, but is not guaranteed to be completely stable.  Additionally, the develop branch represents ongoing development from which candidate releases will be cut.
The `master` branch represents the current stable version currently in production.
[Tags](https://github.com/neobytes-project/NeoBytes/tags) are created regularly to indicate new official, stable release versions of NeoBytes Core.

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md).

## Testing

### Automated Testing

Developers are required to write [unit tests](src/test/README.md) for new code, and to submit new unit tests for any old code that is changed. Unit tests can be compiled and run (assuming they weren't disabled in configure) with: `make check`. Further details on running and extending unit tests can be found in [/src/test/README.md](/src/test/README.md).

There are also [regression and integration tests](/test), written in Python, that are run automatically on the build server.  These tests can be run (if the [test dependencies](/test) are installed) with: `test/functional/test_runner.py`

The Travis CI system makes sure that every pull request is built for Windows, Linux, and macOS, and that unit/sanity tests are run automatically.

### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the code. This is especially important for large or high-risk changes. It is useful to add a test plan to the pull request description if testing the changes is not straightforward.
