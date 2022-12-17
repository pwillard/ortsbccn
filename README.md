# Ebook-ORTSBCCN
Open Rails Train Simulator Content Creation Notebook


AsciiDoctor Source code, license CC-BY-SA-4.0 

At this stage this is a lot of random notes strung together to look like something... but with a whole lot of "not finished" going on.  
I just wanted to see what what a Content Creation Notebok for OPEN RAILS could look like.


# To BUILD this document from AsciiDoctor source you need:

## Install Ruby

Have the RUBY programming language installed. Latest version is 2.5 as of this writing.   https://rubyinstaller.org/

## Install AsciiDoctor - pre-release

Install AsciiDoctor-PDF with the following command: `gem install asciidoctor-pdf --pre`

## Install Rouge syntax highlighter

Install Rouge with the following command: `gem install rouge`

## Install AsciiDoctor Diagram 

Install the diagram tool with the following command: `gem install asciidoctor-diagram`

## Assembling the document

I use the following command to create the PDF document output:

`call asciidoctor-pdf --trace -r asciidoctor-diagram -a pdf-style=resources/pdfstyles/screen-theme.yml -a pdf-fontsdir=fonts book.adoc`

NOTE: ASCIIDOCTOR formatting code is ALMOST github compatible...  so GITHUB tries to render it... (It just doesn't really work)


Script
----
@echo Started: %date% %time%
call asciidoctor-pdf -a pdf-style=resources/pdfstyles/screen-theme.yml -a pdf-fontsdir=fonts book.adoc -o ORTS-CC-Notebook.pdf
@echo Ended: %date% %time% 
rem asciidoctor-pdf  book.adoc
if exist *.png (
    rm *.png
)


----
