The auto-table-extract system is capable of identifying tables within PDF documents and extracting the information from it. Table detection is the process of identifying tables from a document, extracting the cells contained in a table. The auto-table-extract system consists of three main modules: 1) Document conversion 2) Layout Analysis 3) Table detection and extraction.
The input to the auto-table-extract system is a PDF document. This PDF document can be scanned or searchable (selectable text). The ocrmypdf, which is a Tesseract based OCR, is used for document conversion from scanned to searchable PDF. Using PDFMiner, Layout analysis is applied over the PDF document. PDFMiner can determine coordinates of lines, text boxes, figures, characters, and rectangles. The auto-table-extract system uses two methods to identify and extract tables. The extracted data of the table is dumped into an excel sheet. The two methods used for identification and extraction are 1) Table_with_Border ( For tables with fully recognizable borders) 2) Table_without_Border (For partially bordered or borderless tables ). The Table_with_Border method is used to determine the tables with the help of coordinates of text lines, characters, and text boxes provided by the PDFMiner. The Table_without_Border method uses the clustering method and coordinates of the text line to determine the table and extract its contents.
Further, a Pandas DataFrame consisting of extracted data is created, which is used to make the excel sheet containing the data. The output of the auto-table-extract system is an Excel document with the table’s information extracted from the PDF. In the following sections, we describe the two methods called Table_with_Border and Table_without_Border built into the system to perform automatic table detection and extraction. 
