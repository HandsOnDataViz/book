When you create a data visualization with a web tool (such as BatchGeo or Google Fusion Tables), a common goal is to make the interactive element appear inside a second web page (such as your WordPress.org site, or a website that belongs to the partner organization). Rather than simply creating a link to your data viz, a more elegant solution is to embed it inside the second site using an iFrame, a simple HTML code that allows one web page to be displayed within a second web page. (Read more about the <a href="http://www.w3schools.com/tags/tag_iframe.asp" target="_blank">ifram</a><a href="http://www.w3schools.com/tags/tag_iframe.asp" target="_blank">e tag at W3Schools</a>.)

In WordPress.org sites like this one, the <a href="http://wordpress.org/plugins/iframe/" target="_blank">iframe plugin</a> allows authors to embed an external web element inside a post/page using a simple "short code" in square brackets. (I have already activated the plugin on Trinity College WordPress.org sites for me and my students, but you may need to install and/or activate it on your WordPress.org site.) Without the plugin, WordPress usually will "strip out" iframe codes for all users except the site administrator. Beware that inserting an iframe will NOT work for most WordPress.com sites. If your website runs on a different platform, ask your provider if it supports iframe tags.

<a href="http://commons.trincoll.edu/jackdougherty/files/2012/11/PluginActiveIFrame.jpg"><img alt="" src="http://commons.trincoll.edu/jackdougherty/files/2012/11/PluginActiveIFrame.jpg" width="360" height="86" /></a>

Go to WordPress.org and create a new post/page. In the editor, switch from the Visual to the Text tab, which allows users to insert and modify HMTL code. Paste the long string that you copied from the step above. Add square brackets at beginning and end of the iframe tag, and edit a few characters to match this format (called a "shortcode"), then publish to view your post. See specific examples below.

If you're hosting your data visualization on a live website (such as <a href="http://epress.trincoll.edu/dataviz/chapter/host-html-github/" target="_blank">GitHub Pages</a>), copy the web address, like this:

<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/02/IframeCopyURL.jpg"><img class="aligncenter size-full wp-image-255" alt="IframeCopyURL" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/02/IframeCopyURL.jpg" width="600" height="185" /></a>

On WordPress.org site with the iframe plugin installed, go to the post/page text editor (not visual editor), then type in a simple iframe shortcode with square brackets, and paste the web address into the "src=" (source equals) section,  like this:

<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/02/iframePasteURL.jpg"><img class="aligncenter size-full wp-image-256" alt="iframePasteURL" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/02/iframePasteURL.jpg" width="589" height="219" /></a>

When you preview or publish the WordPress post/page, your interactive data visualization from the first website will appear embedded (or nested) within this secondary website, like the example below:

[iframe src="http://jackdougherty.github.io/tableau-public-sample/"]

If you're using BatchGeo or similar tools, look for "Embed code" and copy it, like this:

<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/02/Embed-BatchGeo.png"><img class="aligncenter size-full wp-image-47" alt="Embed-BatchGeo" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/02/Embed-BatchGeo.png" width="436" height="82" /></a>

Then paste the BatchGeo iframe embed code  into a WordPress.org post/page, with the iframe plugin installed, and modify it like this:

<a href="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/02/BatchGeoIFrameEmbed.png"><img class="aligncenter size-full wp-image-48" alt="BatchGeoIFrameEmbed" src="http://epress.trincoll.edu/dataviz/wp-content/uploads/sites/11/2014/02/BatchGeoIFrameEmbed.png" width="559" height="399" /></a>

If you're using Google Fusion Tables, modify your Sharing Settings to make your data visualization Public on the Web or to Anyone with the link. Then Publish your data visualization, and modify the width and height to fit the space allowed by the WordPress theme. (For most WordPress.org sites, 600 x 400 pixels looks best.) Copy the long string of code from the "Paste HTML to embed" field, like this:

<a href="http://commons.trincoll.edu/jackdougherty/files/2013/10/GFT_PublishHTML.png"><img alt="GFT_PublishHTML" src="http://commons.trincoll.edu/jackdougherty/files/2013/10/GFT_PublishHTML.png" width="436" height="306" /></a>

Then paste your Google Fusion Tables embed iframe code into a WordPress.org post/page, with the iframe plugin installed, and modify the shortcode, like this:

<a href="http://commons.trincoll.edu/jackdougherty/files/2013/10/GFT_iFrameEmbedCode.png"><img alt="GFT_iFrameEmbedCode" src="http://commons.trincoll.edu/jackdougherty/files/2013/10/GFT_iFrameEmbedCode.png" width="599" height="449" /></a>

Preview or publish your page/post, and the dataviz from the first site should appear in your second web page. Learn more about iFrame HTML tags and options to modify them at <a href="http://www.w3schools.com/html/html_iframe.asp" target="_blank">W3 schools</a>.
