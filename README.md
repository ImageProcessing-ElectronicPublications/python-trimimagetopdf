trimimagetopdf.py

This script takes a cleaned image of the page: there is only one picture left on the page.  
The script cuts the picture and generates the PDF with the position of the picture on the page.  
That is, the resulting PDF contains a borderless drawing, but at the original location on the page.  
This facilitates the process of generating a PDF page with a heterogeneous content of rectangular segments.  
With a certain modification of the script, you can build a tailing generator RDF, but this is no longer a Unix-way.  

Depends: PIL, reportlab

Usage: trimimagetopdf.py [-h] [-a] [-d dpi] [-o outfile] [-v] imgname

Trim the image and creates a PDF with the same size

positional arguments:  
  imgname               image file name

optional arguments:  
  -h, --help            show this help message and exit  
  -a, --auto            autotrim, bw mode, default False  
  -d dpi, --dpi dpi     dpi for pdf output, default is 300  
  -o outfile, --outfile outfile    output pdf name, default imgname.pdf  
  -f format, --format format    format trim image, default png  
  -l left, --left left  use left, complit -ltwz*, default -1  
  -t top, --top top     use top, complit -ltwz*, default -1  
  -w width, --width width    use width, complit -ltwz*, default -1  
  -z height, --height height    use height, complit -ltwz*, default -1  
  -v, --version         show program's version number and exit  

*) The parameters -l,-t,-w,-z are used when normal trimming does not work and autotrim is not satisfactory.  
Parameter values can be selected manually, and can be borrowed from imagemagick:

convert -verbose -trim original.png trim.png

![Work](https://raw.githubusercontent.com/zvezdochiot/python-trimimagetopdf/master/sample.jpg)

2017  
zvezdochiot

