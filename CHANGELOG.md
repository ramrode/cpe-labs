# Changelog

## [0.13.0](https://github.com/ramrode/cpe-labs/compare/v0.12.1...v0.13.0) (2026-11-06)


### ⚠ BREAKING CHANGES

* **usp:** every simulated USP agent now presents a different endpoint ID, for example os::0000C5-TEST0001 where it was os::0000C5TEST0001. A controller that already knows the agents sees them under new identities, and broker ACLs or credentials keyed on the old ID, or on a password derived from it, need updating.

### Added

* **cpe-sim:** realistic serials via {cpe:alnum:N} in serialPattern ([f18e1f6](https://github.com/ramrode/cpe-labs/commit/f18e1f6b10a35b88c22ddc3c09ea7a5026ac2223))
* **cpe-sim:** realistic serials via {cpe:alnum:N} in serialPattern ([c5d49a6](https://github.com/ramrode/cpe-labs/commit/c5d49a677f56da1c0b712d07d0603c851691cbcc))
* CWMP and USP CPE simulator, reference profiles, docs and CI ([3f386b3](https://github.com/ramrode/cpe-labs/commit/3f386b3fe9e35fe64436e6cde2c63a3f76e7446a))
* **cwmp:** a profile can defer parameters so SetParameterValues answers Status 1 ([#61](https://github.com/ramrode/cpe-labs/issues/61)) ([e406ccb](https://github.com/ramrode/cpe-labs/commit/e406ccb043fd28de887c29db62b7c2caa8698283))
* **cwmp:** a STUN client keeps a NAT binding open and answers UDP connection requests (TR-069 Annex G) ([#71](https://github.com/ramrode/cpe-labs/issues/71)) ([5db1761](https://github.com/ramrode/cpe-labs/commit/5db17619e6944a6a08e78f93dc0bc15ad33d2fdb))
* **cwmp:** device-internal writes honor notification attributes ([#34](https://github.com/ramrode/cpe-labs/issues/34)) ([620b680](https://github.com/ramrode/cpe-labs/commit/620b6804e9bbde57aae46657eaaa937192a61b48))
* **cwmp:** simulate firmware upgrade apply and reboot on Download ([fc83943](https://github.com/ramrode/cpe-labs/commit/fc8394344d82c37dfea551afd19d66d8eab6ddce))
* **cwmp:** simulate firmware upgrade apply and reboot on Download ([0924362](https://github.com/ramrode/cpe-labs/commit/0924362894caa7fda688011bd564388ebc8ba7ef))
* **diagnostics:** triggered diagnostics, and a neighbour scan to run one ([#27](https://github.com/ramrode/cpe-labs/issues/27)) ([e37fa3d](https://github.com/ramrode/cpe-labs/commit/e37fa3d39d3d56d126226c39f606299a041b7b8d))
* **harness:** icwmp, a real TR-069 client in a container ([#35](https://github.com/ramrode/cpe-labs/issues/35)) ([5bc1320](https://github.com/ramrode/cpe-labs/commit/5bc13208db8949377564243915f6fa4daddd24f1))
* **nat:** port-mapping tables that start empty and count honestly ([#32](https://github.com/ramrode/cpe-labs/issues/32)) ([ea0e324](https://github.com/ramrode/cpe-labs/commit/ea0e324be989ead007eb980aeb9e839a53bd2f59))
* **profiles:** a Sagemcom FAST5599 whose uplink is the last port and whose accounts are not Device.Users ([#57](https://github.com/ramrode/cpe-labs/issues/57)) ([4bc650a](https://github.com/ramrode/cpe-labs/commit/4bc650a70495dacf36ad78ac23ebddda23425c0d))
* **profiles:** a TR-098 gateway that supports bulk data collection ([#58](https://github.com/ramrode/cpe-labs/issues/58)) ([43f8716](https://github.com/ramrode/cpe-labs/commit/43f871649230d5456d4d7250c121a9dd151b7da7))
* **profiles:** a Zyxel EX3301-T0 gateway with two WX3100-T0 mesh extenders, dual-stack ([#78](https://github.com/ramrode/cpe-labs/issues/78)) ([a855b2c](https://github.com/ramrode/cpe-labs/commit/a855b2c452703c1e95fb736b202a472489010ac4))
* **profiles:** a Zyxel WX3100-T0 mesh extender, paired with the EX3301-T0 gateway profile ([#81](https://github.com/ramrode/cpe-labs/issues/81)) ([c3a547d](https://github.com/ramrode/cpe-labs/commit/c3a547d6793d8ea62fb32d1664b37fdc8b0a7ea5))
* **profiles:** an ASUS RT-AX88U that keeps its mesh, site survey and remote access under vendor trees ([#56](https://github.com/ramrode/cpe-labs/issues/56)) ([8a04ff3](https://github.com/ramrode/cpe-labs/commit/8a04ff374813bcf607ebaf56bb1bd772edd231e1))
* **profiles:** the EX3301-T0 declares its two firmware banks, so a USP controller can upgrade it ([#82](https://github.com/ramrode/cpe-labs/issues/82)) ([ee695eb](https://github.com/ramrode/cpe-labs/commit/ee695eb016159778ea5b9a5db2779160c4120600))
* **profiles:** the network diagnostics, on both data model families ([#29](https://github.com/ramrode/cpe-labs/issues/29)) ([2e8b421](https://github.com/ramrode/cpe-labs/commit/2e8b42198c6e0e8520b23d7376e46647efcb80e6))
* **profiles:** the NVG and FAST5598 expose their local account tables ([#54](https://github.com/ramrode/cpe-labs/issues/54)) ([fdd827d](https://github.com/ramrode/cpe-labs/commit/fdd827dc7e947602f724234689a07adf87f354f4))
* **profiles:** the second diagnostics wave on the sims ([#30](https://github.com/ramrode/cpe-labs/issues/30)) ([389bc0f](https://github.com/ramrode/cpe-labs/commit/389bc0fb760016cacd55c0d59c61cee1c9832fd7))
* **profiles:** TR-104 voice on the ARRIS, with scripted call activity ([#33](https://github.com/ramrode/cpe-labs/issues/33)) ([a34c28a](https://github.com/ramrode/cpe-labs/commit/a34c28a52196fecc93e45f5870e20227e36f4de7))
* **release:** publish prebuilt binaries on GitHub Releases ([55ebed1](https://github.com/ramrode/cpe-labs/commit/55ebed1c957e40ca668113aa84eb5f8598401f22))
* **release:** the changelog is generated and published on the docs site ([#37](https://github.com/ramrode/cpe-labs/issues/37)) ([d4f110d](https://github.com/ramrode/cpe-labs/commit/d4f110dd23126d72cab1d0c6e20cb2149553775e))
* **softwaremodules:** TR-157 software modules with an app that extends the data model ([#49](https://github.com/ramrode/cpe-labs/issues/49)) ([70c9cbd](https://github.com/ramrode/cpe-labs/commit/70c9cbdfa972e6fd2f16275cff660f37611ff3b6))
* **usp:** an agent can lose its uplink without telling the broker ([#51](https://github.com/ramrode/cpe-labs/issues/51)) ([ca3913d](https://github.com/ramrode/cpe-labs/commit/ca3913d350df428610e9ae9b0cf061803062a50e))
* **usp:** bulk data profiles push reports as the Push! event ([#50](https://github.com/ramrode/cpe-labs/issues/50)) ([ec36670](https://github.com/ramrode/cpe-labs/commit/ec366709dbf29da51ff5d5a12afa4eb4b032d6a4))
* **usp:** firmware upgrade simulation via async FirmwareImage commands ([a3ab9ac](https://github.com/ramrode/cpe-labs/commit/a3ab9ac3f750c4fd5eb9d94cefd812c9668a92ac))
* **usp:** run USP-only without an ACS ([78322e7](https://github.com/ramrode/cpe-labs/commit/78322e7fc72f52d9e0ffa3628232ac7bf273e567))
* **usp:** simulate firmware upgrade via async FirmwareImage commands ([5f824f4](https://github.com/ramrode/cpe-labs/commit/5f824f431bc059bee55d772e1b8acc5b7f2397d6))


### Fixed

* **cwmp:** a connection request session carries only its own event ([#67](https://github.com/ramrode/cpe-labs/issues/67)) ([8593368](https://github.com/ramrode/cpe-labs/commit/85933683d2756ceb2ea742c86b20a40b83ed4da7))
* **cwmp:** the periodic timer is re-armed after every tick and says so ([#68](https://github.com/ramrode/cpe-labs/issues/68)) ([d9e4f10](https://github.com/ramrode/cpe-labs/commit/d9e4f104c29d597ff61ca3de3463d347247e8d65))
* **harness:** the NAT container's UDP conntrack timeout is set the way Docker honours ([#73](https://github.com/ramrode/cpe-labs/issues/73)) ([46af458](https://github.com/ramrode/cpe-labs/commit/46af458c6ec7dcb072c49f779fdf6720f046a422))
* **profiles:** every example declares where its ACS credentials live ([#60](https://github.com/ramrode/cpe-labs/issues/60)) ([d35d347](https://github.com/ramrode/cpe-labs/commit/d35d347c9ba36c8cc09623d8ffcdc39609ba393f))
* **profiles:** scale profile reports the TR-069 forced-Inform set ([#12](https://github.com/ramrode/cpe-labs/issues/12)) ([96a4d1d](https://github.com/ramrode/cpe-labs/commit/96a4d1df2597cc6c9d86c78e93e310f102e35772))
* **profiles:** the ARRIS voice pool is sized for the whole fleet ([#28](https://github.com/ramrode/cpe-labs/issues/28)) ([d95e357](https://github.com/ramrode/cpe-labs/commit/d95e357076e14e27601601709a5c8078e44abb77))
* **profiles:** the boot Inform after a firmware Download carries the new version ([#48](https://github.com/ramrode/cpe-labs/issues/48)) ([0e22d5f](https://github.com/ramrode/cpe-labs/commit/0e22d5f37329940650079ccc7ed8d748d555f816))
* **profiles:** the Calix link fault lasts long enough to be seen ([#52](https://github.com/ramrode/cpe-labs/issues/52)) ([0cd9252](https://github.com/ramrode/cpe-labs/commit/0cd92527547dff76ae54f95808bb8ed27e9bfcba))
* **profiles:** the Calix link fault takes fifty agents dark, not the process ([#53](https://github.com/ramrode/cpe-labs/issues/53)) ([bb8acea](https://github.com/ramrode/cpe-labs/commit/bb8aceaf7bf4d10f1663f298b262049c29193fa1))
* **profiles:** the echo timestamps expand ([#31](https://github.com/ramrode/cpe-labs/issues/31)) ([e79a15d](https://github.com/ramrode/cpe-labs/commit/e79a15d38b68613650474bedd008b72ed5951efb))
* **usp:** a reboot or factory reset over USP brings a dual-stack CPE back on both protocols ([#84](https://github.com/ramrode/cpe-labs/issues/84)) ([241010e](https://github.com/ramrode/cpe-labs/commit/241010e23fcbf416c2b637b73e01a666a0fb950d))
* **usp:** endpoint IDs use the TR-369 os form, &lt;OUI&gt;-&lt;SerialNumber&gt; ([#62](https://github.com/ramrode/cpe-labs/issues/62)) ([524431f](https://github.com/ramrode/cpe-labs/commit/524431f5d14b024e80daeda190821c1aed3219c3))
* **usp:** keep the checksum default comment controller-neutral ([7eda2ca](https://github.com/ramrode/cpe-labs/commit/7eda2caa3ec3d26e63fd6d89940629b7806ebbb1))
* **usp:** stop double-logging endpoint_id on runner lines ([b5f19fb](https://github.com/ramrode/cpe-labs/commit/b5f19fb6dabc85b59e83b388d1b914d0848565c1))
* **usp:** the MQTT reply-to escapes only slashes, as R-MQTT.24 requires ([#65](https://github.com/ramrode/cpe-labs/issues/65)) ([fa54080](https://github.com/ramrode/cpe-labs/commit/fa540803fda9b1242c53d48fba1ce9e5a1e33177))

## [0.12.1](https://github.com/ispx-limited/cpe-labs/compare/v0.12.0...v0.12.1) (2026-11-05)


### Fixed

* **usp:** a reboot or factory reset over USP brings a dual-stack CPE back on both protocols ([#84](https://github.com/ispx-limited/cpe-labs/issues/84)) ([241010e](https://github.com/ispx-limited/cpe-labs/commit/241010e23fcbf416c2b637b73e01a666a0fb950d))

## [0.12.0](https://github.com/ispx-limited/cpe-labs/compare/v0.11.0...v0.12.0) (2026-11-05)


### Added

* **profiles:** a Zyxel WX3100-T0 mesh extender, paired with the EX3301-T0 gateway profile ([#81](https://github.com/ispx-limited/cpe-labs/issues/81)) ([c3a547d](https://github.com/ispx-limited/cpe-labs/commit/c3a547d6793d8ea62fb32d1664b37fdc8b0a7ea5))
* **profiles:** the EX3301-T0 declares its two firmware banks, so a USP controller can upgrade it ([#82](https://github.com/ispx-limited/cpe-labs/issues/82)) ([ee695eb](https://github.com/ispx-limited/cpe-labs/commit/ee695eb016159778ea5b9a5db2779160c4120600))

## [0.11.0](https://github.com/ispx-limited/cpe-labs/compare/v0.10.1...v0.11.0) (2026-11-05)


### Added

* **profiles:** a Zyxel EX3301-T0 gateway with two WX3100-T0 mesh extenders, dual-stack ([#78](https://github.com/ispx-limited/cpe-labs/issues/78)) ([a855b2c](https://github.com/ispx-limited/cpe-labs/commit/a855b2c452703c1e95fb736b202a472489010ac4))

## [0.10.1](https://github.com/ispx-limited/cpe-labs/compare/v0.10.0...v0.10.1) (2026-10-09)


### Fixed

* **harness:** the NAT container's UDP conntrack timeout is set the way Docker honours ([#73](https://github.com/ispx-limited/cpe-labs/issues/73)) ([46af458](https://github.com/ispx-limited/cpe-labs/commit/46af458c6ec7dcb072c49f779fdf6720f046a422))

## [0.10.0](https://github.com/ispx-limited/cpe-labs/compare/v0.9.1...v0.10.0) (2026-10-09)


### Added

* **cwmp:** a STUN client keeps a NAT binding open and answers UDP connection requests (TR-069 Annex G) ([#71](https://github.com/ispx-limited/cpe-labs/issues/71)) ([5db1761](https://github.com/ispx-limited/cpe-labs/commit/5db17619e6944a6a08e78f93dc0bc15ad33d2fdb))

## [0.9.1](https://github.com/ispx-limited/cpe-labs/compare/v0.9.0...v0.9.1) (2026-09-26)


### Fixed

* **cwmp:** the periodic timer is re-armed after every tick and says so ([#68](https://github.com/ispx-limited/cpe-labs/issues/68)) ([d9e4f10](https://github.com/ispx-limited/cpe-labs/commit/d9e4f104c29d597ff61ca3de3463d347247e8d65))

## [0.9.0](https://github.com/ispx-limited/cpe-labs/compare/v0.8.0...v0.9.0) (2026-09-15)


### ⚠ BREAKING CHANGES

* **usp:** every simulated USP agent now presents a different endpoint ID, for example os::0000C5-TEST0001 where it was os::0000C5TEST0001. A controller that already knows the agents sees them under new identities, and broker ACLs or credentials keyed on the old ID, or on a password derived from it, need updating.

### Fixed

* **cwmp:** a connection request session carries only its own event ([#67](https://github.com/ispx-limited/cpe-labs/issues/67)) ([8593368](https://github.com/ispx-limited/cpe-labs/commit/85933683d2756ceb2ea742c86b20a40b83ed4da7))
* **usp:** endpoint IDs use the TR-369 os form, &lt;OUI&gt;-&lt;SerialNumber&gt; ([#62](https://github.com/ispx-limited/cpe-labs/issues/62)) ([524431f](https://github.com/ispx-limited/cpe-labs/commit/524431f5d14b024e80daeda190821c1aed3219c3))
* **usp:** the MQTT reply-to escapes only slashes, as R-MQTT.24 requires ([#65](https://github.com/ispx-limited/cpe-labs/issues/65)) ([fa54080](https://github.com/ispx-limited/cpe-labs/commit/fa540803fda9b1242c53d48fba1ce9e5a1e33177))

## [0.8.0](https://github.com/ispx-limited/cpe-labs/compare/v0.7.0...v0.8.0) (2026-09-13)


### Added

* **cwmp:** a profile can defer parameters so SetParameterValues answers Status 1 ([#61](https://github.com/ispx-limited/cpe-labs/issues/61)) ([e406ccb](https://github.com/ispx-limited/cpe-labs/commit/e406ccb043fd28de887c29db62b7c2caa8698283))
* **profiles:** a Sagemcom FAST5599 whose uplink is the last port and whose accounts are not Device.Users ([#57](https://github.com/ispx-limited/cpe-labs/issues/57)) ([4bc650a](https://github.com/ispx-limited/cpe-labs/commit/4bc650a70495dacf36ad78ac23ebddda23425c0d))
* **profiles:** a TR-098 gateway that supports bulk data collection ([#58](https://github.com/ispx-limited/cpe-labs/issues/58)) ([43f8716](https://github.com/ispx-limited/cpe-labs/commit/43f871649230d5456d4d7250c121a9dd151b7da7))
* **profiles:** an ASUS RT-AX88U that keeps its mesh, site survey and remote access under vendor trees ([#56](https://github.com/ispx-limited/cpe-labs/issues/56)) ([8a04ff3](https://github.com/ispx-limited/cpe-labs/commit/8a04ff374813bcf607ebaf56bb1bd772edd231e1))


### Fixed

* **profiles:** every example declares where its ACS credentials live ([#60](https://github.com/ispx-limited/cpe-labs/issues/60)) ([d35d347](https://github.com/ispx-limited/cpe-labs/commit/d35d347c9ba36c8cc09623d8ffcdc39609ba393f))

## [0.7.0](https://github.com/ispx-limited/cpe-labs/compare/v0.6.0...v0.7.0) (2026-08-24)


### Added

* **profiles:** the NVG and FAST5598 expose their local account tables ([#54](https://github.com/ispx-limited/cpe-labs/issues/54)) ([fdd827d](https://github.com/ispx-limited/cpe-labs/commit/fdd827dc7e947602f724234689a07adf87f354f4))
* **release:** the changelog is generated and published on the docs site ([#37](https://github.com/ispx-limited/cpe-labs/issues/37)) ([d4f110d](https://github.com/ispx-limited/cpe-labs/commit/d4f110dd23126d72cab1d0c6e20cb2149553775e))
* **softwaremodules:** TR-157 software modules with an app that extends the data model ([#49](https://github.com/ispx-limited/cpe-labs/issues/49)) ([70c9cbd](https://github.com/ispx-limited/cpe-labs/commit/70c9cbdfa972e6fd2f16275cff660f37611ff3b6))
* **usp:** an agent can lose its uplink without telling the broker ([#51](https://github.com/ispx-limited/cpe-labs/issues/51)) ([ca3913d](https://github.com/ispx-limited/cpe-labs/commit/ca3913d350df428610e9ae9b0cf061803062a50e))
* **usp:** bulk data profiles push reports as the Push! event ([#50](https://github.com/ispx-limited/cpe-labs/issues/50)) ([ec36670](https://github.com/ispx-limited/cpe-labs/commit/ec366709dbf29da51ff5d5a12afa4eb4b032d6a4))


### Fixed

* **profiles:** the boot Inform after a firmware Download carries the new version ([#48](https://github.com/ispx-limited/cpe-labs/issues/48)) ([0e22d5f](https://github.com/ispx-limited/cpe-labs/commit/0e22d5f37329940650079ccc7ed8d748d555f816))
* **profiles:** the Calix link fault lasts long enough to be seen ([#52](https://github.com/ispx-limited/cpe-labs/issues/52)) ([0cd9252](https://github.com/ispx-limited/cpe-labs/commit/0cd92527547dff76ae54f95808bb8ed27e9bfcba))
* **profiles:** the Calix link fault takes fifty agents dark, not the process ([#53](https://github.com/ispx-limited/cpe-labs/issues/53)) ([bb8acea](https://github.com/ispx-limited/cpe-labs/commit/bb8aceaf7bf4d10f1663f298b262049c29193fa1))

## 0.6.0 (2026-08-20)

### Added

* Triggered diagnostics on the simulated CPEs, including a neighbour scan, on
  both data model families.
* NAT port-mapping tables that start empty and count what the ACS adds.
* TR-104 voice on the ARRIS profile, with scripted call activity.
* Device-internal writes honor the notification attributes set by the ACS.
* icwmp, a real TR-069 client, runs in a container alongside the simulators.
* Sagemcom F@ST 5280 and ARRIS NVG599 reference gateway profiles.

### Fixed

* The ARRIS voice pool is sized for the whole fleet.
* Echo timestamps expand as the profile declares.
