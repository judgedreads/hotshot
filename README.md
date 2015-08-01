#HotShot

Add a GTK+ tabbed interface to any application implementing XEmbed.

##Dependencies

- python3
- GTK+ >= 3.12
- pygobject (should match GTK+ version - using system package manager is
  recommended)
- X (obviously)
- python3-xlib (`pip3 install python3-xlib`)

##Usage

- put the hotshot executable somewhere in your `$PATH`
- pass the application name along with any options as arguments to
  hotshot e.g.
  `hotshot xterm -into`
  see `hotshot -h` for more information
- controls are (currently) only configurable by editing the source code,
  by default they are `Ctrl+Shift+t` for new tab and `Ctrl+Shift+{h,l}`
  to move back and forth among tabs

##Known Issues

- The application frequently segfaults on close. I intend to investigate
  further but it hasn't yet affected the application whilst running.
- There is some weird stuff happening with the focus of widgets in that
  the embedded looks like it isn't focussed even though key-press-events
  are still sent to it. I imagine it's just multiple widgets trying to
  compete for focus. If it bothers you, just clicking on the title bar
  seems to fit it (or pressing tab).

##Credits

Inspired by [tabbed](http://tools.suckless.org/tabbed/)
