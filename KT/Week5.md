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

### 4. Indexing
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
	- transposition from (d,t) to (t,d)
	
### 5. Querying
#### Boolean Querying
+ Boolean Querying using a **TDM** is ???

+ Boolean Querying using an **inverted index**
	- ignore within-document frequencies
+ For Conjunctive Queries (all with AND)
	- from the shorest to the longest
#### Ranked Querying
+ still: **TF + IDF + length**

##### Steps
+ 1. Allocate an **accumulator A(d)** for each doc d, set **A(d) to 0**
	- for store the dot product
+ 2. for each **query term t**
	- 1) Calculate **W(q,t)** adn fetch the inverted list for t
	- 2) For each **entry in the inverted list**, the pair <d(t),f(d,t)>
		- Calculate W(d,t) and **Increment the A(d): Ad ← Ad + wq,t × wd,t
+ 3. Read the array of W(d) values and for each A(d)>0,  
	Normalise by the document length Ad ← Ad /Wd .
+ 4. 4 Identify the r **greatest Ad values** and return the corresponding documents.	
	
#### Accumulator costs
+ In order to reduce costs:
+ **Limiting** approach
	- A simple mechanism is to impose a limit L on the number of accumulators. 
	-  term t is ordered by decreasing W(q,t) --- MOST imformative first
+ **thresholding** approach
	- threshold S for dot product
	- Only create an accumulator A(d) when dot product > S
	- only when wq,t × wd,t > thresholding S
+ Querying costs 
	- Disk space, Memory space, CPU time, Disk traffic are should be considered 

### Add-ons
+ Phrase queries **???**
	- thre main strategies for phrase query evaluation:
		- Process queries as bag-of-words
		- Add word positions to the index entries
		- Use some form of phrase index or word-pair index
+ Link Analysis
	- The two major link analysis algorithms are HITS (hyperlinked-induced
topic search, not discussed in this subject) and PageRank.
+ Pagerank
	- 如果一个网页被很多其他网页链接到的话说明这个网页比较重要，也就是PageRank值会相对较高, 如果一个PageRank值很高的网页链接到一个其他的网页，那么被链接到的网页的PageRank值会相应地因此而提高
	- each web document has a fixed number of credits associated with it, a portion of which it redistributes to documents it links to; in turn, it receives credits from pages that point to it.
	- https://www.youtube.com/watch?v=P8Kt6Abq_rM

	
	
