# Apple II Audit

This repository contains routines to audit Apple II computers (II,
II+, IIe, IIc), providing information about hardware, ROM versions,
RAM configuration, and behavior.

The file to download and try is
[audit/audit.dsk](https://github.com/zellyn/a2audit/blob/master/audit/audit.dsk).

![Seagull Srs Micro Software](img/seagull-srs.png)

Eventually, it should comprise a complete emulator test suite,
enabling emulator writers to systematically identify and eliminate
software-testable differences from real hardware. If a difference
visible to code can be found, a test should be added to this suite.

# Error messages

Error messages can be viewed at
[zellyn.com/a2audit/a2audit/v0](http://zellyn.com/a2audit/v0/) or
[on github](https://github.com/zellyn/a2audit/blob/master/v0/index.md).

## Status

### Done

- [x] toolchain for automation ([diskii](https://github.com/zellyn/diskii))
- [x] sha1sum assembly code (currently not used yet because it's slow)
- [x] language card tests
- [x] main/auxiliary memory softswitch behavior tests
- [x] softswitch reading tests
- [x] Incorporate Cxxx testing into data-driven test
- [x] Add testcases for Cxxx testing
- [x] duplicate HOME and COUT routines from AppleII, so IIe tests
      don't depend on Cxxx ROM working
- [x] Some simple "same result from two different modes" graphics tests

### TODO

- [ ] IIe: check that we really have 128K (aux switching actually does
      anything)
- [ ] IIe: don't test auxmem softswitches if we only have 64k
- [ ] weirder softswitch behavior corner cases
- [ ] floating-bus tests
- [ ] dbl lores tests
- [ ] weird lores tests
- [ ] undelayed hires tests

## Raison d'être

This test suite is a step on the way to implementing Apple IIe
(enhanced) support in
[OpenEmulator](http://openemulatorproject.github.io/): I may alternate
adding tests here and features there.

## Contributors

- [Zellyn Hunter](https://github.com/zellyn)
- [Peter Ferrie ("qkumba")](https://github.com/peterferrie)
- [Cedric Beust](https://github.com/cbeust)

