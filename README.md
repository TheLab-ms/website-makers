# website-makers
This repo contains the old wiki content which will now live in the /makers area of thelab.ms website

## Initial content
The initial content here has been pulled from our Mediawiki site and then converted to markdown using pandoc

Here is some information about the pandoc command used:
'''
pandoc -f mediawiki -t markdown -o filename.md filename.wiki
-f = from format
-t = to format
-o filename = output file
filename = input file
'''

The wiki and initial markdown conversion files are kept in a convert directory for now that will be ignored by pelican.
The convert directory may be removed at some point in the future.

Once the markdown files are created they must be modified to fix all the links.
The fully corrected markdown file ready for pelican use is then moved to the pages directory.

### Conversion Note

Since pandoc did a crappy job all the pages needed to be manually updated.
So, please be on the lookout for any typos or format issues that were missed.

## Content variables
Content files can contain a number of different variables to be parsed by pelican.

While you should not have to directly edit these most times you might have to use the variables for pathing relative to server root.

The configuration file sets what the site url will be which can change depending upon the content.  
For example the main site content will all be starting at / like /images or http://thelab.ms/images but this makers area will be starting with /makers/ like /makers/images or http://thelab.ms/makers/images 

So in order to make sure internal links work properly you should use the {filename} variable on content pages.

Do not simply create an internal link to content such as href="/images/abc.gif" and expect it to work!  Use the proper variable format of href="{filename}/images/abc.gif" and it will work fine.

## Highlighted Projects

We have some project pages in the /makers/ content that have been highlighted by placing them in thier own directory which will be linked from web root (e.g. /makers/tap/ is also /tap/).  

It is important to note that the content for these highlighted projects is located in the website-makers repository and NOT in the website-content repository.

It is also important that internal links are still referenced with the {filename} directive listed above.
This will allow the pages and all thier internal links to images etc. to work from both locations where an absolute path might break in one of the locations.


See the website-pelican repository README.md file for more details.

