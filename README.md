#### Keeb config
Steps to build conf and flashing microcontrollers. Assumes standard qmk install. Sofle used as example but other keebs would work as well.

##### Setting up the environment
qmk config user.keyboard=splitkb/aurora/sofle_v2/rev1
qmk config user.keymap=windrammer

##### Linking repos
In the repo in the directory of the keyboard in the qmk dir, (e.g. ~/qmk_firmware/keyboards/splitkb/aurora/sofle_v2/keymaps/windrammer) run
`ln -s ~/git/keeb-conf/sofle/windrammer windrammer`

##### Compiling
When all changes are done to keymap.c, go to ~/qmk_firmware/keyboards/splitkb/aurora/sofle_v2/keymaps, run:
`qmk compile -e CONVERT_TO=liatris -km keymap.c`

Copy new file from ~/qmk_firmware to ~/git/keeb-conf/sofle/windrammer, should have a name like the following, note the .uf2 ``
`splitkb_aurora_sofle_v2_rev1_windrammer_liatris.uf2`

##### Flashing the controller
Double click the reset button on the keyboard and copy the new file to the movable device that comes up and it will reboot automatically when done and the keyboard is configured.


