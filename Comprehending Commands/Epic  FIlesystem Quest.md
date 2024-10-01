# An Epic Filesystem Quest

This Problem was a test of all the previous lessons(cat,ls and cd) and their intricacies, having the user traverse through a lot of hoops before finally arriving at their flag

My Approach:
- change directory into `/` using `cd /` 
- use `ls` to see the contents, I infer that CUE is the hint(or cue) that I need to view
- I view it using `cat CUE`, it tells me the next hint is in `/usr/share/doc/adduser/examples/adduser.local.conf.examples/skel`
- the hint also told me that is 'trapped' , so I cant cd into it, knowing that I directly view the contents using `ls /usr/share/doc/adduser/examples/adduser.local.conf.examples/skel`, here I see the next clue WHISPER-TRAPPED
- WHISPER-TRAPPED leads me to `/usr/local/lib/python3.8/dist-packages/jinja2/__pycache__` but the clue here is delayed so I need to `cd` into the directory before seeing the clue there
- I run `cd /usr/local/lib/python3.8/dist-packages/jinja2/__pycache__` followed by `ls` to find the next hint SNIPPET
- on executing `cat SNIPPET`, it tells me the next clue is in `/opt/aflplusplus/nyx_mode/QEMU-Nyx/tests/tcg/mips/user/ase/msa/int-add`





