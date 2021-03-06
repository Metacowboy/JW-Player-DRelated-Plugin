D-Related plugin allows you to load in list of the related clips in XML format and display them to the audience when the movie is complete or paused. Plugin's look and proportsions are fully skinnable.

How to use?

To use the plugin in your player, add the name d-related to the plugins flashvar.

To display correctly, the plugin needs path to the related clips XML. This is set with the flashvar called drelated.xmlpath.

XML contains the <title> tag and <video> items. <title> element contains the explaining text displayed in the plugins header (eg. Related videos:)

<videolist>
	<title>Related videos:</title>
	<video>
 		<title> - name of the clip to display in the plugin</title>
		<thumb> - link to the thumbnail</thumb>
		<url> - link to guide the viewer to when the clip is clicked</url>
		<file> - The url to the file to play if the d-related plugin is in dynamic mode</file>
	</video>
</videolist>

Your can modify the plugin by setting the following flashvars:


* drelated.xmlpath
The URL of the related XML

* drelated.position
By default the plugin positions itself to the top of your player, but can also be positioned bottom or center by setting the dposition flashvar to 'bottom' or 'center'

* drelated.skin
Plugin is fully skinnable and is set up from the following elements:

	Bg - the large semitransparent layer that's stretched to exact same size and video
	Cover - the smaller semitransparent layer to bring out the thumbrow and controls;
	shuffle_left, shuffle_right - buttons to scroll the thumbrow to the left or to the right
	infoelement - MovieClip containing textfield with the title for the clips shown
	template - Videoitem 

To set up your own skin, place the bits and pieces to the skin file's stage and give the movieclips instancenames according to the listing above.

* drelated.target
where should the new clip open - in a new window or same window. Default is '_self' 

* drelated.height_offset
Pixel offset for the top of the container background

* drelated.dynamic
Will load the clicked video into the current player.  You must pass in <file> element through the related.xml file.


Notes:


The container should now correctly resize itself when toggling fullscreen, or resizing the player through some other means.
