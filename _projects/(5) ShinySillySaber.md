---
name: ShinySillySaber
tools: [Arduino, Pure Data, Ableton Live]
image: /assets/img/MTF2012_2_square.png
description: Light Saber Wireless Midi Controller
external_url:
---

# ShinySillySaber

ShinySillySaber was a project developed during the Music Tech Fest 2012 in London. The hack was essentially a midi wireless controller for music and simultaneously a trigger of the light patterns of the saber.

{% include elements/figure.html image="/assets/img/MTF2012.jpg" caption="Hackers testing the prototype" %}

All teams were fed with different kinds of hardware from which a group of toy light sabers where available. Those consisted with of foldable saber equiped with led stripes which kept displaying random light patterns. Our idea was to sonify the typical gestures of the saber as well as use it as a midi controller for generating live music. We end up using an Arduino Xbee shield with the nano board which fitted nicely within the saber handle. The LEDs and an encoder for turning on/off the saber where hooked to the Arduino board. Then the Arduino was communicating with the remote computer, analyzing the saber movements and triggering sounds and generating some music trough Pure Data and Ableton Live.

{% include elements/video.html id="gCpKVYUNhBo"%}
