# ZeroWM
Super simple window manager written in Python

## New in version 1.0 (Spicy Salamander):

- Window borders
- Preference file
- Startup file
- Customizeable colours
- Passive event handler
- Transparency support
- Fixed Python3 compatibility
- Fixed some bugs and typos
- Fixed BadAccess bug

## Coming soon:

- Mouse cursor graphic support
- Window resizing 
- Window movement by mouse
- Tiling modes
- Info bar
- Mode support
- Redesigned logos and wallpapers

## Screenshots:

![Screenshot of ZeroWM](https://i.redd.it/i35szxp7o7wz.png)

## Dependencies:

- Feh (Wallpaper application)
- Python 2.7+/3.4+
- LXTerminal (This can be modified by editing the preference file)
- Rofi (This can be modified by editing the preference file)
- Midori (This can be modified by editing the preference file)
- Python-Xlib/Python3-Xlib
- Click
- Linux with Xorg installed


## Usage:
Just add: `python3 <PATH-TO-CODE>/ZeroWM.py` to your .Xinitrc and run `startx`
Alternatively, for testing, you can use Xephyr.

## Customization:
All availiable preferences can be modified by editing Preferences.py. Avaliable options:

### Border customization:

- Preferences.preferences.theme.border.borderSize: Size of border in pixels (DEFAULT = 2)
- Preferences.preferences.theme.border.activeColour: Colour of border when window is focused: (DEFAULT = #ffffff)
- Preferences.preferences.theme.border.inactiveColour: Colour of border when window isn't focused (DEFAULT = #000000)
- Preferences.preferences.applicationDe

### Application Defaults:

All application defaults can be modified by editing Preferences.preferences.applicationDefaults. They follow this syntax:

applicationType={name:"<name of command>", "command":["full path to command", "arg1", "arg2", "arg..."]}
  
For example, the terminal default might look like this:

terminal={"name":"LXTerminal", "command":["/usr/bin/lxterminal"]}

## Startup:

- Code may be placed in the Startup.py onStart() function to be executed at startup.
- Code may be placed in the Startup.py onStop() function to be executed apon a clean exit of the window manager.

## FAQ:

- Q: Does this use Wayland?
  A: No, it uses the Python X bindings via Python-Xlib
  
- Q: Have you thought about using Wayland?
  A: No, but I might look in to it.
  
- Q: How do I run this?
  A: See the `Usage` section above.
  
 - Q: Is it true that you're actually reptile and not a programmer?
   A: No. *slithers away*

## Known bugs:

- Closing some windows causes thousands of X errors that have no effect on the window manager, perhaps it might be possible to just suppress these since they don't actually cause anything bad to happen

- Some applications (Noteably, Doom) leave a black square when closing. I'm not sure what's causing this but I will look in to it

- Resizing window is borked. This kind of makes the WM a little useless, but don't worry, I'll get there in the end.

## Thanks to:

[/u/p4squale](https://reddit.com/u/p4squale) on Reddit for the inspiration and some help with the code.  
[Eberhard Grossgasteiger](https://www.pexels.com/u/eberhardgross/) on Pexels for the wallpaper.
