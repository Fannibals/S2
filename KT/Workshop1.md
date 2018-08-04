### 1. Knowledge
+ **Data**: measurements(bit patterns for computers)
+ **Information**: processed data; patterns that are satisfied for given data
+ **Knowledge**: information interpretted with respect to a user's context to  
extend human understanding in a given area(where we have data)

+ knowledge is for users, determinded by users

classify, group, clustering === transfer from data to information

We want to understand the relationsip between each data point == data model --- knowledge

### 2. KT
+ (a) Knowledge task vs. Concrete task
+ | | knowledge task | concrete task |
  | --- | ---| ---- |
  |input| irregular input | regular, structured, defined input|
  |correctness| no correct answer | has the correct answer|
+ **Concrete tasks:** 
Mechanically processing data to an unambiguous solution;  
Limited contribution to human understanding
+ **Knowledge tasks:**  
Data is unreliable or the outcome is ill-defined(不明确的) (usually both);  
Computers mediate between the user and the data, where context (for the user) is critical;  
Enhance human understanding
      
+ (b) Knowledge tasks or concrete tasks
  - i. Multiplying two floating-point numbers in base 16 &nbsp;&nbsp;&nbsp;  **concrete**
  - ii. Playing a competitive game of naughts-and-crosses   &nbsp;&nbsp;&nbsp;**concrete**
  - iii. Playing a competitive game of go  &nbsp;&nbsp;&nbsp; **knowledge**
  - iv. Playing a competitive game of tennis    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**knowledge**
  - v. Calculating the trajectory of a thrown book    &nbsp;&nbsp;&nbsp;**concrete**
  - vi. Selecting appropriate counter-measures after someone has thrown a book at you &nbsp;&nbsp;&nbsp;**concrete**
  - vii. Selecting a book that a given person will enjoy reading    &nbsp;&nbsp;&nbsp;**knowledge**
  - viii. Translating a program written in C into Java  &nbsp;&nbsp;&nbsp;**concrete**
  - ix. Translating a document written in Japanese into English   &nbsp;&nbsp;&nbsp;**knowledge**
  
### 3. Structured/Semi-structured/Unstructured Data
+ **Unstructured data**
  - Data without regular, decomposable internal structure (cannot understanded by computers)
  - examples: blogs(structured by bloggers), MP3 files, JPEG files
+ **Structured data**
  - Data which strictly conforms to a schema
  - traditional DBs
  - examples: ABN lookup, library catalogues
+ **Semi-structured data**
  - some parts are structured 
  - examples: Wikipedia entries, Bibtex records, bibliography
  
+ In practice, all data is semi-structured: 
  - without a schema, a bit pattern is uninterpretable;
  - without context, a measurement is just a number, etc. 
  - Even “structured” data typically contains inaccessible information: consider a database with a name field. Name of what? A
person (given name? surname? both?)? An organisation? A city? A street? We need context to disambiguate.
  
### 4. "where to eat for dinner?"

### 5. regular expression
+ https://regexr.com/ website for exercising regex
+ (a) /[a-zA-Z]+/
  - One or More letters of the Latin alphabet, e.g. hello, world
    - +: >=1
    - ?: 0/1
    - *: >=0
  - take care of the difference between /[a-z]/ and /[a-z]+/
+ (b) /^[A-Za-z][a-z]*$/  
  - Notes: **only match one String**
  - starting from an english letter, and end with zero or more repeting small english letter
  - word or Alphabet
+ (c) /p[aeiou]{,2}t/
  - Notes; it will match all pxxt
  - Strings containing p and t, and there are up to 2 vowels in between
+ (d) /\s(\w+)\s\1/
  - space+(one or more words)+ space+space

### 6. 
+ (a) Match a price
  - ~\$[^0][0-9]+\.\d{0,2} for price~
  - /\$(0|[1-9][0-9]*)(\.\d{1,2})?/
+ (b) Match an Australian telephone number
  - ~/061-[0-9]{9}/~
  - /(\+61|0)\d([ -]?\d){8}/
+ (c) Remove HTML comments from a document
  - s/\<![ \r\n\t]*(--([^\-]|[\r\n]|-[^\-])*--[ \r\n\t]*)\>//g
+ (d) Validate an email address
  - ~/^[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,4}$~
  - /^(\w|-)+(\.(\w|-)+)*@(\w|-)+(\.(\w|-)+)*(\.[a-z]{2,4})$/

