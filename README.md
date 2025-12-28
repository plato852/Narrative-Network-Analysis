# Narrative Network Analysis of Technology News (1987–2007)

## Project Overview
This project presents a large-scale **narrative network analysis (NNA)** of technology news coverage in *The New York Times* between 1987 and 2007. By combining natural language processing with network science, the study models how corporations, technologies, and institutions are positioned within media narratives during a critical period of digital transformation.

## Research Motivation
Traditional narrative analysis in media studies relies heavily on manual coding, limiting scalability and reproducibility. This project addresses these limitations by implementing an automated, data-driven framework capable of extracting and analysing narrative structure across hundreds of thousands of articles.

## Data
- **Source:** [New York Times Annotated Corpus](https://abacus.library.ubc.ca/dataset.xhtml?persistentId=hdl:11272.1/AB2/GZC6PL)  
- **Period:** 1987–2007  
- **Corpus Size:** ~500,000 technology-tagged articles  
- **Background Corpus:** General NYT Top News articles for relative weighting and bias comparison  

## Methodology
The analysis follows a rigorous computational pipeline:

1. **Preprocessing & NLP**
   - Article filtering using NYT taxonomy tags  
   - Co-reference resolution to maintain entity continuity  
   - Neural dependency parsing for grammatical structure  

2. **Narrative Extraction**
   - Subject–Verb–Object (SVO) triplet extraction  
   - Entity and verb normalisation  
   - Frequency- and semantics-based filtering  

3. **Network Construction**
   - Directed, weighted semantic graphs  
   - Nodes represent entities; edges represent actions  
   - Edge weights encode narrative frequency  

4. **Network Analysis**
   - Centrality measures: degree, betweenness, closeness, HITS, PageRank  
   - Community detection using the Louvain algorithm  

5. **Entity Bias Analysis**
   - **2011 Subject/Object Bias** (syntactic agency)  
   - **2013/2015 Relevance Weighting** (domain-specific salience)  
   - Comparative validation using Spearman correlation  

## Key Findings
- Corporations such as **Microsoft** and **IBM** consistently emerge as central narrative actors.  
- Financial and regulatory terms play a significant structural role, highlighting the economic and institutional framing of technology discourse.  
- Subject/object bias reveals systematic differences between actors portrayed as **initiators** (corporations, entrepreneurs) and **recipients** (technologies, infrastructures).  
- A strong Spearman correlation (ρ ≈ 0.85) confirms the robustness and consistency of alternative bias formulations.

## Tools & Technologies
- **Language:** Python  
- **NLP:** spaCy, Stanza, Coreferee  
- **Network Analysis:** NetworkX, Gephi  
- **Data Formats:** JSON, GraphML  
- **Environment:** Jupyter Notebook  

## Future Work
- Extend the framework to multi-source and multilingual news corpora  
- Incorporate sentiment and emotion analysis  
- Adapt the pipeline for real-time narrative monitoring  

