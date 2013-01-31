SpectrumAnalyzer
================

Sound data utility that exports json.

Use it: http://positlabs.com/files/code/spectrum-analyzer/

Instead of analyzing a sound at runtime (which isn't possible in all cases anyway), we can export the data beforehand. It frees up cpu power for awesome vizualizers and stuff!

This is a work in progress. Still haven't actually used the data for anything, so I might add a couple of parsing features or change how the keys are assigned.

How to
================

1. Decide what type of data you want to use, then check the related check-boxes.

2. Load an mp3 file by clicking the 'load sound' button.

3. Play the song and let it run through to the end.

4. Pressing the 'copy data' buttons will copy a json object to your clipboard.


Spectrum data structure
================
Keys for the data are the timestamp of when the sample was taken. Left / right are channels with 256 normalized values. If FFT is active, these values are frequencies - if not, they are sound-wave data.
		
{millis:
	{"left":[256], "right":[256]}
}


Peak data structure
================
Same structure, but only one value per channel.

{millis:
	{"left":[x], "right":[x]}
}





