# timefreak

**Timefreak** is a set of IPython notebooks that explore questions in time-frequency analysis, especially as it pertains to seismic geophysics.

Feedback, suggestions, and pull requests will be gratefully received. Fork and enjoy!

Timefreak was originally compiled for the *Latest developments in time-frequency analysis* post-convention workshop organized by Mirko van der Baan, Sergey Fomel, and Jean-Baptiste Tary at the SEG Annual Meeting in Denver, Colorado, on 30 October 2014.

The workshop was inspired by the paper by Tary, Herrera, Han, and van der Bann in JGR 2014, which reviewed several time-frequency representations against a set of 'benchmark' signals (see below). . 

## Notebooks

- **basics** &mdash; Some basic signals and their spectrums, illustrating some points about sampling, support, and windowing.
- **spectrograms** &mdash; Exploring `pyplot.specgram`, a basic STFT implementation in `matplotlib`. Reproduces the STFTs from Tary et al. 2014.
- **stft** &mdash; Since `pyplot.specgram` doesn't give you access to the innards of the STFT, and also doesn't have an inverse, here's a simple version complete with an inverse STFT. Also includes a demo of `PyTFD`, a module I found but haven't really tested yet.
- **fst** &mdash; The fast S-transform from the PyGFT package by workers at the University of Calgary. Some nice results, I think. Reproducing figures from Naghidzadeh & Innanen 2011.
- **cwt** &mdash; An unsuccessful test of `scipy.signal.cwt`, and a more successful go with Roger Fearick's `pycwt` module.
- **dwt** &mdash; A go at `pywt`, which turns out to be fairly low-level and not that easy to get a scalogram (let alone a spectrogram) from.

### Dev
Some of the notebooks are a bit (a lot) less developed, and therefore less useful.
- **dmd** &mdash; Dynamic mode decomposition.
- **emd** &mdash; Empirical mode decompsition. I can't get this working.  
- **mp** &mdash; Matching pursuit. Three possiblities. None of these are working.
- **audio** &mdash; Looking at some ways to produce and analyse audio signals with Python. I didn't get very far. I'd ignore it if I were you.
- **cepstrum** &mdash; Exploring cepstrums and wondering about time-time representations... Totally whimsical. You should probably ignore it.

## Signals

Timefreak includes the benchmark signals of van der Bann, Tary, et al. It's not clear how these are licensed, if at all:

- A toy example – a synthetic signal.
- A laughing voice.
- A volcano tectonic event, a gliding tremor (Redoubt Volcano on March 31, 2009; Hotovec et al. 2013).
- A microseismic event (Rolla hydraulic frack, 2011).
- A global earthquake signal (Tohoku 2011, Mw9).
- A seismic trace.

## To do

- Test `stft.ipynb` > `istft`
- Test `stft.ipynb` > `pytfd`
- `stft.ipynb` > Gabor uncertainty

## Requirements

Some of the notebooks can be run with the basic IPython stack, including Python 2.7, NumPy, SciPy, and so on. Some others depend on single-file modules that are included here. Still others depend on libraries that you must install. And some of those depend on other, non-Python libraries, such as FFTW. I ahve tried to document the requirements as they come up in the notebooks. 

For sure you will need [FFTW, version 3.3+](http://www.fftw.org), so you might as well just install it.

`fftw` needs [LAPACK](http://www.netlib.org/lapack). For OS X users, LAPACK is included with the system; Linux and Windows users will probably have to install a package.


## License
These notebooks, but not the 3rd party code snippets they may contain, are licensed under the Apache 2.0 license. See the file LICENSE.

THE NOTEBOOKS ARE PROVIDED "AS IS" WITHOUT WARRANTY OF MERCANTABILITY OR FITNESS FOR A PARTICULAR PURPOSE OR ANY OTHER WARRANTY, EXPRESS OR IMPLIED. IN NO EVENT SHALL AGILE GEOSCIENCE LTD OR MATT HALL BE LIABLE FOR ANY DIRECT OR CONSEQUENTIAL DAMAGES RESULTING FROM USE OF THE NOTEBOOKS. THE USER BEARS THE ENTIRE RISK FOR USE OF THE NOTEBOOKS.
