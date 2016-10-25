## Dealing With Demos

### Live Demos: Terminal Settings

* Use white background
  <br />or disable colorization
* Keep cursor in top half of terminal
  <br />Tmux, partial window, etc.
* Use muliple desktops to switch
* Avoid typos with command history
* Use tabs and name them
* Alternative: embedded terminal

Note:

Josh

If you're going to show code, or do a demo, in a terminal or
a text editor, you need to make some decisions for legible
contrast.  You have to make a choice between colorization of
your code and a dark background, for example.

Also, you really want to keep the action towards the top of
the screen, since some of your audience won't be able to see
the bottom of the screen.  You can do this with a part-screen
terminal window, or buy using split-screen in Tmux.

On Linux and OSX, make use of multiple desktops to switch
between your presentation and the demo/terminal, rather than
exiting the slides.  This spares your audience watching you
fiddle with the slide software.  And use command history
in the terminal to avoid typos.

Further, have a terminal tab, or a tmux window, for each
separate demo.  This keeps your command history for each
demo separate, and makes it easy for you to skip demos
if you're running short on time, or if they're not suitable
for the current audience.

Some slide software (Rails-based, mostly) also supports embedded terminals, which
can be a useful way to run a quick one-command demo inside
your slide preso.  In general this is awkward, though.