```bash
Connected!
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
CUE  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin  challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat CUE
Lucky listing!
The next clue is in: /usr/share/doc/adduser/examples/adduser.local.conf.examples/skel

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/$ ls /usr/share/doc/adduser/examples/adduser.local.conf.examples/skel
WHISPER-TRAPPED  dot.bash_logout  dot.bash_profile  dot.bashrc
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/share/doc/adduser/examples/adduser.local.conf.examples/skel/WHISPER-TRAPPED
Yahaha, you found me!
The next clue is in: /usr/local/lib/python3.8/dist-packages/jinja2/__pycache__

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/local/lib/python3.8/dist-packages/jinja2/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/jinja2/__pycache__$ ls
SNIPPET                     debug.cpython-38.pyc        lexer.cpython-38.pyc        runtime.cpython-38.pyc
__init__.cpython-38.pyc     defaults.cpython-38.pyc     loaders.cpython-38.pyc      sandbox.cpython-38.pyc
_identifier.cpython-38.pyc  environment.cpython-38.pyc  meta.cpython-38.pyc         tests.cpython-38.pyc
async_utils.cpython-38.pyc  exceptions.cpython-38.pyc   nativetypes.cpython-38.pyc  utils.cpython-38.pyc
bccache.cpython-38.pyc      ext.cpython-38.pyc          nodes.cpython-38.pyc        visitor.cpython-38.pyc
compiler.cpython-38.pyc     filters.cpython-38.pyc      optimizer.cpython-38.pyc
constants.cpython-38.pyc    idtracking.cpython-38.pyc   parser.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/jinja2/__pycache__$ cat SNIPPET
Great sleuthing!
The next clue is in: /opt/aflplusplus/nyx_mode/QEMU-Nyx/tests/tcg/mips/user/ase/msa/int-add
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/jinja2/__pycache__$ cd /opt/aflplusplus/nyx_mode/QEMU-Nyx/tests/tcg/mips/user/ase/msa/int-add
hacker@commands~an-epic-filesystem-quest:/opt/aflplusplus/nyx_mode/QEMU-Nyx/tests/tcg/mips/user/ase/msa/int-add$ ls
CLUE                 test_msa_adds_a_d.c  test_msa_adds_s_w.c  test_msa_addv_d.c    test_msa_hadd_u_d.c
test_msa_add_a_b.c   test_msa_adds_a_h.c  test_msa_adds_u_b.c  test_msa_addv_h.c    test_msa_hadd_u_h.c
test_msa_add_a_d.c   test_msa_adds_a_w.c  test_msa_adds_u_d.c  test_msa_addv_w.c    test_msa_hadd_u_w.c
test_msa_add_a_h.c   test_msa_adds_s_b.c  test_msa_adds_u_h.c  test_msa_hadd_s_d.c
test_msa_add_a_w.c   test_msa_adds_s_d.c  test_msa_adds_u_w.c  test_msa_hadd_s_h.c
test_msa_adds_a_b.c  test_msa_adds_s_h.c  test_msa_addv_b.c    test_msa_hadd_s_w.c
hacker@commands~an-epic-filesystem-quest:/opt/aflplusplus/nyx_mode/QEMU-Nyx/tests/tcg/mips/user/ase/msa/int-add$ cat CLU
E
Tubular find!
The next clue is in: /usr/share/doc/gir1.2-gdkpixbuf-2.0
hacker@commands~an-epic-filesystem-quest:/opt/aflplusplus/nyx_mode/QEMU-Nyx/tests/tcg/mips/user/ase/msa/int-add$ cd /usr/share/doc/gir1.2-gdkpixbuf-2.0
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/gir1.2-gdkpixbuf-2.0$ ls
SECRET  changelog.Debian.gz  copyright
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/gir1.2-gdkpixbuf-2.0$ cat SECRET
Great sleuthing!
The next clue is in: /usr/share/doc/librbd1

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/gir1.2-gdkpixbuf-2.0$ cd /usr/share/doc/librbd1
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/librbd1$ ls -a
.  ..  .NUGGET  changelog.Debian.gz  copyright
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/librbd1$ cat .NUGGET
Great sleuthing!
The next clue is in: /opt/aflplusplus/nyx_mode/QEMU-Nyx/roms/qboot
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/librbd1$ cd /opt/aflplusplus/nyx_mode/QEMU-Nyx/roms/qboot
hacker@commands~an-epic-filesystem-quest:/opt/aflplusplus/nyx_mode/QEMU-Nyx/roms/qboot$ ls
TIP
hacker@commands~an-epic-filesystem-quest:/opt/aflplusplus/nyx_mode/QEMU-Nyx/roms/qboot$ cat TIP
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/arch/parisc/include/asm

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/aflplusplus/nyx_mode/QEMU-Nyx/roms/qboot$ cd /opt/linux/linux-5.4/arch/parisc/include/asm
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/parisc/include/asm$ ls -a
.              cacheflush.h       ftrace.h      kmap_types.h     pci.h          sections.h        thread_info.h
..             checksum.h         futex.h       kprobes.h        pdc.h          serial.h          timex.h
.README        cmpxchg.h          grfioctl.h    ldcw.h           pdc_chassis.h  shmparam.h        tlb.h
Kbuild         compat.h           hardirq.h     led.h            pdcpat.h       signal.h          tlbflush.h
agp.h          compat_ucontext.h  hardware.h    linkage.h        perf.h         smp.h             topology.h
alternative.h  delay.h            hash.h        machdep.h        perf_event.h   socket.h          traps.h
asm-offsets.h  dma-mapping.h      hugetlb.h     mckinley.h       pgalloc.h      sparsemem.h       uaccess.h
asmregs.h      dma.h              ide.h         mmu.h            pgtable.h      special_insns.h   ucontext.h
assembly.h     dwarf.h            io.h          mmu_context.h    prefetch.h     spinlock.h        unaligned.h
atomic.h       eisa_bus.h         irq.h         mmzone.h         processor.h    spinlock_types.h  unistd.h
barrier.h      eisa_eeprom.h      irqflags.h    module.h         psw.h          string.h          unwind.h
bitops.h       elf.h              jump_label.h  page.h           ptrace.h       superio.h
bug.h          fb.h               kbdleds.h     parisc-device.h  ropes.h        switch_to.h
bugs.h         fixmap.h           kexec.h       parport.h        rt_sigframe.h  syscall.h
cache.h        floppy.h           kgdb.h        patch.h          runway.h       termios.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/parisc/include/asm$ cat .README
Lucky listing!
The next clue is in: /usr/share/xml/iso-codes
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/parisc/include/asm$ cd  /usr/share/xml/iso-codes
hacker@commands~an-epic-filesystem-quest:/usr/share/xml/iso-codes$ ls
LEAD           iso_3166-1.xml  iso_3166-3.xml  iso_3166_2.xml  iso_639-2.xml  iso_639-5.xml  iso_639_3.xml
iso_15924.xml  iso_3166-2.xml  iso_3166.xml    iso_4217.xml    iso_639-3.xml  iso_639.xml    iso_639_5.xml
hacker@commands~an-epic-filesystem-quest:/usr/share/xml/iso-codes$ cat LEAD
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{cob9KxR6L4VoB1xz1_GRpjvCuJi.dljM4QDLzgTN0czW}
```
