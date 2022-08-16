This readme.txt file was generated on <YYYY-MM-DD> by <Name>
Date last modified: <YYYY-MM-DD>	Current version: <VX.X>

TABLE OF CONTENTS
=================
* DATASET TITLE
* AUTHORS AND AFFILIATIONS
* ACKNOWLEDGEMENTS
* LANGUAGE
* SUMMARY/ABSTRACT
* KEYWORDS
* FILE ORGANIZATION
* BACKGROUND INTRODUCTION
* DATASET DESCRIPTION 
* DATA DICTIONARIES
* METHODOLOGY DESCRIPTION
* DATA ANALYSIS
* RESULTS/CONCLUSION AND DISCUSSION 
* SHARING & ACCESSING INFORMATION
* RELATED MATERIALS
* ADDITIONAL NOTES/COMMENTS

DATASET TITLE
-------------
* Dataset title: Data from the Code.gov website


AUTHORS AND AFFILIATIONS
------------------------
* Dataset producer(s)/creator(s): 
	- Name: 
	- Organization/institution: U.S. General Services Administration
	- Email: code@gsa.gov
* Primary contact: 
	- Name: 
	- Organization/institution:
	- Email:
* Contributor(s): 
	- Name: 
	- Organization/institution:
	- Email:


ACKNOWLEDGEMENTS
----------------
* Funding information: 
	- Funder name:  
	- Grant number: 
	- Principle investigator (PI):
		- Name: 
		- Organization/institution:
		- Email:
* Supervision, collaboration, and help:
	- Supervision/guidance: 
		- Name: 
		- Organization/institution:
		- Email:
		- Supervision/guidance details:
	- Collaboration: 
		- Name: 
		- Organization/institution:
		- Email:
		- Collaboration details: describe the roles of different collaborators	
	- Help: 
		- Source of the help: may come from a person or an organization, etc.
		- Source contact: address, location, or web link, etc.
		- Help details: describe what you obtained from the source.
* Reference publication/resources: 
	- citation: 
	- link:


LANGUAGE
--------
* Language: Default is English; add more if not only English


SUMMARY/ABSTRACT
----------------
* The research question related to the dataset: 
* Characteristics of your dataset: 


KEYWORDS
--------
* Keywords: Please make a keyword list; separate keywords using semi-colon (;)
federal government; open source software

FILE ORGANIZATION
-----------------
* File structure:
	- Directories/folders
		- Directory/folder name: Code_gov
		- Files:
			- File name: agency_name.json
			- File type: dataset

BACKGROUND INTRODUCTION
-----------------------
* What is your interest/motivation/objective(s): Document open source software produced by the federal government.
* Provide the project history: 
* How does this project contribute overall? 


DATASET DESCRIPTION 
-------------------
* Data attribute: Describe if the dataset is experimental/simulation/observational, quantitative/qualitative, etc. For example, simulation of Hurricane Katrina, genomics sequence of a new string of bacteria.
	- If collected dataset, please provide the following info:
		- Collection date and time: 2022-06
		- Collection details: Downloaded the JSON files from the code.gov website.
* Data sources: Please provide provenance information
	1). Internal data source: Please provide relationships with other (data) files in the project, include name and location
	- Spreadsheet with the code hosting platforms
	2). External data source: If the original data is obtained from other (pre-existing) sources, such as other publication/repo/website/database, etc, please include name, location, query and the time while doing the query, url, citation/bib record, AND the licenses/restrictions for re-use.


DATA DICTIONARIES
-----------------
The provided columns/variables can vary by agency.

Standard list of columns/variables:
* Name: `agency`
* Meaning/definition: The agency acronym for Clinger Cohen Act agency, as defined by the United States Government Manual.
* Pattern:
	- Conventions/standards that follow: The agency acronym for Clinger Cohen Act agency, as defined by the United States Government Manual.
	- Value domain: text
	
* Name: `version`
* Meaning/definition: The version of the metadata schema in use. Implements semantic versioning 2.0.0 rules as defined at http://semver.org
* Pattern:
	- Conventions/standards that follow: e.g. 2.0.0
	- Value domain: text
	
* Name: `measurementType`
* Meaning/definition: An object containing description of the open source measurement method.
* Specified values: 
	- value: **cost**
	- definition: Cost of software development
	
	- value: **systems*
	- definition: System certification and accreditation boundaries
	
	- value: **projects**
	- definition: A complete software solution / project
	
	- value: **modules**
	- definition: A self-contained module from a software solution
	
	- value: **linesOfCode**
	- definition: Source lines of code
	
	- value: **other**
	- definition: Another measurement method not referenced above

