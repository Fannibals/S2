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
	- 
