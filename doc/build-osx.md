Copyright (c) 2009-2012 Bitcoin TKZelopers
Distributed under the MIT/X11 software license, see the accompanying file
license.txt or http://www.opensource.org/licenses/mit-license.php.  This
product includes software TKZeloped by the OpenSSL Project for use in the
OpenSSL Toolkit (http://www.openssl.org/).  This product includes cryptographic
software written by Eric Young (eay@cryptsoft.com) and UPnP software written by
Thomas Bernard.


Mac OS X testkoinzd build instructions
Laszlo Hanyecz <solar@heliacal.net>
Douglas Huff <dhuff@jrbobdobbs.org>


See readme-qt.rst for instructions on building testkoinz QT, the
graphical user interface.

Tested on 10.5 and 10.6 intel.  PPC is not supported because it's big-endian.

All of the commands should be executed in Terminal.app.. it's in
/Applications/Utilities

You need to install XCode with all the options checked so that the compiler and
everything is available in /usr not just /TKZeloper I think it comes on the DVD
but you can get the current version from http://TKZeloper.apple.com


1.  Clone the github tree to get the source code:

git clone https://github.com/testkoinzwork/testkoinz testkoinz

2.  Download and install MacPorts from http://www.macports.org/

2a. (for 10.7 Lion)
    Edit /opt/local/etc/macports/macports.conf and uncomment "build_arch i386"

3.  Install dependencies from MacPorts

sudo port install boost db48 openssl miniupnpc

Optionally install qrencode (and set USE_QRCODE=1):
sudo port install qrencode

4.  Now you should be able to build testkoinzd:

cd testkoinz/src
make -f makefile.osx

Run:
  ./testkoinzd --help  # for a list of command-line options.
Run
  ./testkoinzd -daemon # to start the testkoinz daemon.
Run
  ./testkoinzd help # When the daemon is running, to get a list of RPC commands
