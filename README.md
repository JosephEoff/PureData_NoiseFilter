# PureData_NoiseFilter
This is a PureData patch to provide a noise filter for audio signals.

NoiseFilter.pd implements the noise reduction

NoiseLevelDetector.pd uses a novel method of detecting constant sound levels and forms the basis of the NoiseFilter.

BandLimitedNoiseFilter.pd is a noise filter with a bandpass filter in front of it.

MultibandNoiseFilter.pd uses a number of BandLimitedNoiseFilter to cover the audio range from 40Hz to 22000 Hz and demonstrates the use of the BandlimitedNoiseFilter

Test.pd is a complete patch to process audio.  It listens on the microphone input and sends the filtered audio back out through the line out jack of the computer.

This filter is basically a noise gate that doesn't need a lower level.  The only needed input is how much to attenuate the noise.  A typical noise gate requires that you set a lower level below which the gate is muted.  This level is absolute and must bechanged manually.  The NoiseFilter presented here automatically detects the current noise level and adapt automatically.  It attempts to maintain the set level of noise attenutation without user intervention.
