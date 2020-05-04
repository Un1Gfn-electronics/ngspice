
reset gEDA/gschem/guile)
```bash
# rm -r /home/darren/.cache/guile
rm -r /home/darren/.gEDA
rm -r /home/darren/.config/gEDA
```

.sch -> .cir
```bash
gnetlist -v -p spice       -o - capacitor2.sch
gnetlist -v -p spice-sdb   -o - capacitor2.sch
```

.sch -> \*
```bash
gnetlist -V
gnetlist -v --list-backends

gnetlist -v -p partslist1  -o - capacitor2.sch
gnetlist -v -p partslist2  -o - capacitor2.sch
gnetlist -v -p partslist3  -o - capacitor2.sch

gnetlist -v -p verilog     -o - capacitor2.sch
```