* Name: `releases`
* Meaning/definition: List of objects containing each versioned source code release made available.
* Field names for each object:
	- `name` - The name of the release.
	- `version` - The version for this release. For example, '1.0.0'.
	- `organization` - The organization or component within the agency to which the releases listed belong. For example, '18F' or 'Navy'.
	- `description` - A one or two sentence description of the release.
	- `permissions` - An object containing description of the usage/restrictions regarding the release.
		- `licenses`
			- `URL` - The URL of the release license, if available. If not, null should be used.
			- `name` - An abbreviation for the name of the license. For example, 'CC0' or 'MIT'.
			- `usageType` - A list of enumerated values which describes the usage permissions for the release
				 - **openSource** - Open source
				 - **governmentWideReuse** - Government-wide reuse
				 - **exemptByLaw** - The sharing of the source code is restricted by law or regulation, including—but not limited to—patent or intellectual property law, the Export Asset Regulations, the International Traffic in Arms Regulation, and the Federal laws and regulations governing classified information
				 - **exemptByNationalSecurity** - The sharing of the source code would create an identifiable risk to the detriment of national security, confidentiality of Government information, or individual privacy
				 - **exemptByAgencySystem** - The sharing of the source code would create an identifiable risk to the stability, security, or integrity of the agency’s systems or personnel
				 - **exemptByAgencyMission** - The sharing of the source code would create an identifiable risk to agency mission, programs, or operations
				 - **exemptByCIO** - The CIO believes it is in the national interest to exempt sharing the source code
				 - **exemptByPolicyDate** - The release was created prior to the M-16-21 policy (August 8, 2016)"
	- `tags` - An array of keywords that will be helpful in discovering and searching for the release.
	- `contact` - Point of contact information for the release.
		 - **email**
		 - **name**
		 - **URL**
		 - **phone**
	- `status` - The development status of the release.  
		- **Ideation**
        	- **Development**
       		- **Alpha**
        	- **Beta**
       		- **Release Candidate**
        	- **Production**
         	- **Archival**
	- `vcs` - A lowercase string with the name of the version control system that is being used for the release. For example, 'git'.
	- `repositoryURL` - The URL of the public release repository for open source repositories. This field is not required for repositories that are only available as government-wide reuse or are closed (pursuant to one of the exemptions)."	
	- `languages` - An array of strings with the names of the programming languages in use on the release.
	- `laborHours` - An estimate of total labor hours spent by your organization/component across all versions of this release. This includes labor performed by federal employees and contractors.
	- `date` - A date object describing the release.
	
* Special/specified value/code/symbol: 
	- definition: eg, "N/A" indicates No/missing value.
	- explanation: eg, "999" indicates No/missing value.
* Terminology/dialect/jargon definition/explanation 
* Accuracy: resolution/interval
	

METHODOLOGY DESCRIPTION
-----------------------
* Summary of the theory/method/principle/techniques/algorithms: 
* Design/processing details:
	- Why to choose this method?
		- Advantages of this method over others: 
		- Any hypothesis/assumptions when using this method:
		- References: Links or citation of related documentation containing the method. 	
	- What is the procedure/experiment/model in this work:
	- Model/experiment/method setup:
		- list any figure or chart to show the workflow:
		- Step-by-step/procedure-by-procedure description:
		- Computational/experiment environment/condition:
			- hardware environment: eg, HPC clusters 
			- software environment: operating system, package, library, module, etc.  
		- Experiment/model/instrument configuration/settings:
		- Equipment/instrument/model info: 
			- source info:
			- manufacture info:
			- model number:
			- model version: 


DATA ANALYSIS
-------------
* The tool [software, model, script(s)] used for data analysis: 
* Data processing/cleaning:
	- Step-by-step description
	- Which variable is analyzed: 
	- What is the algorithm/method/technique/algorithm in this analysis?
	- code/scripts:
		- The license: 
		- OS/software configuration and version number: 
		- Hardware/software (OS) environment/condition:
	- Any quality-assurance procedures: Threshold/parameter setting, etc.
* Visualization: data --> figure/chart/graph
	- which figure is corresponding to which script and which dataset?


RESULTS/CONCLUSION AND DISCUSSION 
---------------------------------
* Results/conclusion and discussion: Draw a conclusion if there is any. 


SHARING & ACCESSING INFORMATION
-------------------------------
* License/restriction placed on the dataset: 
	- CCO:
	- CC By:
	- license.txt (for custom licensing considerations):
* Recommended citation for the dataset:
Author(Publication Year): Title of dataset (2-digit Version number) [General resource type]. Resource identifier. Publication agent.
	- 2-digit Version number: VX.X
		- the first digit: the version number for major changes of dataset
		- the second digit: the version number for minor changes of dataset
	- General resource type: Dataset, text, video, image, audio, collection, data file and code book, etc.
	- Status: unpublished, forthcoming, published
	- Resource identifier: DOI, web url, etc. 
	- Publication agent: the name of institution or the data center that publishes the resource.
* Links to the dataset: 
* Links to publications that cite/use the dataset:


RELATED MATERIALS
-----------------
List any additional related materials that was not included in "the current dataset package". For each related material,
* Type of material: may include dataset, article, code, presentation, collection, etc. 
* Status: forthcoming, available
* Link: 
* Citation: 
* Relationship to "the current dataset package": 
	- is supplement to 
	- is cited by
	- is the previous version of
	- is the new version of
	- ...


ADDITIONAL NOTES/COMMENTS
-------------------------
* Additional notes/comments: 
