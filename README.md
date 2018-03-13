# water-diviner
An AR app to guide users to the nearest water source

# Initial Approach

## Geolocated Data
We found the OpenStreetMaps has the largest catalog of drinking water sources: 
https://wiki.openstreetmap.org/wiki/Tag:amenity%3Ddrinking_water
- [ ] Figure out how to pull that data via an API call
- [ ] Search through ArcGIS water related datasets
- [x] Make Reddit call to OSM channel: https://www.reddit.com/r/openstreetmap/comments/846gnf/creating_reality_vr_hackathon_ar_water_map/

## Hardware
We currently have a Meta 2 headset that I was able to lean from MetaVision. Then HP loaned us a backpack workstation that can run VR,
so we're thinking of a AR experience that uses those in combo.

## Three initial routes for the framework

### Plan A: ArcGIS Mapping Engine
ArcGIS is one of the Gold Sponsors of the Creating Reality hackathon, and they are offering a $2500 prize for building something either 
with their new AR Runtime SDK (preferrably), or some of their API's. Issue currently is their new SDK doesn't work with Unity. 
We've talked through a couple of ways to hack it to work with the OpenVR SDK though, we just need to get the ArcGIS SDK (.NET) to talk
with the OpenVR standard (C++).  
https://github.com/ValveSoftware/openvr/tree/master/samples
https://github.com/Esri/hololens-terrain-viewer/blob/master/README.md
- [ ] Dig through OpenVR Standard and get a basic understanding of it
- [ ] Join the ArcGIS AR Runtime SDK Private Beta program
- [ ] Dig through ArcGIS AR Runtime SDK

### Plan B: Mapbox + Unity with ArcGIS API calls
Our alternative approach is to use Mapbox's Unity SDK. Our team is generally much more familiar with Unity, and I've worked with 
Mapbox in Unity before several times. If we go this route we could make something similar to Pokemon Go style, and spend more time working
on gamifying the experience, playing with the dynamics of a reputation system for discovering/auditing drinkable water sources, and so on.


### Plan C: AR Core
We also have a Google Pixel, and ArcGIS Runtime SDK works with Android, so a simpler route might be to build a phone AR based experience.
