# Branch Presets

Ever stored rendering component data source items under a page? For example:

	/sitecore/content/Page
	/sitecore/content/Page/Datasources/ComponentDataSourceItem

It's a good practice and it seems to work quite well for page specific components.

But have you ever wished branch templates understood that in a logical fashion? What if this:

	/sitecore/templates/branches/Foo/$name
	/sitecore/templates/branches/Foo/$name/Datasources/ComponentDataSourceItem

...expanded out to have the branch create the hierarchy __and__ re-link the layout details on the instiantiated branch item to point to the right child data source item?

Doing this lets you use branch templates to create preset rendering hierarchies, __including__ page specific data source items.

Sound good? Well you've found the right place to get the code to do just that. This requires Sitecore 8 or above with the pipeline-based item provider to operate.