Installation
===============

At it's foundation, the Processing.js bundle ties together language patterns from the Javascript bundle that ships with TextMate and the Processing bundle created for the original Java implementation of Processing. Without both of these installed, the Processing.js bundle won't function properly. Check your Bundles menu to see that both are present and if either or both are missing they can be acquired via SVN at the following locations:

	Javascript Bundle	http://svn.textmate.org/trunk/Bundles/JavaScript.tmbundle/
	Processing Bundle	http://svn.textmate.org/trunk/Bundles/Processing.tmbundle/
	
Preview
===============

Preview is meant to allow the testing of code with as little overhead as possible by using the following behavior when run:

- Documents containing only Processing.js code will automatically be wrapped with HTML including processing.js and init.js as well as a canvas element sized to the dimensions stated in the JS code. Previewing these types of documents will not invoke a save action enabling code changes to be made and previewed before being saved.
- Documents containing embedded Processing.js code, wrapped in HTML, will automatically be saved before preview.
- Untitled documents that have not been saved can be previewed just the same as saved documents.

When automatically wrapping Processing.js code, Preview currently uses the official github links to include processing.js and init.js. While this affords compatibility, loading those remote files for each preview can be unnecessarily slow. To speed up performance, open the Processing.js bundle in the bundle editor by going to Bundles > Bundle Editor > Show Bundle Editor and clicking on "Preview" under the Processing.js title. Change the following two lines so that they point to local copies of init.js and processing.js respectively:

	LINE 12| <script language="javascript" src="http://github.com/jeresig/processing-js/raw/master/examples/init.js"></script>
    LINE 13| <script language="javascript" src="http://github.com/jeresig/processing-js/raw/master/processing.min.js"></script>

Future versions of this bundle will accommodate this change in a more user-friendly manner.