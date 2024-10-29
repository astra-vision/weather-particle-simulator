# Fast Reactive Control for Illumination Through Rain and Snow
This repo is for releasing **x64** binaries for Windows and Linux.  
The work (de Charette et al., ICCP 2012) belongs to Carnegie Mellon University and is distributed under MIT licensing term. Please, also refer to the [official project page](https://www.cs.cmu.edu/smartheadlight/index2.html).

**News 2024-10-29**: Following multiple requests, we have changed to MIT license and will also share code in some time.

## Paper 
[Fast Reactive Control for Illumination Through Rain and Snow](https://www.cs.cmu.edu/smartheadlight/index2.html) \
[Raoul de Charette](https://team.inria.fr/rits/membres/raoul-de-charette/), [Robert Tamburo](https://www.ri.cmu.edu/ri-people/robert-joseph-tamburo/), [Peter C. Barnum](https://scholar.google.com/citations?user=y_yzS-AAAAAJ&hl=en), [Anthony Rowe](https://users.ece.cmu.edu/~agr/), [Takeo Kanade](https://www.ri.cmu.edu/ri-faculty/takeo-kanade/), [Srinivasa Narasimhan](http://www.cs.cmu.edu/~srinivas/)  
Carnegie Mellon University, ICCP 2012 (Winner of the **Best Paper Honorable Mention Award**)

If you find our work useful, please cite:
```
@inproceedings{de2012fast,
  title={Fast reactive control for illumination through rain and snow},
  author={de Charette, Raoul and Tamburo, Robert and Barnum, Peter C and Rowe, Anthony and Kanade, Takeo and Narasimhan, Srinivasa G},
  booktitle={International Conference on Computational Photography (ICCP)},
  year={2012}
}
```


## Requirements
The following binaries are required to run the simulator:
* Open Scene Graph 3.4.1
* Boost library 1.62.0
* OpenCV 3.2.0

While this may work with other versions, tests were only conducted with the versions listed.

### Windows (x64)
On Windows, we recommend installing the required dependencies following:
* For Open Scene Graph **3.4.1**, build sources OR download binaries from [this official link](https://objexx.com/OpenSceneGraph/OpenSceneGraph-3.4.1-VC2017-64-Release.7z) (refer to [OSG page](https://objexx.com/OpenSceneGraph.html) for broken link)
* For OpenCV **3.2.0**, build sources OR download vc14 x64 binaries from [this official link](https://github.com/opencv/opencv/releases/tag/3.2.0) (refer to [OpenCV page](https://opencv.org/releases/) for broken link)
* **\[optional\]** Boost library **1.62.0** shall not be required as it is statically linked. But, if any mumbo jambo occurs, try building boost sources OR download vc14 x64 binaries from [this official link](https://sourceforge.net/projects/boost/files/boost-binaries/1.62.0/) (refer to [Boost page](https://www.boost.org/users/download/) for broken link)


### Linux (x64)
On Ubuntu, we recommend installing the required dependencies following these guides:  
* For Open Scene Graph **3.4.1**, follow [this page](https://vicrucann.github.io/tutorials/osg-linux-quick-install/)  **(!) Careful to use said version**  
* For Boost library **1.62.0**, follow [this page](https://stackoverflow.com/a/41272796/2738304) **(!) Careful to modify script to use said version** 
* For OpenCV **3.2.0**, follow section ''Installing OpenCV from the Source'' from [this page](https://linuxize.com/post/how-to-install-opencv-on-ubuntu-18-04/)  (if you hit ffmpeg compile error apply [this fix](https://stackoverflow.com/questions/46884682/error-in-building-opencv-with-ffmpeg)) **(!) Update code to use said version**  

## Running the simulator
To test all dependencies are correctly installed, just run:
* Linux (Ubuntu 20.04, Focal Fossa): ``cd lin_x64; ./AHLSimulation``  
* Linux (Ubuntu 18.04, Bionic Beaver): ``cd lin_x64; ./AHLSimulation_bionic``  ⚠️ For [rain rendering](https://github.com/astra-vision/rain-rendering/) to use this Bionic binary, you must change "AHLSimulation" to "AHLSimulation_bionic" in [this line](https://github.com/astra-vision/rain-rendering/blob/9e994b0cd7e5e210189821345f6655b21c79ca48/tools/simulation.py#L286).  (thanks to Eran Kishon for providing these binaries)
* Windows: ``cd win_x64 & AHLSimulation.exe``

If command fails, resolve missing dependencies.  
If command succeeds, just exit the simulator by entering ``0`` and enter.

## License
This data is property of Carnegie Mellon University and originates from (de Charette et al., 2012)
https://www.cs.cmu.edu/~ILIM/projects/IL/smartHeadlight/index2.html

Binaries and code are released under MIT License
