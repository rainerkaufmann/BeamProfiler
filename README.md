## Low-cost beam profiler (WIP)

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
The rest of the setup is built from parts of the of Thorlabs cage mounting system, posts and post holders and simple optical elements. The total price for our beam profiler was 372 EUR including VAT and delivery cost (for details see Table 1). The cost can be remarkably reduced (~180 EUR) by using free-standing optical mounts and simple NBK7 glass lenses. It shall be noted, that commercial beam profilers often need de-(magnification) and/or attenuation optics, too.
<br><br>
<table>
  <tr>
    <th>Parts (from Tholabs if not stated otherwise)</th>
    <th>Price (EUR)</th>
  </tr>
  <tr>
    <td>½” Post & post holder</td>
    <td>20</td>
  </tr>
  <tr>
    <td>30 mm cage plates and assembly rods</td>
    <td>80</td>
  </tr>
  <tr>
    <td>1” Neutral density filter</td>
    <td>55</td>
  </tr>
  <tr>
    <td>Achromatic, anti-reflection lenses</td>
    <td>200</td>
  </tr>
  <tr>
    <td>1080p Webcam (AUSDOM AW335)</td>
    <td>15</td>
  </tr>
  <tr>
    <td>Mount for Webcam (3D-printed)</td>
    <td>2</td>
  </tr>
<table>
Table 1 | Individual costs of beam profiler components.
<br><br>
Discussion of issues...
