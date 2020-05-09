How does logic gates work
* [NOT](https://www.allaboutcircuits.com/textbook/digital/chpt-3/not-gate/)
* [NAND](https://www.allaboutcircuits.com/textbook/digital/chpt-3/ttl-nand-and-gates/)

[Line Driver, Open Collector and Totem Pole](https://knowledge.ni.com/KnowledgeArticleDetails?id=kA00Z0000019MXOSA2&l=en-US)

[TTL inverter and NAND gate](https://wiki.analog.com/university/courses/electronics/electronics-lab-27)

models
* [2N3904](https://www.onsemi.com/products/discretes-drivers/general-purpose-and-low-vcesat-transistors/2n3904)
* [SSM2212](https://www.analog.com/en/design-center/simulation-models/spice-models.html)
* [1N914](https://www.onsemi.com/products/discretes-drivers/diodes-rectifiers/small-signal-switching-diodes/1n914) ([1N914](https://my.centralsemi.com/product/partpage2.php?part=1N914))

[List of 7400-series integrated circuits](https://en.wikipedia.org/wiki/List_of_7400-series_integrated_circuits#Larger_footprints)

[Ti docs and modules (search w/ regex)](http://www.ti.com/logic-circuit/gate/products.html)
* [SN74LS00 ~ Quad 2-input positive-NAND gates](http://www.ti.com/product/SN74LS00/toolssoftware)

mixed
* [convert VCD to d_source](https://sourceforge.net/p/ngspice/discussion/ngspice-tips/thread/635bb14a/)
* [F-Si](https://wiki.f-si.org/images/4/42/Ngspice_FSiC2019.pdf#page=4)
* [ISOTEL](https://www.isotel.eu/index.html) [SPICE x Verilog x C/C++](https://www.isotel.eu/mixedsim/index.html) ([example](https://sourceforge.net/p/ngspice/discussion/133842/thread/bfb9dad0/#96e7))
* xspice
  * [pll](https://sourceforge.net/p/ngspice/ngspice/ci/master/tree/examples/xspice/pll/)
  * [howto](http://ngspice.sourceforge.net/xspicehowto.html)
  * [usage](http://ngspice.sourceforge.net/xspiceusage.html)
  * [MCUSim library](https://trac.mcusim.org/) ([GitHub](https://www.avrfreaks.net/forum/mcusim-open-source-simulator-microcontrollers))

[spice](http://bwrcs.eecs.berkeley.edu/Classes/IcBook/SPICE/)
* [doc](http://bwrcs.eecs.berkeley.edu/Classes/IcBook/SPICE/UserGuide/overview_fr.html)

[ngspice](http://ngspice.sourceforge.net/)
* [tutorial](http://ngspice.sourceforge.net/tutorials.html)
* [doc](http://ngspice.sourceforge.net/docs.html)
* [doc (xhtml)](http://ngspice.sourceforge.net/docs/ngspice-html-manual/manual.xhtml)
* [doc (external)](http://ngspice.sourceforge.net/literature.html)
* [books](http://ngspice.sourceforge.net/books.html)
* [LTwiki](http://ltwiki.org/index.php?title=C_Capacitor)
* [demo circuit](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator/lt-spice-demo-circuits.html)
* [working with other tools](http://ngspice.sourceforge.net/resources.html)

spice models
* https://www.diodes.com/design/tools/spice-models/
* https://www.onsemi.com/
* https://www.analog.com/
* http://espice.ugr.es/espice/src/modelos_subckt/
* [BSIM](http://bsim.berkeley.edu/) [BSIM-SOI](http://bsim.berkeley.edu/models/bsimsoi/)
* Diode
  * [all about circuits](https://www.allaboutcircuits.com/textbook/semiconductors/chpt-3/spice-models/)
  * [wikipedia category](https://en.wikipedia.org/wiki/Category:Diodes)
  * [1N400X](https://en.wikipedia.org/wiki/1N400x_general-purpose_diodes)
  * [1N34A](https://www.alldatasheet.com/view.jsp?Searchword=1N34A)
    * [eBay](https://www.ebay.com/sch/i.html?_nkw=1n34a)
    * [code](https://electronics.stackexchange.com/q/242660#comment530741_242660)
    * [jameco](https://www.jameco.com/webapp/wcs/stores/servlet/Product_10001_10001_35941_-1)

analog toturial
* [Neso Academy](https://www.youtube.com/playlist?list=PLBlnK6fEyqRiw-GZRqfnlVIBz9dxrqHJS)
* [Caltech](https://www.youtube.com/playlist?list=PLc7Gz02Znph-c2-ssFpRrzYwbzplXfXUT)
* [GATE ACADEMY](https://www.youtube.com/playlist?list=PLgzsL8klq6DLhLOLOgEHsH4Li7zJhw6HT)

[lepton-eda](https://github.com/lepton-eda/lepton-eda) and [pcb-rnd](http://repo.hu/projects/pcb-rnd/)
* [about pcb-rnd](https://www.eevblog.com/forum/geda/pcb-rnd/)
* [lepton vs pcb-rnd](https://www.eevblog.com/forum/geda/the-current-state-of-gedalepton-eda-and-what-this-means-for-pcb-rnd/)
* [working with other tools](http://repo.hu/projects/pcb-rnd/user/09_appendix/bridges.svg)

[bash ignoreeof](https://wiki.archlinux.org/index.php/Bash#Shell_exits_even_if_ignoreeof_set)
```bash
set -o ignoreeof
```

###### Hidden

<details><summary>&nbsp;</summary>

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

inverter w/ BSIM
```
pushd /home/darren/ngspice/ngspice-31/examples/soi
ngspice inv_tr.sp
...
quit
popd
```

```bash
pacman -Syu kicad kicad-library
rm -rf /home/darren/.config/kicad
```

KiCad/Eeschema
* [nspice x eeschema](http://ngspice.sourceforge.net/ngspice-eeschema.html)
* [cmos nand](https://github.com/bobc/kicad-simulation-examples)

</details>
