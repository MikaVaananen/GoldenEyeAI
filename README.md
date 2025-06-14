<!-- This is the markdown template for the final project of the Building AI course, 
created by Reaktor Innovations and University of Helsinki. 
Copy the template, paste it to your GitHub README and edit! -->

# GoldenEyeAI
Final project for the Building AI course

## Summary
The aim of the project is to identify parts on CMS particle tracker modules. GoldenEyeAI will detect the alignment and offset of module parts with relation to each other for module quality assurance purposes.

## Background
The tracker modules consist of three layers: silicon sensor, readout chip and an interconnect PCB. The layers are first glued together, and electrical connections between layers are formed with wirebonds. The bonds are very small and delicate, any small deviation in the expected location of bond pads can be catastrophic. The modules are expensive and limited in availability, so monitoring the bond pad offsets is crucial for a succesful production run. In total, some thousands of modules will be used and any data that can be collected can be very useful in future production runs.

# Problems to solve:
* Angular alignment of module layers: how large of a deviation is there between layers?
* Translational offsets of module layers: how well are the layers aligned translationally?

## How is it used?
GoldenEyeAI will be used before wirebonding the layers together. The wirebond operator will place a glued module under a camera jig, that will take a high-resolution image of the module. The operator will then run GoldenEyeAI, which will measure the rotational and translational misalignment of the module layers. Here is an example image of a module:
![Example image of a module](/module.jpg)
The gray areas on the top and bottom of the module are the readout chip wirebond pads, and the golden areas on the green PCB are the wirebond pads on the interconnect. GoldenEyeAI will be used in multiple research institutes and production centers with differing photography jigs, so the images will vary depending on the user.

## Data sources and AI methods
The AI method used for detection will be a CNN. We essentially need to identify small areas on the images, so a CNN will be a good fit. The data will be collected from a number of production centers that are already equipped with photography jigs.

## Challenges
The project will not solve any further problems related to the quality of the modules. The scope is limited only to the alignment of module layers.

## What next?
A standardized photography jig that would be used at the different production centers would drastically improve data quality.

## Acknowledgments
The inspiration of this project comes from the CMS collaboration, and specifically the CMS Upgrade project.
