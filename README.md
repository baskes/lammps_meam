# lammps_meam
in.elastic with MEAM potential works erratically
typical failure:
lammps(72964,0x7fff78ef0300) malloc: *** error for object 0x7fc920433810: incorrect checksum for freed object - object was probably modified after being freed.
*** set a breakpoint in malloc_error_break to debug
[Mikes-MBP:72964] *** Process received signal ***
[Mikes-MBP:72964] Signal: Abort trap: 6 (6)
[Mikes-MBP:72964] Signal code:  (0)
[Mikes-MBP:72964] [ 0] 0   libsystem_platform.dylib            0x00007fff8a899f1a _sigtramp + 26
[Mikes-MBP:72964] [ 1] 0   lammps                              0x0000000106115b41 c.3679 + 157345
[Mikes-MBP:72964] [ 2] 0   libsystem_c.dylib                   0x00007fff9833a9ab abort + 129
[Mikes-MBP:72964] [ 3] 0   libsystem_malloc.dylib              0x00007fff95110fe2 szone_error + 625
[Mikes-MBP:72964] [ 4] 0   libsystem_malloc.dylib              0x00007fff951074d5 tiny_free_list_remove_ptr + 289
[Mikes-MBP:72964] [ 5] 0   libsystem_malloc.dylib              0x00007fff95105b2e szone_free_definite_size + 1583
[Mikes-MBP:72964] [ 6] 0   lammps                              0x0000000105c25628 _ZN9LAMMPS_NS4Atom11count_wordsEPKc + 178
[Mikes-MBP:72964] [ 7] 0   lammps                              0x0000000105f7b031 _ZN9LAMMPS_NS8PairMEAM10read_filesEPcS1_ + 1239
[Mikes-MBP:72964] [ 8] 0   lammps                              0x0000000105f7a91f _ZN9LAMMPS_NS8PairMEAM5coeffEiPPc + 573
[Mikes-MBP:72964] [ 9] 0   lammps                              0x0000000105dcfb59 _ZN9LAMMPS_NS5Input15execute_commandEv + 2681
[Mikes-MBP:72964] [10] 0   lammps                              0x0000000105dcee72 _ZN9LAMMPS_NS5Input4fileEv + 922
[Mikes-MBP:72964] [11] 0   lammps                              0x0000000105de0278 main + 75
[Mikes-MBP:72964] [12] 0   libdyld.dylib                       0x00007fff94efc5c9 start + 1
[Mikes-MBP:72964] *** End of error message ***
