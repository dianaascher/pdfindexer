##pdfindexer
==========

### Purpose
Index and search PDF sources (files and URLs) using Apache Lucene and PDFBox

### Project
* Open Source hosted at https://github.com/dianaascher/pdfindexer
* License based on license of libraries used (see [pom.xml](https://github.com/dianaascher/pdfindexer/pom.xml))
* Maven based Java project including JUnit 4 tests.

### How to build
* git clone https://github.com/dianaascher/pdfindexer
* cd pdfindexer
* mvn install

# Examples
see [test folder](https://github.com/dianaascher/pdfindexer/tree/master/test) for example input and results

### Nudge
* Source: [Nudge PDF](https://github.com/dianaascher/pdfindexer/test/pdfsource1/Nudge.pdf "Click to open PDF source")
* Keywords: https://github.com/dianaascher/pdfindexer/test/searchwords.txt
* Result:  [Nudge PDF Index](https://github.com/dianaascher/pdfindexer/test/pdfindex.html "Click to open html source")

    java -jar target/com.bitplan.pdfindex-0.0.1.jar --sourceFileList test/pdffiles.lst --idxfile test/index2 --outputfile test/html/pdfindex.html --searchWordList test/searchwords.txt --root test/ 
     resulting html file is in test/html/pdfindex.html

resulting html file is in test/html/pdfindex.html

### Nudge project 
PDF text from Nudge
* Source: http://dianaascher.com/nudge.pdf
* Keywords: searchwords.txt
* Result: [Nudge PDF Index](http://dianaascher.com/wp-content/uploads/2013/08/Nudge.pdf "Click to open HTML source") 

# Usage
		Pdfindexer Version: 0.0.3
		
		 github: https://github.com/dianaascher/pdfindexer.git
		
		  usage: java com.bitplan.pdfindexer.Pdfindexer
		 --title VAL                  : title to be used in html result
		 -d (--debug)                 : debug
		                                create additional debug output if this switch
		                                is used
     -e (--autoescape)            : autoescape blanks
			                              set to off if you'd like to use lucene query
			                              syntax		                                
		 -f (--src) VAL               : source url, directory/or file
		 -h (--help)                  : help
		                                show this usage
		 -i (--idxfile) VAL           : index file
		 -k (--keyWords) VAL          : search
		                                comma separated list of keywords to search
		 -l (--sourceFileList) VAL    : path to ascii-file with source urls,directories
		                                or file names
		                                one url/file/directory may be specified by line
		 -m (--maxHits) N             : maximum number of hits per keyword
		 -o (--outputfile) VAL        : (html) output file
		                                the output file will contain the search result
		                                with links to the pages in the pdf files that
		                                haven been searched
		 -p (--templatePath) VAL      : path to Freemarker template file(s) to be used
		                                to format the output
		 -r (--root) VAL              : root
		                                if a  root is specified the paths in the
		                                sourceFileList and in the output will be
		                                considered relative to this root path
		 -s (--silent)                : stay silent
		                                do not create any output on System.out if this
		                                switch is used
		 -t (--templateName) VAL      : name of Freemarker template to be used
		 -v (--version)               : showVersion
		                                show current version if this switch is used
		 -w (--searchKeyWordList) VAL : file with search words
