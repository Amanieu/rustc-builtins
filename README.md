[![Build Status][status]](https://travis-ci.org/japaric/rustc-builtins)

[status]: https://travis-ci.org/japaric/rustc-builtins.svg?branch=master

# `rustc-builtins`

> [WIP] Porting `compiler-rt` intrinsics to Rust

See [rust-lang/rust#35437][0].

[0]: https://github.com/rust-lang/rust/issues/35437

## Contributing

1. Pick one or more intrinsics from the [pending list][/#progress].
2. Fork this repository
3. Port the intrinsic(s) and their corresponding [unit tests][1] from their [C implementation][2] to
   Rust.
4. Send a Pull Request (PR)
5. Once the PR passes our extensive [testing infrastructure][3], we'll merge it!
6. Celebrate :tada:

[1]: https://github.com/rust-lang/compiler-rt/tree/8598065bd965d9713bfafb6c1e766d63a7b17b89/test/builtins/Unit
[2]: https://github.com/rust-lang/compiler-rt/tree/8598065bd965d9713bfafb6c1e766d63a7b17b89/lib/builtins
[3]: https://travis-ci.org/japaric/rustc-builtins

## Progress

The intrinsics that involve quadruple precision floating point numbers ("`f128`") has been crossed
off because Rust doesn't support them.

- [ ] absvdi2.c
- [ ] absvsi2.c
- [ ] absvti2.c
- [ ] adddf3.c
- [ ] addsf3.c
- [ ] addtf3.c
- [ ] addvdi3.c
- [ ] addvsi3.c
- [ ] addvti3.c
- [ ] apple_versioning.c
- [ ] arm/adddf3vfp.S
- [ ] arm/addsf3vfp.S
- [ ] arm/aeabi_cdcmp.S
- [ ] arm/aeabi_cdcmpeq_check_nan.c
- [ ] arm/aeabi_cfcmp.S
- [ ] arm/aeabi_cfcmpeq_check_nan.c
- [ ] arm/aeabi_dcmp.S
- [ ] arm/aeabi_div0.c
- [ ] arm/aeabi_drsub.c
- [ ] arm/aeabi_fcmp.S
- [ ] arm/aeabi_frsub.c
- [ ] arm/aeabi_idivmod.S
- [ ] arm/aeabi_ldivmod.S
- [ ] arm/aeabi_uidivmod.S
- [ ] arm/aeabi_uldivmod.S
- [ ] arm/bswapdi2.S
- [ ] arm/bswapsi2.S
- [ ] arm/clzdi2.S
- [ ] arm/clzsi2.S
- [ ] arm/comparesf2.S
- [ ] arm/divdf3vfp.S
- [ ] arm/divmodsi4.S
- [ ] arm/divsf3vfp.S
- [ ] arm/divsi3.S
- [ ] arm/eqdf2vfp.S
- [ ] arm/eqsf2vfp.S
- [ ] arm/extendsfdf2vfp.S
- [ ] arm/fixdfsivfp.S
- [ ] arm/fixsfsivfp.S
- [ ] arm/fixunsdfsivfp.S
- [ ] arm/fixunssfsivfp.S
- [ ] arm/floatsidfvfp.S
- [ ] arm/floatsisfvfp.S
- [ ] arm/floatunssidfvfp.S
- [ ] arm/floatunssisfvfp.S
- [ ] arm/gedf2vfp.S
- [ ] arm/gesf2vfp.S
- [ ] arm/gtdf2vfp.S
- [ ] arm/gtsf2vfp.S
- [ ] arm/ledf2vfp.S
- [ ] arm/lesf2vfp.S
- [ ] arm/ltdf2vfp.S
- [ ] arm/ltsf2vfp.S
- [ ] arm/modsi3.S
- [ ] arm/muldf3vfp.S
- [ ] arm/mulsf3vfp.S
- [ ] arm/nedf2vfp.S
- [ ] arm/negdf2vfp.S
- [ ] arm/negsf2vfp.S
- [ ] arm/nesf2vfp.S
- [ ] arm/restore_vfp_d8_d15_regs.S
- [ ] arm/save_vfp_d8_d15_regs.S
- [ ] arm/softfloat-alias.list
- [ ] arm/subdf3vfp.S
- [ ] arm/subsf3vfp.S
- [ ] arm/switch16.S
- [ ] arm/switch32.S
- [ ] arm/switch8.S
- [ ] arm/switchu8.S
- [ ] arm/sync_fetch_and_add_4.S
- [ ] arm/sync_fetch_and_add_8.S
- [ ] arm/sync_fetch_and_and_4.S
- [ ] arm/sync_fetch_and_and_8.S
- [ ] arm/sync_fetch_and_max_4.S
- [ ] arm/sync_fetch_and_max_8.S
- [ ] arm/sync_fetch_and_min_4.S
- [ ] arm/sync_fetch_and_min_8.S
- [ ] arm/sync_fetch_and_nand_4.S
- [ ] arm/sync_fetch_and_nand_8.S
- [ ] arm/sync_fetch_and_or_4.S
- [ ] arm/sync_fetch_and_or_8.S
- [ ] arm/sync_fetch_and_sub_4.S
- [ ] arm/sync_fetch_and_sub_8.S
- [ ] arm/sync_fetch_and_umax_4.S
- [ ] arm/sync_fetch_and_umax_8.S
- [ ] arm/sync_fetch_and_umin_4.S
- [ ] arm/sync_fetch_and_umin_8.S
- [ ] arm/sync_fetch_and_xor_4.S
- [ ] arm/sync_fetch_and_xor_8.S
- [ ] arm/sync_synchronize.S
- [ ] arm/truncdfsf2vfp.S
- [ ] arm/udivmodsi4.S
- [ ] arm/udivsi3.S
- [ ] arm/umodsi3.S
- [ ] arm/unorddf2vfp.S
- [ ] arm/unordsf2vfp.S
- [ ] ashldi3.c
- [ ] ashlti3.c
- [ ] ashrdi3.c
- [ ] ashrti3.c
- [ ] atomic.c
- [ ] atomic_flag_clear.c
- [ ] atomic_flag_clear_explicit.c
- [ ] atomic_flag_test_and_set.c
- [ ] atomic_flag_test_and_set_explicit.c
- [ ] atomic_signal_fence.c
- [ ] atomic_thread_fence.c
- [ ] clear_cache.c
- [ ] clzdi2.c
- [ ] clzsi2.c
- [ ] clzti2.c
- [ ] cmpdi2.c
- [ ] cmpti2.c
- [ ] comparedf2.c
- [ ] comparesf2.c
- [ ] comparetf2.c
- [ ] cpu_model.c
- [ ] ctzdi2.c
- [ ] ctzsi2.c
- [ ] ctzti2.c
- [ ] divdc3.c
- [ ] divdf3.c
- [ ] divdi3.c
- [ ] divmoddi4.c
- [ ] divmodsi4.c
- [ ] divsc3.c
- [ ] divsf3.c
- [ ] divsi3.c
- [ ] divtc3.c
- [ ] divtf3.c
- [ ] divti3.c
- [ ] divxc3.c
- [ ] emutls.c
- [ ] enable_execute_stack.c
- [ ] eprintf.c
- [ ] extenddftf2.c
- [ ] extendhfsf2.c
- [ ] extendsfdf2.c
- [ ] extendsftf2.c
- [ ] ffsdi2.c
- [ ] ffsti2.c
- [ ] fixdfdi.c
- [ ] fixdfsi.c
- [ ] fixdfti.c
- [ ] fixsfdi.c
- [ ] fixsfsi.c
- [ ] fixsfti.c
- [ ] fixtfdi.c
- [ ] fixtfsi.c
- [ ] fixtfti.c
- [ ] fixunsdfdi.c
- [ ] fixunsdfsi.c
- [ ] fixunsdfti.c
- [ ] fixunssfdi.c
- [ ] fixunssfsi.c
- [ ] fixunssfti.c
- [ ] fixunstfdi.c
- [ ] fixunstfsi.c
- [ ] fixunstfti.c
- [ ] floatdidf.c
- [ ] floatdisf.c
- [ ] floatditf.c
- [ ] floatsidf.c
- [ ] floatsisf.c
- [ ] floatsitf.c
- [ ] floattidf.c
- [ ] floattisf.c
- [ ] floatundidf.c
- [ ] floatundisf.c
- [ ] floatunditf.c
- [ ] floatunsidf.c
- [ ] floatunsisf.c
- [ ] floatunsitf.c
- [ ] floatuntidf.c
- [ ] floatuntisf.c
- [ ] gcc_personality_v0.c
- [ ] i386/ashldi3.S
- [ ] i386/ashrdi3.S
- [ ] i386/chkstk.S
- [ ] i386/chkstk2.S
- [ ] i386/divdi3.S
- [ ] i386/floatdidf.S
- [ ] i386/floatdisf.S
- [ ] i386/floatundidf.S
- [ ] i386/floatundisf.S
- [ ] i386/lshrdi3.S
- [ ] i386/moddi3.S
- [ ] i386/muldi3.S
- [ ] i386/udivdi3.S
- [ ] i386/umoddi3.S
- [ ] int_util.c
- [ ] lshrdi3.c
- [ ] lshrti3.c
- [ ] moddi3.c
- [ ] modsi3.c
- [ ] modti3.c
- [ ] muldc3.c
- [ ] muldf3.c
- [ ] muldi3.c
- [ ] mulodi4.c
- [ ] mulosi4.c
- [ ] muloti4.c
- [ ] mulsc3.c
- [ ] mulsf3.c
- [ ] multc3.c
- [ ] multf3.c
- [ ] multi3.c
- [ ] mulvdi3.c
- [ ] mulvsi3.c
- [ ] mulvti3.c
- [ ] mulxc3.c
- [ ] negdf2.c
- [ ] negdi2.c
- [ ] negsf2.c
- [ ] negti2.c
- [ ] negvdi2.c
- [ ] negvsi2.c
- [ ] negvti2.c
- [ ] paritydi2.c
- [ ] paritysi2.c
- [ ] parityti2.c
- [ ] popcountdi2.c
- [ ] popcountsi2.c
- [ ] popcountti2.c
- [ ] powidf2.c
- [ ] powisf2.c
- [ ] powitf2.c
- [ ] ppc/divtc3.c
- [ ] ppc/fixtfdi.c
- [ ] ppc/fixunstfdi.c
- [ ] ppc/floatditf.c
- [ ] ppc/floatunditf.c
- [ ] ppc/gcc_qadd.c
- [ ] ppc/gcc_qdiv.c
- [ ] ppc/gcc_qmul.c
- [ ] ppc/gcc_qsub.c
- [ ] ppc/multc3.c
- [ ] ppc/restFP.S
- [ ] ppc/saveFP.S
- [ ] subdf3.c
- [ ] subsf3.c
- [ ] subtf3.c
- [ ] subvdi3.c
- [ ] subvsi3.c
- [ ] subvti3.c
- [ ] trampoline_setup.c
- [ ] truncdfhf2.c
- [ ] truncdfsf2.c
- [ ] truncsfhf2.c
- [ ] trunctfdf2.c
- [ ] trunctfsf2.c
- [ ] ucmpdi2.c
- [ ] ucmpti2.c
- [ ] udivdi3.c
- [ ] udivmoddi4.c
- [ ] udivmodsi4.c
- [ ] udivmodti4.c
- [ ] udivsi3.c
- [ ] udivti3.c
- [ ] umoddi3.c
- [ ] umodsi3.c
- [ ] umodti3.c
- [ ] x86_64/chkstk.S
- [ ] x86_64/chkstk2.S
- [ ] x86_64/floatundidf.S
- [ ] x86_64/floatundisf.S
- [x] arm/aeabi_memcmp.S
- [x] arm/aeabi_memcpy.S
- [x] arm/aeabi_memmove.S
- [x] arm/aeabi_memset.S
- [x] x86_64/floatdidf.c
- [x] x86_64/floatdisf.c
- ~~fixunsxfdi.c~~
- ~~fixunsxfsi.c~~
- ~~fixunsxfti.c~~
- ~~fixxfdi.c~~
- ~~fixxfti.c~~
- ~~floatdixf.c~~
- ~~floattixf.c~~
- ~~floatundixf.c~~
- ~~floatuntixf.c~~
- ~~i386/floatdixf.S~~
- ~~i386/floatundixf.S~~
- ~~powixf2.c~~
- ~~x86_64/floatdixf.c~~
- ~~x86_64/floatundixf.S~~

## License

Licensed under either of

- Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE) or
  http://www.apache.org/licenses/LICENSE-2.0)
- MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.

### Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted for inclusion in the
work by you, as defined in the Apache-2.0 license, shall be dual licensed as above, without any
additional terms or conditions.
