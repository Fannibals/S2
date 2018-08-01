### 1. Knowledge
+ **Data**: symbols, raw 
+ **Information**: data that are processed to be useful; provides answers to "who", "what",  
"where", and "when" questions
+ **Knowledge**: **Application** of data and information; answers **"how"** questions 

+ knowledge is for users, determinded by users

classify, group, clustering === transfer from data to information

We want to understand the relationsip between each data point == data model --- knowledge

### 2. KT
+ (a) Knowledge task vs. Concrete task
+ | | knowledge task | concrete task |
  | --- | ---| ---- |
  |input| irregular input | regular, structured, defined input|
  |correctness| no correct answer | has the correct answer|
      
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
  
### 4. "where to eat for dinner?"

### 5. regular expression
+ https://regexr.com/ website for exercising regex
+ (a) /[a-zA-Z]+/
  - One or More (english) letter charactes
    - +: >=1
    - ?: 0/1
    - *: >=0
  - take care of the difference between /[a-z]/ and /[a-z]+/
+ (b) /^[A-Za-z][a-z]*$/
  - starting from an english letter, and end with zero or more repeting small english letter
  - **333 or 369???**
+ (c) /p[aeiou]{,2}t/
  - Strings containing p and t, and there are up to 2 vowels in between
+ (d) /\s(\w+)\s\1/
  - space+(one or more words)+ space+space

### 6. 
+ (a) Match a price
  - \$[^0][0-9]+\.\d{0,2} for price
+ (b) Match an Australian telephone number
  - /061-[0-9]{9}/
+ (c) Remove HTML comments from a document
+ (d) Validate an email address
  - /^[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,4}$

