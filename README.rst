**Pure Python implementation of rpmvercmp.-- Archived Repository**  

**Notice: This repository is part of a Conary/rpath project at SAS that is no longer supported or maintained. Hence, the repository is being archived and will live in a read-only state moving forward. Issues, pull requests, and changes will no longer be accepted.**

The RPM Package Manager (http://rpm.org) has a version comparision algorithm,
implemented in its C library, which performs the comparison in a certain way.

In certain circumstances, where the C library is not installable (for example,
on non-rpm based systems), or does not support the desired version of the
python interpreter, the pure-python implementation may be useful.

Source Code
===========
https://github.com/sassoftware/python-rpm-vercmp

Installation
============
        $ pip install rpm_vercmp

Usage
=====

        import rpm_vercmp
        assert rpm_vercmp.vercmp("1.0", "1.0") == 0
        assert rpm_vercmp.vercmp("1.0", "1.1") == -1

Testing
=======
The testsuite uses rpm's test file in m4 format.
The file cat be fetched from:
https://raw.githubusercontent.com/rpm-software-management/rpm/master/tests/rpmvercmp.at
