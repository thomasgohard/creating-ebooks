# Creating an ebook using EPUB 3.0

## Creating the ebook package

**Note:** A sample ebook package is provided in the `sample-ebook-package` folder. This sample package contains everything below.

1. Create a new folder. This will be the root of your new ebook. Everything in `this style` and any
	```xml
	code
	```
	 from here on is **case-sensitive**.
2. Inside the new folder, create:
	1. a file named `mimetype`,
	2. a folder named `META-INF`, and
	3. a folder named `EPUB`.
3. Inside the file `mimetype`, add the line `application/epub+zip`.
4. Inside the `META-INF` folder, create a file named `container.xml`.
5. Inside the file `container.xml`, add the following:
	```xml
	<?xml version="1.0" encoding="utf-8"?>
	<container xmlns="urn:oasis:names:tc:opendocument:xmlns:container" version="1.0">
		<rootfiles>
			<rootfile full-path="EPUB/content.opf" media-type="application/oebps-package+xml"/>
		</rootfiles>
	</container>
	```
6. Inside the `EPUB` folder, create a file named `content.opf`.
7. Inside the file `content.opf`, add the following:
	```xml
	<?xml version="1.0" encoding="utf-8"?>
	<package xmlns="http://www.idpf.org/2007/opf" version="3.0" unique-identifier="ebookID">
		<metadata xmlns:dc="http://purl.org/dc/elements/1.1/">
			<dc:identifier id="ebookID"></dc:identifier>
			<dc:title></dc:title>
			<dc:language></dc:language>
			<meta property="dcterms:modified"></meta>
		</metadata>
		<manifest>
			<item id="" href="" media-type=""/>
		</manifest>
		<spine>
			<itemref idref=""/>
		</spine>
	</package>
	```
