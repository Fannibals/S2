## KT-Week5: Web Search

### 1. Elements of a web search engine
+ Crawling
	- data to be searched needs to be gathered from the web
+ Parsing
	- tranlate datat into a canonical form
+ Indexing
	- data structures
+ querying

### 2. Crawling
+ getting the documents
+ whether exist

+ challenges:
	- no central index of URLs of interest
	- return same pages, never know when it has done ... 

+ Assumption:
	- if a web page is of interest, there will be a linke to it from another page.
+ Corollary:
	- given a suffiently rich set of starting points, every interesting site on the web will be reached everntually.
+ processes
	- Create a prioritised list L of URLs to visit 
	- A list V of URLs records visted info.
	- repeat forever
	
+ challenges
	- **L must be prioritsed to ensure that**
	- Every page is visited eventually.
	- Synonym URLs are disregarded.
	- Significant or dynamic pages are visited sufficiently frequently.
	- The crawler isn’t cycling indefinitely in a single web site (caught in a crawler trap).

### 3. Parsing
+ the tokens in the documents are extracted, then added to a data structure that records which documents contain which tokens.

#### 3.1 Page analysis
+ Page recognition
	- determining format of pages
+ Web pages are supposed to HTML and XML, but actually not
+ Scraping: ignore some compoenents like ad or comments

#### 3.2 Tokenisation
+ The aim of parsing is to reduce a web page, or a query, to a sequence of tokens.
+ Canonicalisation
	-  a process for converting data that has more than one possible representation into a "standard", "normal", or canonical form.
	
#### 3.3 Stemming
- the most significant form of canonicalization 
- Porter stemmer
	- sses -> ss 
#### 3.4 Zoing
- web search engines typically calculate weights for each of these zones,  
and compute similarities for documents by combining these results on the fly

#### 3.5 Indexing
+ Concept
	- with an index, query processing can be restricted to documents that contain at least one of the query terms.

	- INVERTED INDEX -- inverted lis
+ Search structure
	- for each distinct word t, the search structure contains:
		- A pointer to the srat of the corrsponding inverted list
		- A count ft of the documents containing t.
	- contains **vocabulary**
+ Inverted lists
	- identifier d of doc containing t
	- f(d,t) of t in d

