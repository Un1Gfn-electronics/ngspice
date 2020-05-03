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

http://ngspice.sourceforge.net/ngspice-tutorial.html
```
cd /home/darren/ngspice/ngspice.sourceforge.net_ngspice-tutorial.html
ngspice vdiv.cir
ngspice capacitor.cir
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

[Ngspice](http://ngspice.sourceforge.net/)
* [doc](http://ngspice.sourceforge.net/docs.html)
* [doc (online)](http://ngspice.sourceforge.net/docs/ngspice-html-manual/manual.xhtml)
* [doc (external) (BSIM)](http://ngspice.sourceforge.net/literature.html)
* [books](http://ngspice.sourceforge.net/books.html)
* [LTwiki](http://ltwiki.org/index.php?title=C_Capacitor)
* [demo circuit](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator/lt-spice-demo-circuits.html)
* model library
  * [diodes.com](https://www.diodes.com/design/tools/spice-models/)

Diode
* [all about circuits](https://www.allaboutcircuits.com/textbook/semiconductors/chpt-3/spice-models/)
* [wikipedia category](https://en.wikipedia.org/wiki/Category:Diodes)
* [1N400X](https://en.wikipedia.org/wiki/1N400x_general-purpose_diodes)
* [1N34A](https://www.alldatasheet.com/view.jsp?Searchword=1N34A)
  * [eBay](https://www.ebay.com/sch/i.html?_nkw=1n34a)
  * [code](https://electronics.stackexchange.com/q/242660#comment530741_242660)
  * [jameco](https://www.jameco.com/webapp/wcs/stores/servlet/Product_10001_10001_35941_-1)

[BSIM](http://bsim.berkeley.edu/)
* [BSIM-SOI](http://bsim.berkeley.edu/models/bsimsoi/)

Analog
* [Neso Academy](https://www.youtube.com/playlist?list=PLBlnK6fEyqRiw-GZRqfnlVIBz9dxrqHJS)
* [Caltech](https://www.youtube.com/playlist?list=PLc7Gz02Znph-c2-ssFpRrzYwbzplXfXUT)
* [GATE ACADEMY](https://www.youtube.com/playlist?list=PLgzsL8klq6DLhLOLOgEHsH4Li7zJhw6HT)

Mixed
* [F-Si](https://wiki.f-si.org/images/4/42/Ngspice_FSiC2019.pdf#page=4)
* [xspice pll](https://sourceforge.net/p/ngspice/ngspice/ci/master/tree/examples/xspice/pll/)

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
