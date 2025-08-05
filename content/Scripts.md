
>[!script]- get_lbs.py
>**Input:** List of DOIs
>**Output:** a bib file with bibliographies of all papers which prove a DS lower bound and cite the papers whose DOIs are in the input list. 
>- filter applied to the above function to only include DS lower bounds in the output based on some key words. 

>[!script]- get_citations.py
>**Input:** List of DOIs
>**Output:** a bib file with bibliographies of all the papers which cites the papers whose DOIs are in the input list.
>- no duplicate DOIs.  	

>[!script]- get_folder_dois.py
>**Input:** A folder name in Zotero
>**Output:** a text file with the DOIs of the bib items in the input folder in each line. 
	  
>[!script]- update_zotero_dois.py
>**Input:** A folder name in Zotero
**Output:** no output. But modfies the metadata of the elements in the input folder to complete the incomplete metadata using Semantic Scholar API.  
	  
>[!script]- fetch_dois.py
**Input:** A list of titles of papers.
**Output:** prints the DOIs of the Papers from input list.
>- uses CrossRef API.
>- *very slow* makes each query seperately to the API with a time delay.  

>[!script]- update_zotero_dois.py
>**Input:**
>**Output:**

>[!script]- tag_duplicates.py
>**Input:**
>**Output:**

>[!script]- Splitter.py
>**Input:**
>**Output:**

>[!script]- tagger.py
>**Input:** name of a folder in zotero.
>**Output:** a bib file where tags are applied appropriately from a collection of tags. 
>- The same tags are applied to zotero elements as well.  

>[!script]- folder_split.py
>**Input:**
>**Output:**

>[!script]- merge_citations.py
>**Input:** A target folder in zotero, a list of DOIs.  
>**Output:** The union of the citations of all the DOIs is merged with the target folder so that there are no duplicates. 

# Work flow

Step 1: Given a zotero folder x as input, *get_folder_dois.py* outputs a text file named x_DOIs.txt which consists of DOIs and Titles of the bibitems from the folder x in the format *"DOI | Title"*
- ensure books are not included.

Step 2: *get_citations.py* takes that text file with DOIs as input and collects the union of all the papers that some paper in the folder x using the text file generated above and ouputs the bibliography into bib file named x_citations.bib.  

Step 3: Splitter splits the x_citations.bib into 3 bib files: x_invalid_references.bib, x_lbs.bib and x_non_lbs.bib
- x_invalid_references.bib contains items which do not have either title, Abstract or DOI. 
- x_lbs.bib contains all papers which have a valid Title, Abstract, DOI and that has certain key words ("lower bound")
- x_non_lbs.bib contains papers which do not contain the key words. 

Step 4: **annotate.py**
	Pass through a LLM or NLP algorithm to apply a better filter and also to obtain data like Problems, Lower bound Technique, Bounds , Static/Dynamic. 


- Start with a seed folder
- Get all the metadata possible by running get_metadata.py on the sedd folder. 

Once the seed folder has good metadata, 
- Run get_citations.py - to get all the papers that cite the seed papers.
  - [ ] Make sure get_citations checks avoids duplicates by only adding when the current paper is not in the seed folder.  
- Run get_references.py - to get all the papers that are cited by the seed papers.
	- [ ] Make sure get references avoids duplicates. 

- Run get_metadata.py for both these files using CrossRef if possible.

- Run tagger.py to get all the tags 