## Low-cost beam profiler (WIP)

Knowing the exact diameter and profile of a laser beam is highly beneficial for a wide range of (bio-)optical applications; e.g. determining the power distribution of your laser spot to avoid radiation damage on your sample or optical elements. Unluckily, commercial beam profilers (either camera based or scanning slit / knife-edge devices) usually cost several k EUR. Consequently, several research groups have created designs for low-cost beam profiler.
<br><br>
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
Fig. 1
<br><br>
The webcam we are currently using is an AUSDOM AW335 with a ¼” CMOS chip and a resolution of 1920 x 1080 pixels. A standard ¼” chip has a light sensitive area with a diagonal of approximately 4.5 mm, resulting in a pixel size of about 2 µm x 2 µm. Both parameters still have to be evaluated by reflection microscopy imaging.
In addition to a very low price of approx. 15 EUR, the webcam has a threaded tube comprising the sensor chip, which is an ideal working point for the mount in the optical setup. The CAD drawing of the mount for the partially disassembled webcam can be seen in Fig. 2. One part of the mount is complementary to the threaded tube of the webcam; the other is mimicking a mounting plate of the Thorlabs optical cage system.
