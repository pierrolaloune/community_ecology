# Community ecology code
Data manipulation in community ecology using different datasets (TRY, sPlot, BIEN) and community ecology index

As part of our scientific methodology, we proceeded to manipulate the data in order to create two distinct databases: one dedicated to the traits of woody species in the Mediterranean region, and the other to the communities of these same species. To do this, we integrated the community data from the _sPlot_ database with the trait data available in the _BIEN_ database. In order to enrich our collection of trait data, for which some information was missing, we also called on the _TRY_ database, an approach which enabled us to efficiently complete our dataset. Before integrating the data into our methodology, it is important to note that the information within the databases has been standardized beforehand. This crucial step ensures data consistency and quality, facilitating comparative analysis and integration.

## How sPlot Works
### Data Integration
sPlot amalgamates vegetation-plot data, including species composition, geographical locations, and environmental conditions from different regions or countries, into a single, accessible framework.
### Standardization
To ensure comparability across datasets, sPlot standardizes data formats, species nomenclature, and environmental variables. This process involves harmonizing scientific names and ensuring consistent measurement units for environmental variables.
### Accessibility
Researchers can access the database for specific projects, adhering to ethical guidelines and data-sharing policies that govern the use of sPlot data.
### Collaboration and Growth
sPlot is designed to be collaborative, allowing contributors to add new datasets continuously. This feature ensures that the database remains up-to-date and reflective of current vegetation patterns and biodiversity.
### Information Contained in sPlot
sPlot hosts a wealth of information crucial for a wide range of ecological inquiries:
- Species Composition: Lists species present in each plot, including vascular plants and sometimes bryophytes and lichens.
- Abundance and Cover: Provides data on the abundance or cover of species, facilitating analyses of community structure.
- Plot Metadata: Includes plot size, sampling date, and methodology.
- Geographical Location: Enables spatial analyses of vegetation patterns across different environmental gradients.
- Environmental Conditions: Offers data on soil, climate, and other conditions for exploring vegetation-environment relationships.
- Temporal Data: Supports studies of vegetation changes over time through repeated plot surveys.
### Applications
The sPlot Database is instrumental in addressing questions related to:
- Global patterns of plant trait diversity
- Effects of climate change on vegetation
- Conservation status of different vegetation types
- Distribution and impact of invasive species

## BIEN and TRY Databases Overview
### BIEN Database
#### Introduction to BIEN
The Botanical Information and Ecology Network (BIEN) is a comprehensive platform that aggregates and standardizes global botanical data. Its primary aim is to support large-scale analyses of plant biodiversity, biogeography, and trait distributions. By integrating botanical observations, specimen records, and trait data from various sources, BIEN facilitates research on plant diversity patterns and responses to environmental changes.
#### How BIEN Works
- Data Aggregation: BIEN compiles botanical data from herbarium records, plot inventories, and observational datasets, offering a unified resource for exploring global plant diversity.
- Standardization and Quality Control: The database employs rigorous data cleaning and standardization protocols to ensure data accuracy and comparability. This includes verifying species nomenclature and harmonizing trait measurements.
- Accessibility and Tools: BIEN provides user-friendly tools for data exploration, species distribution modeling, and trait analysis. Researchers can access spatially explicit data on species occurrences and traits to conduct biodiversity assessments.
#### Information in BIEN
- Species Occurrence Records: Geographic locations and environmental settings where plant species have been observed or collected.
- Plant Traits: Standardized measurements of plant functional traits, such as leaf size, wood density, and seed mass, which are critical for understanding ecological strategies.
- Taxonomic Information: Detailed taxonomic hierarchies and synonymy, facilitating research on biodiversity patterns across taxonomic groups.
- Phylogenetic Trees: Phylogenetic relationships among plant species, supporting studies on evolutionary patterns and trait evolution.
### TRY Database
#### Introduction to TRY
The TRY Plant Trait Database is a global repository that collates plant trait data with the objective of improving our understanding of plant functional diversity. Managed by a consortium of international researchers, TRY focuses on making trait data accessible to the scientific community to foster research on climate change impacts, ecosystem services, and biodiversity conservation.
#### How TRY Works
- Collaborative Data Collection: TRY compiles plant trait data from published studies, databases, and direct contributions from researchers worldwide.


