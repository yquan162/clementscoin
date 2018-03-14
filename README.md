Clementscoin Core integration/staging tree
================================

http://clementstech.club

Copyright (c) 2009-2014 Bitcoin Developers
Copyright (c) 2011-2014 Litecoin Developers
Copyright (c) 2018 Clementscoin Developers

What is Clementscoin?
----------------

Clementscoin is an experimental digital currency that enables instant payments to
anyone, anywhere in the world. Clementscoin uses peer-to-peer technology to operate
with no central authority: managing transactions and issuing money are carried
out collectively by the network. Clementscoin Core is the name of open source
software which enables the use of this currency.

Specifications
--------------
 - 3.125 minute block targets
 - subsidy halves in 105k blocks
 - ~1.4 million total coins
 - 75 coins per block
 - 288 blocks to retarget difficulty
 - RPC Port - 3665
 - Connection Port - 3666

For more information, as well as an immediately useable, binary version of
the Clementscoin Core software, see [http:/clementstech.club](http://clementstech.club).

License
-------

Clementscoin is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------
The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/yquan162/clementscoin/tags) are created
regularly to indicate new official, stable release versions of Clementscoin Core.

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Clementscoin
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion with the devs and community.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./clementscoin-qt_test

### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the
code. This is especially important for large or high-risk changes. It is useful
to add a test plan to the pull request description if testing the changes is
not straightforward.

Translations
------------

We only accept translation fixes that are submitted through [Bitcoin Core's Transifex page](https://www.transifex.com/projects/p/bitcoin/).
Translations are converted to Clementscoin periodically.

Translations are periodically pulled from Transifex and merged into the git repository. See the
[translation process](doc/translation_process.md) for details on how this works.

**Important**: We do not accept translation changes as GitHub pull requests because the next
pull from Transifex would automatically overwrite them again.

