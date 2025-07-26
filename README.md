# Framework 12 Cyberdeck Mode

Tools for using the Framework 12 2-in-1 laptop in an unusual configuration:
with the screen folded around the back, but flipped over with the keyboard on top and the built-in screen disabled.

This is designed for use with AR glasses like those from XREAL as the sole display, in the style of a console cowboy.

## Current state

It gets the job done.

Right now, this is a bash script that uses framework_tool and kscreen-doctor.
Eventually, this will be a Rust and Kirigami app with GUI and advanced features like automatic triggers.


## Support

This will work for Framework 12 only. It uses Framework embedded controller
commands to change the behavior when the screen is rotated.

Currenty, it also only works for KDE Plasma due to using kscreen-doctor to disable the built-in display, but that will change in the future.

## Requirements

Depends on the framework_tool cli from https://github.com/FrameworkComputer/framework-system

* Download the built cli tool from [an action run](https://github.com/FrameworkComputer/framework-system/actions?query=branch%3Amain)
* Unpack it and make it executable `chmod +x framework_tool`
* Place in a path folder, e.g. `sudo cp framework_tool /usr/local/bin/`

## Installation

* Download `bin/cyberdeck`
* Place in a path folder, e.g. `sudo cp cyberdeck /usr/local/bin/`

## Use

* Enable cyberdeck mode with `cyberdeck on`
* Return to normal operation with `cyberdeck off`

Notes: 

The command will prompt for sudo password in order to
execute the framework_tools commands

Consider binding `cyberdeck off` to a keyboard shorcut
(System settings -> keyboard -> shortcuts)
in case you
left cyberdeck mode on but don't have your glasses handy, as the
laptop screen will be disabled.
