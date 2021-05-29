-----BEGIN PGP SIGNED MESSAGE-----
Hash: SHA1

HOWTO:  Build GnuPG on OS X

by Gordon Worley <redbird@mac.com>
updated by Alexander Nouak <macgpg@zeitform.de>

Version 4.29.1 (12 January 2016)

Introduction:

This document describes how to build GnuPG on Mac OS X 10.2+.  The process
is exactly the same as for any Unix system, but this howto is something of a
tradition (and you never know when Darwin might get crazy again).

Please keep in mind that you need to have XCode or Developer Tools respectivly 
as well as the BSD Subsystem installed

For the latest version of this document, check the Mac GPG Website
<http://macgpg.sourceforge.net/>.


How To:

Begin by downloading and verifying the GnuPG archives from
<http://www.gnupg.org/>.  Here's what to type:

curl -O ftp://ftp.gnupg.org/gcrypt/gnupg/gnupg-1.4.20.tar.gz
curl -O ftp://ftp.gnupg.org/gcrypt/gnupg/gnupg-1.4.20.tar.gz.sig

  If this server does not work please take a look at the mirrors page of GnuPG
  at http://www.gnupg.org/(en)/download/mirrors.html, choose a mirror and 
  replace the URL in an appropriate way. For instance choose
  curl -O ftp://ftp.franken.de/pub/crypt/mirror/ftp.gnupg.org/gcrypt/gnupg/
  gnupg-1.4.20.tar.gz

To verify:

gpg --verify gnupg-1.4.20.tar.gz.sig

or, if you don't have an older copy of GnuPG or another OpenPGP program
(NEVER verify the version of GnuPG you download with itself), use the SHA-1
checksums found on the GnuPG Web site and compare with the checksum from:

openssl sha1 gnupg-1.4.20.tar.gz

The checksum for this version should be: 
359e464bcabbe370696e3dba45a1d63968c06ab3

Next, untar GnuPG:

tar -xzf gnupg-1.4.20.tar.gz

And move into the GnuPG directory:

cd gnupg-1.4.20

  If you need to include or exclude anything else please run the following
  command to get a list of all options available:

  ./configure -h

Now you need to set up GnuPG to build on your system.  You do this by
running configure:

./configure

Once you have everything configured, it's time to compile GnuPG by running:

make

(Tip for Power Users:  To help make run even faster, use the -jn option to
 overlap processes that make spawns where n is the number of processors on
 your system plus one.  For example, on a single processor eMac, you'd use
 'make -j2'.)

Optionally, you can run make check before you install to make sure that your
system will be safe to run GnuPG on.

make check

If all tests pass, the only thing left to do is type:

sudo make install

And, voila!  GnuPG should be installed on your computer!

After you have GnuPG installed, it wouldn't hurt to check the quality of the
random numbers being produced by /dev/random.  To test this, first type:

gpg --gen-random 0 > rnd &

and after a little while kill the process (once you've got 20 or 30 MB of
random numbers).  Then, using a program like ent, check the quality of the
numbers.  Of particular interest will be the entropy, compressibility, and
chi^2 p-value (this should be as high as possible, as low as possible, and
as close to .5 as possible, respectively; see ent documentation for more
details).



-----BEGIN PGP SIGNATURE-----
Version: GnuPG v1.4
Comment: GPGTools - http://gpgtools.org

iEYEARECAAYFAlaUrxsACgkQ0HWns9BC0+sLWwCg1d3ncSarP3mTl70LASjbi7Vj
ZmQAn0PVIxjn2GVjrYjPIMUnU6ZKdGte
=qNJi
-----END PGP SIGNATURE-----
