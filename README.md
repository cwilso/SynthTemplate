# Synth Template

This is a template for building synthesizers built on the [Web Audio API](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html).  It is intended to build polyphonic synthesizers (although it can be easily adapted - monophonic is actually a bit easier).

This uses my [Web MIDI Polyfill](https://github.com/cwilso/WebMIDIAPIShim) to add MIDI support via the [Web MIDI API](https://dvcs.w3.org/hg/audio/raw-file/tip/midi/specification.html) - in fact, I partly wrote this as a test case for the polyfill and the MIDI API itself, so if you have a MIDI keyboard attached, check it out.  The polyfill uses Java to access the MIDI device, so if you're wondering why Java is loading, that's why.  It may take a few seconds for MIDI to become active - the library takes a while to load - but when the ring turns gray (instead of blue), it's ready.  If you have a native implementation of the Web MIDI API in your browser, the polyfill shouldn't load - but at the time of this writing, there are no such implementations.

This incorporates the [PointerEvents polyfill](https://github.com/toolkitchen/PointerEvents) for pointer events, rather than using mouse events directly, in order to work well on touch screens.

Check it out, feel free to fork, submit pull requests, etc.

-Chris