# Community Data Analysis with sPlot

This repository is dedicated to the analysis of woody plant community data in the Mediterranean region. The primary aim is to merge community data from the sPlot database with trait data from BIEN and TRY databases, focusing on enriching our dataset with missing trait information. This README outlines the methodology used to prepare and analyze the data, the evaluation of Mediterranean woody plant community characterization rates, and the calculation of diversity indices.

## Data Preparation and Manipulation

The data analysis process began by setting the working directory to where our datasets are located. Essential R packages such as `dplyr`, `tidyr`, `ggplot2`, `sf`, and others were loaded to facilitate data manipulation, visualization, and analysis.

The primary datasets include:

- `sPlot_traits.csv` for species traits.
- `sPlot_species_abundance.csv` for species abundance.
- `sPlot_header.csv` and `sPlot_metadata.csv` for additional metadata.
- Additional datasets for specific analyses, like `sPlot_woodiness.csv` for woody species.

Data from the sPlot community database was merged with trait data, with missing trait information supplemented from the TRY database. Standardization of information across databases was crucial to ensure data uniformity and quality for subsequent analyses.

## Evaluation of Mediterranean Woody Plant Community Characterization Rates

Unique species were identified from the dataset, and a species-site matrix was created. This allowed for the calculation of species characterization rates within communities, highlighting the predominant species that define the Mediterranean landscape. The analysis focused on differentiating generalist species from those adapted to specific ecological niches.

## Diversity Indices

### Defining and Naming Communities

Communities were defined based on species frequency data, with each community assigned a unique name. Communities were then summarized by the number of species, average abundance, and other metrics. The association of communities with specific habitats and abiotic conditions was examined by integrating data on habitat types and environmental factors.

### Calculating Species Abundance Distribution

The distribution of species abundance within communities was analyzed, revealing a pattern of few common species and many rare species. This pattern aligns with Fisher's logarithmic series, emphasizing the prevalence of numerous rare species compared to a few common ones.

### Alpha Diversity

Alpha diversity, representing the number of species found at a local scale within a habitat or site, was calculated using the Shannon diversity index. This index reflects both species richness and evenness in species distribution across communities.

### Beta Diversity

Beta diversity was analyzed using the Bray-Curtis index, suitable for abundance data rather than presence/absence data. NMDS ordination based on Bray-Curtis distances was performed to explore community distribution patterns in multidimensional space. Hierarchical clustering further investigated community similarities based on species composition, and beta diversity analyses were conducted to study the diversity between different community groups in relation to environmental variables and alpha diversity indices.

## Repository Structure

- Data preparation scripts and analyses are documented, focusing on merging, cleaning, and analyzing plant community and trait data.
- The diversity of Mediterranean woody plant communities is evaluated, highlighting predominant species and their ecological niches.
- Alpha and beta diversity indices are calculated to examine within-community species richness and between-community species composition variation.

## Contributions

This work contributes to understanding the biodiversity and structure of plant communities in the Mediterranean region. Insights into species dominance, ecological niches, and community composition in relation to environmental factors are provided, enhancing our knowledge of Mediterranean ecosystems.

Pierre Bouchet, 2024-03-28

- Trait Harmonization: The database standardizes trait definitions and units, offering a consistent framework for trait data. This includes a comprehensive trait ontology covering various plant functional traits.
- Data Availability: Researchers can request access to TRY data for specific projects, subject to data use agreements that respect data contributors' conditions.
#### Information in TRY
- Plant Functional Traits: An extensive collection of quantitative traits, including physiological, morphological, and phenological traits, for thousands of plant species.
- Metadata: Contextual information accompanying trait measurements, such as experimental conditions, growth forms, and geographic locations.
- Data Sources: References and origins of the trait data, ensuring transparency and traceability.
