###### Files

|Source|Files|
|-|-|
|http://ngspice.sourceforge.net/ngspice-tutorial.html|01_sf_*|

###### Experiments

Cleanup
```bash
rm -r ngspice-31/
tar xf ngspice-31.tar.gz
```

Inverter
```
pushd /home/darren/ngspice/ngspice-31/examples/soi
ngspice inv_tr.sp
...
quit
popd
```

ngspice x gtkwave
<sup>[1](http://ngspice.sourceforge.net/docs/ngspice-html-manual/manual.xhtml#magicparlabel-19379)</sup>
<sup>[2](http://ngspice.sourceforge.net/docs/ngspice-html-manual/manual.xhtml#subsec_Edisplay__1)</sup>
<sup>[3](http://ngspice.sourceforge.net/docs/ngspice-html-manual/manual.xhtml#subsec_Running_example_C3)</sup>
```
pushd /home/darren/ngspice/ngspice-31/examples/xspice/
ngspice xspice_c3.cir
run
plot filt_in lpf_out
eprvcd filt_in >/tmp/ngspice.vcd
...
quit
gtkwave /tmp/ngspice.vcd
popd
```

###### References

[ngspice](http://ngspice.sourceforge.net/)
* [doc](http://ngspice.sourceforge.net/docs.html)
* [doc (online)](http://ngspice.sourceforge.net/docs/ngspice-html-manual/manual.xhtml)
* [doc (external) (BSIM)](http://ngspice.sourceforge.net/literature.html)
* [books](http://ngspice.sourceforge.net/books.html)

[BSIM](http://bsim.berkeley.edu/)
* [BSIM-SOI](http://bsim.berkeley.edu/models/bsimsoi/)

analog
* [Neso Academy](https://www.youtube.com/playlist?list=PLBlnK6fEyqRiw-GZRqfnlVIBz9dxrqHJS)
* [Caltech](https://www.youtube.com/playlist?list=PLc7Gz02Znph-c2-ssFpRrzYwbzplXfXUT)
* [GATE ACADEMY](https://www.youtube.com/playlist?list=PLgzsL8klq6DLhLOLOgEHsH4Li7zJhw6HT)

[pcb-rnd](http://repo.hu/projects/pcb-rnd/)
* [forum](https://www.eevblog.com/forum/geda/pcb-rnd/)
* [bridges](http://repo.hu/projects/pcb-rnd/user/09_appendix/bridges.svg)

###### Hidden

<details><summary>&nbsp;</summary>

```bash
pacman -Syu kicad kicad-library
rm -rf /home/darren/.config/kicad
```

KiCad/Eeschema
* [nspice x eeschema](http://ngspice.sourceforge.net/ngspice-eeschema.html)
* [cmos nand](https://github.com/bobc/kicad-simulation-examples)

</details>
