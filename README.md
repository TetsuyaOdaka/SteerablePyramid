# Steerable Pyramid
Python3 Implementation of steerable pyramid.

This is based on the article bellow.  

[The Heeger-Bergen Pyramid-Based Texture Synthesis Algorithm, Briand,T. et al. (2014)](http://www.ipol.im/pub/art/2014/79/)

According to this article, this is a "real version" of steerable pyramid which is used in Portilla and Simoncelli(2000).  

[Parametric Texture Model Based on Joint Statistics of Complex Wavelet Coefficient, Portilla, J. and Simoncelli, E.(2000) ](http://www.cns.nyu.edu/pub/lcv/portilla99.pdf)  
  
  
    
    
 ## Results
 - Depth : 4
 - Orientation : 4 (0, pi/4, pi/2, 3*pi/4)
 
 ### Original Image
<img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/saucer-mono256.png" width="256" alt="saucer">

 ### Pyramid Images
 #### band frequency 
<img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/img-layer0-lb0.png" alt="steerable pyramid"> <img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/img-layer0-lb1.png" alt="steerable pyramid"> <img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/img-layer0-lb2.png" alt="steerable pyramid"> <img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/img-layer0-lb3.png" alt="steerable pyramid">
 
<img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/img-layer1-lb0.png" alt="steerable pyramid"> <img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/img-layer1-lb1.png" alt="steerable pyramid"> <img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/img-layer1-lb2.png" alt="steerable pyramid"> <img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/img-layer1-lb3.png" alt="steerable pyramid">
 
<img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/img-layer2-lb0.png" alt="steerable pyramid"> <img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/img-layer2-lb1.png" alt="steerable pyramid">&nbsp;<img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/img-layer2-lb2.png" alt="steerable pyramid">&nbsp;<img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/img-layer2-lb3.png" alt="steerable pyramid">
 
<img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/img-layer3-lb0.png" alt="steerable pyramid"> <img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/img-layer3-lb1.png" alt="steerable pyramid"> <img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/img-layer3-lb2.png" alt="steerable pyramid"> <img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/img-layer3-lb3.png" alt="steerable pyramid">
  
#### low frequency residual  
<img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/img-residual-layer3.png" alt="steerable pyramid">

#### high frequency residual  
<img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/img-h0.png" alt="steerable pyramid">  


### Reconstructed Images
<img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/img-recon-full.png" alt="steerable pyramid">  


### Images of Filters (Fourier Domain)
#### First Highpass Filter (H0 in Portilla and Simoncelli)
<img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/fil_highpass0.png" alt="filter">

#### First Lowpass Filter (L0 in Portilla and Simoncelli)
<img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/fil_lowpass0.png" alt="filter">

#### Bandpass Filters (B*L in Portilla and Simoncelli)
<img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/fil_lo-bandpass0-layer0.png" alt="filter"> <img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/fil_lo-bandpass1-layer0.png" alt="filter"> <img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/fil_lo-bandpass2-layer0.png" alt="filter"> <img src="https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/out/fil_lo-bandpass3-layer0.png" alt="filter">  


## Usage 
### Environment
- python3.5 (3.0+)
- GPU is not used.

### Execution
- create 'out' directory. 
- `python create_collapse_pyramid.py -i saucer-mono256.png -x 256 -y 256`,  if you want to know details about parameters, see [source code](https://github.com/TetsuyaOdaka/SteerablePyramid/blob/master/create_collapse_pyramid.py)  
  
  
## References
- [The Heeger-Bergen Pyramid-Based Texture Synthesis Algorithm, Briend, T. et al.(2014)](http://www.ipol.im/pub/art/2014/79/)
- [Parametric Texture Model Based on Joint Statistics of Complex Wavelet Coefficient, Portilla, J. and Simoncelli, E.(2000)](http://www.cns.nyu.edu/pub/lcv/portilla99.pdf)
- [The Steerable Pyramid:A Flexible Architecture For Multi-Scale Derivative Computation, Simoncelli,E. and Freeman, W.(1995)](http://www.cns.nyu.edu/pub/eero/simoncelli95b.pdf)
- [A Filter Design Technique For Steerable Pyramid Image Transform, Karasaridis, A. and Simoncelli,E.(1996)](https://pdfs.semanticscholar.org/625e/ec8262570a3d62a2f252c151ef14e2be9b5d.pdf)
- [Design and Use of Steerable Filters, Freeman,W. and Adelson,E.(1991)](http://people.csail.mit.edu/billf/publications/Design_and_Use_of_Steerable_Filters.pdf)
