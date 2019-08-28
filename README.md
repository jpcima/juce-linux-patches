# juce-linux-patches
Repository of JUCE patches for Linux functionality not available in upstream

- `Projucer-resave-without-X11.patch`
  
  This allows to run the Projucer command line and resave projects, in build environments which cannot depend on having the X11 server running.

## Upstream fixes

**Importance: Major**

- JUCE 5.4.4

This fixes a case of UI not opening at all, or not responding to events.
https://github.com/WeAreROLI/JUCE/commit/164aac7efa22123e76468fd62ca289fa533f8934
