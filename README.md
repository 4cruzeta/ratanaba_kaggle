# 1. Introduction

This notebook is part of the research project "OpenAi to Z Challenge", which aims to uncover archaeological sites in the Amazon rainforest, with a particular focus on the investigation of geoglyphs and evidence of human intervention.

To achieve this, we will utilize the Copernicus GLO-30 Digital Elevation Model (DEM) dataset available in GeoTIFF format. Our analysis aims to visualize various aspects of the terrain to identify anomalies that may indicate human activity or historical geoglyphs.

Throughout this notebook, we will employ different visualization techniques, including hillshade, slope mapping, aspect analysis, and color relief mapping, to enhance our understanding of the spatial characteristics of the landscape. We will evaluate which visualization methods provide the clearest insights into the potential archaeological sites.

The following sections will outline our approach and methodology, including data loading, processing, and visualization, ultimately leading to a discussion of the observed results.

#### Dataset Citation:

NASA JPL (2021). <i>NASADEM Merged DEM Global 1 arc second V001</i>.  Distributed by OpenTopography. https://doi.org/10.5069/G93T9FD9. Accessed: 2025-06-06

European Space Agency (2024).  <i>Copernicus Global Digital Elevation Model</i>.  Distributed by OpenTopography.  https://doi.org/10.5069/G9028PQB. Accessed: 2025-06-11
# Updating Our Project to Meet the Next Checkpoints

We’ve been making great progress on our current project, successfully implementing image processing, filtering, and export functions using Google Earth Engine. Throughout this process, we’ve worked diligently to fine-tune our functions, ensuring they are robust and aligned with actual data (such as available bands like `'MSK_CLDPRB'` and `'SCL'`).  

Now, our next goal is to integrate these steps into a comprehensive workflow that fits the upcoming project checkpoints. Here's the plan:

### Next Steps in Our Workflow:

1. **Download Data for Each Site**  
   We will create a loop that processes each site—using their coordinates—and applies our existing filtering functions precisely as developed. This ensures each dataset is processed consistently and efficiently.

2. **Automate Image Processing and Export**  
   For each location, we will:
   - Set the region based on site coordinates.
   - Retrieve the Sentinel-2 collection.
   - Apply our custom filtering functions (masking clouds and shadows).
   - Generate median composite images.
   - Export the images for further analysis.

3. **Leverage the Data in AI Prompts**  
   Once images are ready, we plan to use an AI API **(like GPT-4.1 Vision)** to analyze these images' contents, generate descriptions, identify anomalies, and produce candidate footprints.

### Our Progress:

- **Function Development:**  
  We've successfully developed functions that perform visual filtering with correct band references, using available bands like `'MSK_CLDPRB'` and `'SCL'`.  
- **Data Integration:**  
  We are now prepared to process multiple sites using a combined loop that automates the entire pipeline.

### Moving Forward:

- Adjust the project workflow to run these functions iteratively for all sites.
- Ensure the images are exported correctly, and archives are ready for analysis.
- Incorporate AI prompts to interpret the visual data and generate actionable insights.

**We're on the right path, and these refinements will make our process robust, scalable, and ready to meet the upcoming checkpoints.**  
