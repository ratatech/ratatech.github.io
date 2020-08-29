---
name: Dark Noise
tools: [Analog Electronics, Arduino]
image: /assets/img/RatatechIsolated.png
description: Light sensible analog synthesizer
external_url:
---

# Dark Noise

Inspired and composed by different traditional modules, Dark Noise is a simple monophonic synthesizer with only one peculiarity, light sensibility. Each of the modules is connected between them directly in the circuit, but it has some of the modules inputs/outputs allowing specific patching trough external jacks. Moreover it has a midi input that provides control the synthesizer with any MIDI instrument, controller, computer…

{% include elements/figure.html image="/assets/img/RatatechIsolated.png"%}

## VCO, LFO and VCA

These modules have been adapted from Ray Wilson’s classic Sound-Lab Mini-Synth. The oscillator is modified to be controlled with a LDR (light dependent resistor). This allows control the frequency of the VCO. The LDR works by decreasing his resistance with the incident intensity of light. Increasing and decreasing the intensity of light makes change the voltage level introduced at the oscillator, what makes change the frequency.

## ADSR and VCF

The ADSR has been adapted from René Schmitz’s envelope generator. It is a simple circuit that allows to control the traditional parameters attack, decay, sustain and release.

The Filter is based on Ken Stone’s Synthacon VCF that is a module inspired the awesome Steiner-Parker Synthacon VCF. It has three modes LP, BP and HP, and it can be controlled via the LDR like the VCO. In this case the light controls the cut-off frequency.

{% include elements/figure.html image="/assets/img/RatatechIsolated2.png"%}

## MIDI2CV

The MIDI control module is based on the Collin Cunningam’s MidiVox shield for Arduino. This is a great shield that allows Arduino to be converted in a programmable synthesizer, although in this case it acts only as an interface that converts the digital signals from the incoming MIDI device to analog CV and Gate signals.

## Sound samples

<iframe frameborder="0" scrolling="no" src="https://freesound.org/embed/sound/iframe/148781/simple/large/" width="920" height="245"></iframe>
<iframe frameborder="0" scrolling="no" src="https://freesound.org/embed/sound/iframe/148782/simple/large/" width="920" height="245"></iframe>
