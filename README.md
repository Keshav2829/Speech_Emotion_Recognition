# Speech_Emotion_Recognition

Emotion detection is a challenging task, because emotions are subjective. There is no common consensus on how to measure or categorize them. We define a SER system as a collection of methodologies that process and classify speech signals to detect emotions embedded in them. Such a system can find use in a wide variety of application areas like interactive voice based-assistant or caller-agent conversation analysis. In this study we attempt to detect underlying emotions in recorded speech by analysing the acoustic features of the audio data of recordings.
There are three classes of features in a speech namely, the lexical features (the vocabulary used), the visual features (the expressions the speaker makes) and the acoustic features (sound properties like pitch, tone, jitter, etc.). The problem of speech emotion recognition can be solved by analysing one or more of these features. Choosing to follow the lexical features would require a transcript of the speech which would further require an additional step of text extraction from speech if one wants to predict emotions from real-time audio. Similarly, going forward with analysing visual features would require the excess to the video of the conversations which might not be feasible in every case while the analysis on the acoustic features can be done in real-time while the conversation is taking place as we’d just need the audio data for accomplishing our task.


# Dataset

The data used in this project was combined from five different data sources as mentioned below:
	1. TESS (Toronto Emotional Speech Set): 2 female speakers (young and old), 2800 audio files, random words were spoken in 7 different emotions.
	2. SAVEE (Surrey Audio-Visual Expressed Emotion): 4 male speakers, 480 audio files, same sentences were spoken in 7 different emotions.
RAVDESS: 2452 audio files, with 12 male speakers and 12 Female speakers, the lexical features (vocabulary) of the utterances are kept constant by speaking only 2 statements of equal lengths in 8 different emotions by all speakers.


# Features
  1. Spectra Centroids:-
		It indicates at which frequency in the energy of a spectrum is centered upon over in other words it indicates where the centre of mass for the sound is located. The size of vector will be equal to number of frames present in a signal.
	2. Spectral Rolloff:-
		It is a measure of shape of a signal it represents the frequency at which high frequency declined to zero.To obtain it we have to calculate the fraction of beans in the power spectrum where 85% of its power is at low frequency
	3. Zero crossing:- 
		A simple way of measuring the smoothness of a signal is to calculate the number of zero crossing within a segment of that signal a voice signal oscillates slowly whereas an unvoiced fricative can have (3000 zero crossings)
	4. Chroma Features:- (just for info)
		It is typically a 12 element feature vector indicating how much energy of each pitch class is present in signal. in short it provides a robust way to describe a similarity measure between music pieces.
	5. MFCC
	In sound processing, the mel-frequency cepstrum (MFC) is a representation of the short-term power spectrum of a sound, based on a linear cosine transform of a log power spectrum on a nonlinear mel scale of frequency.
	
	Mel-frequency cepstral coefficients (MFCCs) are coefficients that collectively make up an MFC.[1] They are derived from a type of cepstral representation of the audio clip (a nonlinear "spectrum-of-a-spectrum"). The difference between the cepstrum and the mel-frequency cepstrum is that in the MFC, the frequency bands are equally spaced on the mel scale, which approximates the human auditory system's response more closely than the linearly-spaced frequency bands used in the normal spectrum. This frequency warping can allow for better representation of sound, for example, in audio compression that might potentially reduce the transmission bandwidth and the storage requirements of audio signals.
	
	MFCCs are commonly derived as follows:
	
		○ Take the Fourier transform of (a windowed excerpt of) a signal.
		○ Map the powers of the spectrum obtained above onto the mel scale, using triangular overlapping windows or alternatively, cosine overlapping windows.
		○ Take the logs of the powers at each of the mel frequencies.
		○ Take the discrete cosine transform of the list of mel log powers, as if it were a signal.
		○ The MFCCs are the amplitudes of the resulting spectrum.
    
  6. Spectrogram:- (only for deep learning project)
A spectrogram is a visual way of representing the signal strength, or “loudness”, of a signal over time at various frequencies present in a particular waveform.  Not only can one see whether there is more or less energy at, for example, 2 Hz vs 10 Hz, but one can also see how energy levels vary over time.  In other sciences spectrograms are commonly used to display frequencies of sound waves produced by humans, machinery, animals, whales, jets, etc., as recorded by microphones.  In the seismic world, spectrograms are increasingly being used to look at frequency content of continuous signals recorded by individual or groups of seismometers to help distinguish and characterize different types of earthquakes or other vibrations in the earth.


