# What is new in FlexRouter 3.5

Timing, Transposing & Velocity to CC features

*Version 3.5 contains huge updates in timing feature that properly distributes timing across all channels, there is new transpose, note range and velocity to CC features, that enables lot more fun, also program number starts from 1 (not from 0) .*


## What is it?

FlexRouter is a highly customizable Kontakt 5 Multiscript from [Jason Tackaberry](https://github.com/jtackaberry/flexrouter) designed for managing and unifying keyswitches across instruments from many different developers.

![](https://dominiksvoboda.com/wp-content/uploads/2023/08/dominiksvoboda.com-snimek-obrazovky-2023-08-15-v-21.53.40.png)

Some features include:

* support for note, program change, or CC-based keyswitches
 * FlexRouter refers to all these MIDI events as "keyswitches" even though they're not all strictly "keys"
* arbitrary translation between notes, CCs, and program changes
 * one "keyswitch" input event can be translated to *multiple* configurable output events
* can route events to instruments on ports A-D (64 separate channels)
* multiple note-based keyswitches can be activated simultaneously (useful for e.g. layering articulations)
* one keyswitch note/CC/PC can trigger routing to multiple target channels
* note- and CC-based keyswitches can have configurable velocity/value ranges
* one instance of FlexRouter supports 16 rules
* each rule supports up to 128 independently configured keyswitches
* Optional anti-hanging for notes and sustain pedal when jumping between keyswitches
* Optional CC chasing per rule
* Timing feature
* Note Range feature
* Transposing feature
* Velocity to CC feature
* probably a few bugs :)


## How do I install it?

Just click on script.ksp file in github and click on copy raw text icon and paste to multiscript editor in NI Kontakt

## What kinds of things can I use it for?

Here are just a few random use-cases that can be solved using FlexRouter:

* Put each articulation patch on different channels (up to 64) and control with keyswitches
  from a single channel
* Route to different patches based on keyswitch velocity
* Assign different instruments on channels 1 through 16, each with multiple patches for articulations, and
  control each instrument independently
* Use UACC to control conventional note-keyswitched libraries
* Use UACC with Spitfire libraries, but cherry-pick certain articulations from
  other libraries on other channels
* Use standard notes on channel 16 to control Spitfire via UACC on channel 1

There's also a [walkthrough video](https://www.youtube.com/watch?v=FddWrEwaNmM) that shows how to implement some of these use-cases.
(Note, the video shows version 1, but all the examples still work with version 2.)


## How do I contribute or make my own customizations?

### Reporting bugs or pull request

Create an account on GitHub and [open an issue](https://github.com/jerayan/flexrouter/issues) or [pull request](https://github.com/jerayan/flexrouter/pulls) for improvement.


### Hacking code

First download and install [Sublime Text 3](http://www.sublimetext.com/3), and then download and install the [SublimeKSP](https://github.com/nojanath/SublimeKSP#installation) plugin for ST3.

While you're at it, visit [Nils Liberg's page for the original SublimeKSP](http://nilsliberg.se/ksp/) and click the donate button to buy Nils a coffee for his original work because there's no way I'd have avoided gouging out my eyes at the abomination that is KSP were it not for Nils' KSP extensions.

Clone the FlexRouter repository, and open the KSP scripts under src/ within ST3.

Use SublimeKSP to compile flexrouter.ksp (F5 by default -- see SublimeKSP's README.md for details) and paste the contents of the clipboard (which gets automagically populated by SublimeKSP) into Kontakt as per the installations steps above.

If you want to contribute changes back to FlexRouter, please use the usual GitHub workflow: fork this repository and send me a pull request.  Please don't be offended by scrutiny and nitpicking on any contributed code. :)
