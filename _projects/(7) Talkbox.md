---
name: Talkbox
tools: [Analog Electronics]
image: /assets\img\talkbox_pcb_top_square.png
description: Talkbox sound effect
external_url:
---

# Talkbox

The idea of building the Talkbox came as a request from my friend [Aleix Bou](https://twitter.com/AleixBou). I knew the sound and I've seen vintage footage of people using this weird sound effect where people talks and sings through a tube. Some cool examples can be found by Stevie Wonder or more recently by Byron Chambers aka "Mr. Talkbox" as in Bruno Mars 24K Magic intro. The appearance of Roger Troutman doing some demonstration on TV is one of my favorites.

{% include elements/video.html id="L_CBZkd2tGE" %}

I always believed that this particular sound effect was some sort of vocoder where the sound is picked up directly at the mouth thought the tube. After some quick research I realized that the Talkbox it's much simpler than the Vocoder and actually works the inverse direction. The basic idea is just to feed the sound to the mouth, replacing the vocal cords as sound generator and shape the tube's incoming sound with the mouth. Some basic description of how the talkbox works and many more related resources can be found at [GFWORKS](https://www.gfworks.jp/talkbox/index.html).



#### Compression Driver and PA

Looking at similar DIY projects I found the [work](https://www.instructables.com/id/DIY-Talkbox/) by [Mosivers](https://www.instructables.com/member/mosivers/) a good start point since he used the [Monacor KU-516](https://www.monacor.com/products/pa-technology/speakers-/horn-speakers/low-impedance--/ku-516/) compression driver in combination with a small integrated PA. The Monacor KU-516 seems to be a good choice for a replacement of the old and discontinued Electro Voice “1823M” and “1824M” Compression Drivers. It is recommended also by the Japanese experts of [GFWORKS](https://www.gfworks.jp/talkbox/compression_driver.html). Ideally, the driver should cover the vocal frequency range, which is not that easy when talking about small speakers and compression drivers. The Monacor KU-516 provides still a relatively wide bandwidth covering a range of	160-6500 Hz. The [Kemo M033N PA](https://www.kemo-electronic.de/en/Light-Sound/Amplifier-Splitter/Modules/M033N-Amplifier-18-W-universal.php) drives an output power of 18W for a 4Ω impedance and a supply of 20V. The power supply chosen for the project is 12V and the Monacor KU-516 impedance is of 16Ω and Power rating (RMS) of 50W so technically it will be under amplified. Still, given the application, considering than the compression driver should go directly into a person's mouth, we don't need to reach very high levels. A few breadboard prototype tests revealed how the selected PA provides enough/safe amplification.

#### Project design

Technically, with the PA, the compression driver and a tube, the Talkbox cloud be already assembled and finished. But in order to have a more complete unit, I decided to add two more sections. First a preamp, because the input level could vary substantially. The keyboard seems to be the more popular instrument to use with the Talkbox. But other instruments/sound sources like a guitar, smartphone or a computer could potentially be used as well. So it could come handy to have this extra input boost for a more flexible input. Secondly, a tone control section. This might be less of a requirement but a wish feature, but many commercial Talkbox sound effects out there include one and I found it a very basic but effective way of shape the timber of the signal. Still the main idea of this project was just to do a very simple design reusing available well-knowns designs for the different sub-circuits.

#### Preamplifier and Tone Control

There is different opinions out there about the placement of the preamps and tone control stages within the audio chain. It seems to depend in quite some factors and really depending on the specific application. Some argue that placing the tone control before the gain stage could sound a bit more noise while the inverse configuration can't work perfectly also at certain frequency ranges. I won't go into this discussion and for the sake of simplicity I decided to just place them with the pre-amp just before the tone control circuit.

Starting with the tone control, I selected the design of the guys of [Electrosmash](https://www.electrosmash.com/big-muff-pi-analysis) where they adapted the full Big Muff Pi guitar pedal circuit. I liked this circuit because of its effectivity and simplicity as they mention. One pot just to control a RC low-pass/CR high-pass filtering network.

For the preamplifier I just went for the non-inverting amplifier configuration using the popular TL072 op-amp. I set the input/output resistor ratio gain stage initially to boost the input signal by 10dB gain. Still, as the tone control section has as about 7-8dB loss, I added +10dB to the gain stage. So while the intermediate gain (a the input of the tone control circuit) is +20dB, this becomes about 12dB gain at the tone control output.

To verify and fine tune some of the component values, I simulated this part of the project in LTSPICE. Se below the schematic and frequency response (with fixed gain) when sweeping the tone control potentiometer. We can clearly see the low-pass/high-pass behavior which corresponds to the left and right-most position of the potentiometer respectively. While ideally the flattest response should correspond to the exact middle position of the potentiometer we can see how this is practically not achieved and normally the flattest response should be around the middle plus slight to the right rotation.

{% include elements/figure.html image="/assets/img/talkbox_ltspice_sim.png"%}
{% include elements/figure.html image="/assets/img/talkbox_tone_control_freq_response.png"%}




{% include elements/figure.html image="/assets/img/talkbox_schematic.png"%}

{% capture carousel_images_extra %}
/assets/img/P1080021.jpg
/assets/img/P1080020.jpg
/assets/img/P1080026.jpg
{% endcapture %}
{% include elements/carousel_extra.html %}

{% capture carousel_images %}
/assets/img/20200705_183042.jpg
/assets/img/20200705_183225.jpg
/assets/img/20200705_183852.jpg
/assets/img/20200705_184126.jpg
/assets/img/20200705_204743.jpg
/assets/img/20200705_210150.jpg
{% endcapture %}
{% include elements/carousel.html %}
