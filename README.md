#! /bin/sh

pgrep -x sxhkd > /dev/null || sxhkd &

bspc monitor -d I II III IV V VI VII VIII IX X

bspc config border_width         3
bspc config window_gap          12

bspc config split_ratio          0.52
bspc config borderless_monocle   true
bspc config gapless_monocle      true

bspc rule -a Gimp desktop='^8' state=floating follow=on
bspc rule -a Chromium desktop='^2'
bspc rule -a mplayer2 state=floating
bspc rule -a Kupfer.py focus=on
bspc rule -a Screenkey manage=off
feh --bg-fill /home/ghostx/Descargas/wallpapers/11.jpg
xsetroot -cursor_name left_ptr &
wmname LG3D &
~/.config/polybar/./launch.sh
bspc config focus_follows_pointer true
bspc config border_width 0
picom --experimental-backends &
