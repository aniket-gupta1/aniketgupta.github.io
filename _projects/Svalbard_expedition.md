---
layout: page
title: Svalbard Expedition
description: An expedition to the Arctic to understand and quantify glacier melt with modern computer vision. 
img: assets/img/Svalbard.jpeg
importance: 2
category: work
---
In August 2024, I participated in a research expedition to the Svalbard archipelago in the Arctic, aimed at studying glacial melt using Unmanned Aerial Vehicles (UAVs) and photogrammetry techniques. The expedition was organized in collaboration with NTNU in Norway and Greenpeace. The over-arching goal of the project was to deploy UAVs to capture high-resolution imagery of several glaciers over multiple days. This will enable the development of high-resolution 3D maps of the glaciers for each day, allowing us to measure changes in glacial morphology over time. 

<div class="row">
    <div class="col-sm-12 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/svalbard/overview.png" title="Svalbard Overview" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The mapping expedition to the Kongsbreen (pictured above) and other glaciers in Svalbard was conducted on the Greenpeace sailing research vessel S/Y Witness. Small UAS were deployed from this vessel to repeatedly collect very high resolution imagery of the marine terminating glaciers over the course of the week long expedition
</div>

### Project Date and Location
* **Campaign Date:** August 2024 
* **Location:** Northern Svalbard Arctic Archipelago, in the vicinity of Ny-Ålesund 
* **Glaciers Surveyed:** Blomstrandbreen, Conwaybreen, Kongsbreen, and Kronebreen


### Project Goals
Glacial melt is a major contributor to global sea level rise and a component of freshwater influx into the world's oceans. While satellite observations measure glacial retreat at a coarse scale, they are limited by spatial resolution and sparse temporal sampling due to cloud cover.

This campaign aimed to measure temporal changes in glacial morphology on highly active marine-terminating glaciers using Unmanned Aerial Vehicles (UAVs).

Specific objectives included:

1.  **Develop Change Detection Algorithms:** Create photogrammetry-based change detection algorithms.
2.  **Achieve High Resolution:** Measure changes in glacial morphology at high spatial ($<1$cm) and temporal ($<24$hrs) resolutions.
3.  **Measure Processes:** Collect data to measure frontal ablation, melt, and surge at the glacier front.

### Data Collection Methodology
* **Vessel:** The expedition was conducted using the Greenpeace research sailing vessel **S/Y Witness**.
* **Logistics Focus:** Expedition goals included minimizing logistical costs and minimizing the carbon footprint.
* **Equipment:** Commercially available **DJI Mavic Pro UAVs** were manually flown close to the glaciers.
* **Data Type:** The UAVs captured high-resolution, highly overlapping imagery, which was geotagged with GPS metadata to facilitate accurate georeferencing of 3D reconstructions.

### Surveyed Glaciers
The expedition visited a total of five unique sites.
* **Sites Visited:** Blomstrandbreen, Conwaybreen, Kongsbreen, and Kronebreen glaciers.
* **Repeated Visits (for detailed melt characterization):** Blomstrandbreen, Kongsbreen-North, and Kronebreen-North were surveyed three independent times each during the four-day period, over intervals of 1–2 days.

### Key Results and Discussion
* **Reconstruction Quality:** High-resolution and high-overlap imagery yielded very low covariance estimates across all 3D reconstructions.
    * Along the Kronebreen-North glacier, the estimated covariance for $>90\%$ of the $2.1$ million tie points was $<1$cm.
* **Decoupling Motion and Melt:** To accurately quantify melt, glacier motion must be decoupled from melt and calving.
    * The team mapped crevasses over $\sim70$ meters of the glacier surface, which serve as robust visual features for point cloud matching across days, enabling accurate estimation of glacier displacement.
* **Glacier Motion Rate:** Preliminary results for **Kronebreen-North** indicated an average motion of approximately **3 meters per day**, consistent with previously reported velocity estimates.
* **Volume Loss Measurement:** By compensating for translational motion and aligning the daily 3D reconstructions, a consistent map is obtained from which volume loss can be accurately measured.
    * Observed morphological change over a single day (Figure 3) clearly shows volume loss, with big pieces falling off along large crevasses. This calving is likely where ice is significantly affected by melt from seawater undercutting.

<div class="row">
    <div class="col-sm-12 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/svalbard/dense_map.png" title="Dense Map" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Some intermediate results of our processing pipeline. (Top) Imagery texture mapped on top of the 3D reconstruction of a section of the Kronebreen-North glacier (Bottom) A plot of the covariance of the measurements associated with the 3D reconstructions above (colormap _viridis_ - dark blue represents low covariance, bright green represents highest covariance). We note that the covariance for approximately 92\% of the 2.1M points in the 3D SfM reconstruction is $<$1cm.
</div>


<div class="row">
    <div class="col-sm-12 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/svalbard/change_kronebreen.png" title="Change at Kronebreen" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Aligned point clouds from 2024/08/25 (blue) and 2024/08/26 (light blue) of a section from the Kronebreen-North glacier. We can clearly see the volume loss on the glacier, most of the big pieces fall off along big crevasses where the ice is significantly affected by melt from seawater undercutting them.
</div>