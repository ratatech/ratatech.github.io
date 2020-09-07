---
name: Talkbox
tools: [Analog Electronics]
image: /assets\img\talkbox_pcb_top_square.png
description: Talkbox sound effect
external_url:
---

# Talkbox

The idea of building the Talkbox came as a request from my friend Aleix Bou. I knew the sound and I've seen vintage footage of people using this weird sound effect where people talks and sings through a tube as this one by Stevie Wonder:

{% include elements/video.html id="PnR19INlXV8" %}

I always believed that this particular sound effect was some sort of vocoder where the sound is picked up directly at the mouth thought the tube. After some quick research I realized that the Talkbox it's much simpler than the Vocoder and actually works the inverse direction. The basic idea is just to feed the sound to the mouth, replacing the vocal cords as sound generator and shape the tube's incoming sound with the mouth. Some basic description of how the talkbox works and many more related resources can be found at [GFWORKS](https://www.gfworks.jp/talkbox/index.html).

## Compression Driver and PA

Looking at similar DIY projects I found the [work](https://www.instructables.com/id/DIY-Talkbox/) by [Mosivers](https://www.instructables.com/member/mosivers/) a good start point since he used the [Monacor KU-516](https://www.monacor.com/products/pa-technology/speakers-/horn-speakers/low-impedance--/ku-516/) compression driver in combination with a small integrated PA. The Monacor KU-516 seems to be a good choice for a replacement of the old and discontinued Electro Voice “1823M” and “1824M” Compression Drivers. It is recommended also by the Japanese experts of [GFWORKS](https://www.gfworks.jp/talkbox/compression_driver.html). Ideally, the driver should cover the vocal frequency range, which is not that easy when talking about small speakers and compression drivers. The Monacor KU-516 provides still a relatively wide bandwidth covering a range of	160-6500 Hz. The [Kemo M033N PA](https://www.kemo-electronic.de/en/Light-Sound/Amplifier-Splitter/Modules/M033N-Amplifier-18-W-universal.php) drives an output power of 18W for a 4Ω impedance and a supply of 20V. The power supply chosen for the project is 12V and the Monacor KU-516 impedance is of 16Ω and Power rating (RMS) of 50W so technically it will be under amplified. Still, given the application, considering than the compression driver should go directly into a person's mouth, we don't need to reach very high levels. A few breadboard prototype tests revealed how the selected PA provides enough/safe amplification.

## Project design

Technically, with the PA, the compression driver and a tube, the Talkbox cloud be already assembled and finished. But in order to have a more complete unit, I decided to add two more sections. First a preamp, because the input level could vary substantially. The keyboard seems to be the more popular instrument to use with the Talkbox. But other instruments/sound sources like a guitar, smartphone or a computer could potentially be used as well. So it could come handy to have this extra input boost for a more flexible input. Secondly, a tone control section. This might be less of a requirement but a wish feature, but many commercial Talkbox sound effects out there include one and I found it a very basic but effective way of shape the timber of the signal.



{% include elements/figure.html image="/assets/img/talkbox_schematic.png"%}
{% include elements/figure.html image="/assets/img/talkbox_tone_control_freq_response.png"%}
