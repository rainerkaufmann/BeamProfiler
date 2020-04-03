## Low-cost beam profiler (WIP)
by Julian Falkenhayn & Rainer Kaufmann

Knowing the exact diameter and profile of a laser beam is highly beneficial for a wide range of (bio-)optical applications; e.g. determining the power distribution of your laser spot to avoid radiation damage on your sample or optical elements. Unluckily, commercial beam profilers (either camera based or scanning slit / knife-edge devices) usually cost several k EUR. Consequently, several research groups have created designs for low-cost beam profiler.
<br>
Here, we present our approach to a low-cost beam profiler, which utilizes a webcam for the profile recording and is designed for collimated laser beams with large diameters. The setup is built of three major components (Fig. 1):
<br><br>
(i) a neutral density filter (optical density typically between three and for) for the attenuation of the laser power to facilitate the measurement with a standard webcam;
<br><br>
(ii) a lens system for demagnification of the laser beam - with f2/f1 = M, the desired demagnification;
<br><br>
(iii) a cheap webcam with a sensor chip which is easily accessible by disassembly of the webcam and an elevated surface in the webcam housing for easy mounting.
<br><br>
<img src="https://raw.githubusercontent.com/rainerkaufmann/BeamProfiler/master/fig1_parts.jpg" width="512">
<br>
Figure 1 | Major components of beam profiler.
<br><br>
The webcam we are currently using is an AUSDOM AW335 with a ¼” CMOS chip and a resolution of 1920 x 1080 pixels. A standard ¼” chip has a light sensitive area with a diagonal of approximately 4.5 mm, resulting in a pixel size of about 2 µm x 2 µm. Both parameters still have to be evaluated by reflection microscopy imaging.
<br>
In addition to a very low price of approx. 15 EUR, the webcam has a threaded tube comprising the sensor chip, which is an ideal working point for the mount in the optical setup. The CAD drawing of the mount for the partially disassembled webcam can be seen in Fig. 2. One part of the mount is complementary to the threaded tube of the webcam; the other is mimicking a mounting plate of the Thorlabs optical cage system.
<br><br>
<img src="https://raw.githubusercontent.com/rainerkaufmann/BeamProfiler/master/fig2_camera-mount.jpg" width="512">
<br>
Figure 2 | Camera mount.
<br><br>
The rest of the setup is built from parts of the of Thorlabs cage mounting system, posts and post holders and simple optical elements. The total price for our beam profiler was 372 EUR including VAT and delivery cost (for details see Table 1). The cost can be remarkably reduced (~180 EUR) by using free-standing optical mounts and simple NBK7 glass lenses. It shall be noted, that commercial beam profilers often need de-(magnification) and/or attenuation optics, too.
<br><br>
<table>
  <tr>
    <th>Parts (from Tholabs if not stated otherwise)</th>
    <th>Price (EUR)</th>
  </tr>
  <tr>
    <td>½” Post & post holder</td>
    <td align="right">20</td>
  </tr>
  <tr>
    <td>30 mm cage plates and assembly rods</td>
    <td align="right">80</td>
  </tr>
  <tr>
    <td>1” Neutral density filter</td>
    <td align="right">55</td>
  </tr>
  <tr>
    <td>Achromatic, anti-reflection lenses</td>
    <td align="right">200</td>
  </tr>
  <tr>
    <td>1080p Webcam (AUSDOM AW335)</td>
    <td align="right">15</td>
  </tr>
  <tr>
    <td>Mount for Webcam (3D-printed)</td>
    <td align="right">2</td>
  </tr>
<table>
Table 1 | Individual costs of beam profiler components.
<br><br><br>
<h3>Discussion of issues</h3>
One might wonder why there is no wide spread of low-cost, home-built beam profiler. This is probably due to the “Bayer-problem”. Consumer cameras, including webcams, are colour sensors, which have filters in front of each pixel in a pattern of alternating rows of red/green and green/blue filters, called Bayer-filter (or Bayer-pattern). Furthermore, the signal received by a single pixel is further processed and interpolated with its surrounding pixels to finally obtain a colour image. Both facts are rendering consumer cameras fairly unfavourable for beam profiling.
<br>  
However, we are in the process of testing three different options (all of them are still work in progress) to circumvent these problems:
<br><br>
(A) Mostly ignoring the problems, which can result in a spiky beam profile (Fig. 3), but should provide proper beam parameters for spot sizes order of magnitudes greater than the pixel size. Further optimization routines can be:
<br>
(A.1) Smoothing the measured data with standard filters (e.g. gaussian or mean).
<br>
(A.2) Removing pixels with non-fitting colour filters or binning 2x2 pixels with the value of the pixel with fitting colour filter in this matrix and hence, reducing the resolution of the final image to 960x540 pixels with a pixel size of 4 µm x 4 µm. For this, the Bayer-pattern of the webcam has to be known, e.g. by investigating the wavelength dependencies of the values of each pixel.
<br><br>
(B) Using the raw data of an image showing the Bayer-pattern. However, it is difficult to extract the raw data from a webcam, depending on the manufacturer. The raw data can be processed the following ways:
<br>
(B1) Calculate a correction factor for each colour filtered pixel (red, green, blue) according to the wavelength of the lasers (for more detail see: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3584619/#!po=45.0000).
<br>
(B2) Since the Bayer-pattern can easily be known by analysing the raw data, the method (A.2) can be applied (further information: https://arxiv.org/pdf/1801.06508.pdf).
<br>
(B3) Manually removing the Bayer-filter of the sensor chip. However, this process often damages the CMOS and removes the microlens-array in front of the pixels.
<br>
(C) Using a blank, high resolution CMOS or CCD sensor chip without a Bayer-filter and do the wiring, controlling and programming yourself. Disadvantage: this process would be very time consuming.
<br><br>
