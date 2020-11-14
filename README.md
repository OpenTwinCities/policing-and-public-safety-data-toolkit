# Policing and Public Safety Data Toolkit  

## Project overview  

Important conversations around policing practices and public safety are happening in cities and towns across the country. We need to empower more civic technologists to leverage data to help deepen these conversations. Inspired by projects like the [Stanford Open Policing Project](https://openpolicing.stanford.edu/) and the [Center for Policing Equity](https://policingequity.org/), we recognize that common approaches, a shared vision of what data collection/aggregation can look like, and shared conceptual understandings can empower more people to engage with policing and public safety data in their communities.  

There are two specific “gaps” that this toolkit focuses on:  

1. Some municipalities have data available, but limited data analysis capacity.  
    **Solution:** Example notebooks, aimed at brigade members and other volunteers, to act as templates for asking and answering questions around policing and public safety using data sets that are commonly available in communities.  

2. Some municipalities have limited data available.  
    **Solution:** Provide information on where to find data, the laws around public data, and how to make data requests.  

A primary audience of this work is Code for America Brigade members and other volunteers who seek inspiration for how to start looking at policing and public safety data in their communities.  We’re assuming some basic background in data analysis (familiarity with .CSV files, navigating open data websites, some basic familiarity with R/Python, etc.). The resources in this toolkit should help civic technologists get up and running faster when trying to leverage local data to deepen your own local conversations.  

We also want to acknowledge that data has power, and is imperfect. None of the analyses or examples in this toolkit should be taken as a source of "final truth" or "ultimate proof".  These resources should be used to _start_ conversations, not _end_ them.  If used right, this toolkit can lead you to more--and better--questions. Remember: data _never_ tells the whole story, but it can help us deepen the stories we tell, or identify stories that are missing.  

**Goals:**  
    + Elevate existing projects and efforts; avoid reproducing others' work wherever possible.  
    + Use existing data to ask questions, notice patterns, and deepen public conversations.  
    + Explore both the problems in existing policing practices and new possibilities for promoting public safety.  

**Out of current scope:**  
    - Create a national clearinghouse of policing and public safety data  
    - Large-scale data collection efforts  


## Repository structure  

**data/**  
Only host data in this GitHub repository if absolutely necessary (for example, if data is not consistently maintained or runs the risk of disappearing at its original source location).  Otherwise, reference the original source website in your notebook and show how the data can be obtained directly from the source. *TODO*: Work on a set of archival "best practices" for storing datasets. Create a tutorial to help civic technology teams get started with this.  

**notebooks/**  
Templates, separated by topic folder, that act as examples of the kinds of analysis and storytelling you can do with some of the common types of policing and public safety data that are available for many cities/states/regions. Ideally, these should be structured so that others can look at the notebook, repoint it to a different data source from a different city/state/region, and adapt it for local use. When a notebook is ready to publish, it should be rendered as .HTML and saved to the corresponding location in the reports/ folder.  
```pre
├── police_stops
│   ├── police_stops.Rmd
│   └── police_stops.ipynb
├── non_emergency_incidents ← 311 calls/reports, non-emergency incident reports
├── emergency_911
├── use_of_force
├── arrests
├── warrants
├── police_equipment ← supply lines, LESO data, equipment budgets, etc.
├── police_personnel_records ← police force demographics, misconduct records, contracts, training
└── hate_crime
```  

**references/**  
Data dictionaries to help understand commonly-found data elements present in different types of policing and public safety datasets, data source lists (by state) and additional resource links.  
```pre
├── data_dictionaries
│   ├── data_dictionary_police_stops.md
│   └── data_dictionary_other.md (etc.)
├── data_sources
│   ├── federal.md
│   ├── minnesota.md
│   └── other_state.md (etc.)
└── additional_resources.md
```  

**reports/**  
Rendered notebooks in .HTML format, separated by topic folder. Reports in this folder are intended to be viewable in a web browser.  Keep your naming structure consistent between this folder and the notebooks/ folder.  
```pre
├── police_stops
│   └── police_stops.html
├── non_emergency_incidents ← 311 calls/reports, non-emergency incident reports
├── emergency_911
├── use_of_force
├── arrests
├── warrants
├── police_equipment ← supply lines, LESO data, equipment budgets, etc.
├── police_personnel_records ← police force demographics, misconduct records, contracts, training
└── hate_crime
```  

**tutorials/**  
Tutorials addressing important topics in policing and public safety data to help civic technologists understand, approach, and advocate for effective use of this data.  
```pre
├── gather_and_understand_existing_data.md
├── request_data.md
└── advocate_for_good_data_practices.md
```  

**index.html**  
Public-facing landing page, which offers a friendly way to consume parts of the toolkit for folks who don't like looking at GitHub.  
*TODO: add Reports: Links to .HTML pages in reports/ folder*  
*TODO: add Tutorials: Links to markdown docs on GitHub (for now)*  


Note: This repository structure is modeled off of [DrivenData's Cookiecutter Data Science](https://drivendata.github.io/cookiecutter-data-science/#directory-structure) template.  
