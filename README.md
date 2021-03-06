# juce-linux-patches
Repository of JUCE patches for Linux functionality not available in upstream

- `Projucer-resave-without-X11.patch`
  
  This allows to run the Projucer command line and resave projects, in build environments which cannot depend on having the X11 server running.

- `lxvst.patch`

    This allows to compile LinuxVST in one of the later versions of JUCE, not requiring to manually import any proprietary code.

    To make this patch work, you should copy the following GPL-licensed file from JUCE 5.3.2 into the newer JUCE version:
`modules/juce_audio_processors/format_types/juce_VSTInterface.h`

## Usage notes

If you are not familiar with use of patches, this is how to proceed.

Pre-requisite: a UNIX-style environment with the `patch(1)` command

Place yourself in the JUCE work folder, using `cd` commands.
Apply a patch using this command:

`patch -p1 -i juce-5.x.x-foo.patch`

If you would to try if the patch works first without applying, because your target JUCE version is different for instance, pass the option `--dry-run`.

## Upstream fixes

**Importance: Major**

- JUCE 5.4.4

This fixes a case of UI not opening at all, or not responding to events.
https://github.com/WeAreROLI/JUCE/commit/164aac7efa22123e76468fd62ca289fa533f8934
