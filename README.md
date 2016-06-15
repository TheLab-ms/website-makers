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




