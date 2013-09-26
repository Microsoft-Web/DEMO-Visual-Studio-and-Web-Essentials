<a name="title" />
# Visual Studio and Web Essentials - Web Tooling #

---
<a name="Overview" />
## Overview ##

<a id="goals" />
### Goals ###
In this demo, you will see how to:

<a name="technologies" />
### Key Technologies ###

* [Web Essentials](http://vswebessentials.com/)
* [Visual Studio 2013](http://www.microsoft.com/visualstudio/esn/products/2013-editions)
* [Browser Link](http://blogs.msdn.com/b/webdev/archive/2013/09/10/what-is-new-in-browser-link-with-visual-studio-2013-rc.aspx)

<a name="setup" />
### Setup and Configuration ###

Follow these steps to setup your environment for the demo.

1. Open the **GeekQuiz.sln** solution located under **source/begin**.

1. If you don't have a user account, launch the application and register one.

1. Log-in in both Chrome and IE and select to be remembered. This will avoid having to enter the credentials during the demo.

1. Dock Visual Studio to the right and set up the layout of IE and Chrome as shown in the following figure.

	![Layout](Images/layout.png?raw=true)

1. In Visual Studio, open Index.cshtml in the editor.

<a name="Demo" />
## Demo ##
This demo is composed of the following segments:

1. [Browser Link and Web Essentials](#segment1)
1. [Intellisense improvements](#segment2)

<a name="segment1" />
### Browser Link and Web Essentials ###

1. Expand the browser menu in the Visual Studio toolbar and select **Browse With...**.

	![Browse With](Images/browse-with.png?raw=true)

1. Hold down **CTRL** and select **Google Chrome and Internet Explorer**.

	![Multiple Browsers](Images/multiple-browsers.png?raw=true)

1. Click **Set as Default** and click **Cancel**.

1. Press **CTRL + F5** to start debugging.

1. Replace the `<!-- TODO: add options here-->` comment with the following code snippet and press **TAB**.
	
	<!-- mark:1 -->
	````HTML
	button.btn-info.option{Answer $}*4
	````

1. Click the Browser Link **Refresh** button.

	![Refresh Browser Link](Images/refresh-browser-link.png?raw=true)

1. Click **Internet Explorer** (to set focus on it) and press **CTRL + ALT + I**.
	
	> **Speaking point:** Let's change the color of the border around the question.

1. Place the mouse over the light blue border and click on it, as shown in the following figure.

	![Inspect Border](Images/inspect-border.png?raw=true)

	> **Speaking point:** Note that the element and its children are highlighted in Visual Studio. Now we know which CSS class we need to change.

1. Back in Visual Studio, press **CTRL + ,**,  type _site.css_ and press **ENTER**.

	![Opening Site.css](Images/opening-sitecss.png?raw=true)

1. Scroll to the bottom of the file.

	![Bottom](Images/bottom.png?raw=true)

1. Click the light blue square that is part of the border property of the `.flip-container .front` class.

	![Color Picker](Images/color-picker.png?raw=true)

1. Expand the color picker by clicking the button with the chevrons, circled in the following figure.

	![Expand Color Picker](Images/expand-color-picker.png?raw=true)

1. Select a new color, close the color picker and press **CTRL + ALT + ENTER** to update the browsers.

	![Update Border](Images/update-border.png?raw=true)

1. Open the **Index.cshtml** editor.

1. Click **Google Chrome** (to set focus on it) and press **CTRL + ALT + D**.

1. Place the mouse over the question's title and click on it, as shown in the following figure.

	![Edit Question](Images/edit-question.png?raw=true)

1. Update the original text with _What does it look like when a write a longer question?_.

	> **Speaking point:** Explain that the VS editor is updated and changes are saved automatically.

1. Back in Visual Studio, click the Browser Link **Refresh** button so IE is refreshed.
<a name="segment1" />

1. Expand the **Error List** window and double-click the SEO related warning.

	![SEO Error](Images/seo-error.png?raw=true)
	
1. When asked if you would like to insert a `<meta>` tag, click **Yes**. The editor for **\_Layout.cshtml** is opened an the following code is automatically added.

	````HTML
	<meta name="description" content="The description of my page" />
	````
1. Change the value of the `content` attribute to _GeekQuiz_ and save the file.

### Snippets and Intellisense ###

1. Switch back to the **Index.cshtml** editor.

1. Add the following code inside the `<section>` element.

	````HTML
	<form>
		 <input type="text" id="name" />
	</form>
	````
1. Type `<label for="` inside the `<form>` element. As shown in the following figure, there is intellisense based on the Id of elements within the same valid scope (the `<form>`).

	![Id Intellisense](Images/id-intellisense.png?raw=true)

1. Delete the recently added `<form>` element and all its content.

1. Type `<aud` inside the `<section>` element as shown in the following figure.

	![Audio Element](Images/audio-element.png?raw=true)

	> **Note:** This demo segment adds an `<audio>` element to the page to showcase HTML 5 snippet support. This is meant to be a joke and the changes will be deleted, since we don't actually want to add audio to the site.

1. Press **TAB** twice. The following code will be added.

	````HTML
	<audio controls="controls">
		 <source src="file.mp3" type="audio/mp3" />
		 <source src="file.ogg" type="audio/ogg" />
	</audio>
	````

1. Delete the second line and update the source of the first one with the following link to the WebCampsTV Katana show:
http://media.ch9.ms/ch9/11d8/604b8163-fad3-4f12-9607-b404201211d8/KatanaProject.mp3. The resulting code is shown below.

	````HTML
	<audio controls="controls">
		 <source src="http://media.ch9.ms/ch9/11d8/604b8163-fad3-4f12-9607-b404201211d8/KatanaProject.mp3" type="audio/mp3" />
	</audio>
	````

1. Add the following code at the bottom of the file.

	````HTML
	@section Scripts {
		<script src="~/Scripts/init.js"></script>
	}
	````

1. In **Solution Explorer**, right-click the **Scripts** folder, expand the **Add** menu and select **JavaScript File**.

	![Adding Javascript File](Images/adding-javascript-file.png?raw=true)

1. Name the file _init_ and click **OK**.

1. Add the following code to the new JS file.
	
	<!-- mark:1-5 -->
	````JavaScript
	(function () {
		 $(document).ready(function () {
			  
		 });
	}());
	````

1. Type `document.getElementsByClassName("")` in the first line of the ready callback, as shown in the following figure.

	![ByClassName](Images/byclassname.png?raw=true)

1. Delete that line.

1. Type `var audioElements = document.getElementsByTagName("au")` in the first link of the ready callback, as shown in the following figure.

	![GetElementByTagName](Images/getelementbytagname.png?raw=true)

1. Select **"audio"** and press **Enter**. The result is shown in the following figure.

	![Retrieve Audio Elements](Images/retrieve-audio-elements.png?raw=true)

1. Add the following code below the line you just typed.
	
	<!-- mark:1-4 -->
	````JavaScript
	var len = audioElements.length;
	for (var i = 0; i < len; i++) {
		 audioElements[i].play();
	}	
	````

1. Click the Browser Link **Refresh** button. Once the pages are refreshed, audio will start playing.

1. Close both browser windows.

1. Delete the `<audio>` element and the `@section Scripts`.

	> **Speaking point:** We don't really want our site to have audio (it seems a bit 1990s), so let's get rid of these things we have added.





	





