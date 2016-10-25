## Dealing With Demos

### Prepping demos

Make sure your demo is drilled and repeatable:

* Scripting
* VMs or Containers

Also:

* Be unambitions
* Test your actual hardware
* Don't expect internet
* Never do "cascading" demos

Note:

Josh

There is one and only one way to do successful demos:
drill, drill, drill.  Before you ever present a demo
in front of an audience, make sure you have run it at
least 3 times, and preferbly 5 to 10.  

Often the first
run of your demo will leave behind state which will mess
up further runs.  To avoid this, use automated scripting,
or better VMs or Containers which can be reset to a starting
state.

If there's a second rule to good demos, it's "be unambitious".
Don't demo something which is pushing the limits of what
your software can do, beause that's guaranteed to fail in
front of an audience.  Also, test the demo under the
circumstances in which you'll present it: on your laptop,
with the preso software running, and no internet connection.

Also, stepwise demos where each step requires the 
prior step to have worked are very risky; inevitably
step #1 or #2 fails.  