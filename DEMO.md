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


<a name="setup" />
### Setup and Configuration ###

**TO IMPROVE**
Follow these steps to setup your environment for the demo.

1. Add step to log-in into the web site into both Chrome and IE. Click remember me.

1. Set up layout of IE and Chrome and VS.

	![Layout](Images/layout.png?raw=true)

1. Open Index.cshtml

<a name="Demo" />
## Demo ##
This demo is composed of the following segments:

1. [Design features](#segment1)
1. [Intellisense improvements](#segment2)

<a name="segment1" />
### Design features ###

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


1. Place the mouse over the light blue border, as shown in the following figure, and click.

	![Inspect Border](Images/inspect-border.png?raw=true)

	> **Speaking point:** Note that the element is highlighted in Visual Studio. Now we know the CSS class that we need to change.

1. Back Visual Studio, press **CTRL + ,**,  type _site.css_ and press **ENTER**.

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

1. Place the mouse over the question's title and click.

	![Edit Question](Images/edit-question.png?raw=true)

1. Update the original text with _What does it look like when a write a longer question?_.

	> **Speaking point:** Explain that the VS editor is updated and changes are saved automatically.

1. Back in Visual Studio, click the Browser Link **Refresh** button so IE is refreshed.
<a name="segment1" />

1. Close both browser windows and maximize Visual Studio.

### Design features ###

1. Type `<aud` inside the `<section>` element as shown in the following figure.

	![Audio Element](Images/audio-element.png?raw=true)

1. Press **TAB** twice. The following code will be added.

	````HTML
	<audio controls="controls">
		 <source src="file.mp3" type="audio/mp3" />
		 <source src="file.ogg" type="audio/ogg" />
	</audio>
	````

1. Delete the second line and update the source of the first one with the following link to the WebCampsTV Katana show
http://media.ch9.ms/ch9/11d8/604b8163-fad3-4f12-9607-b404201211d8/KatanaProject.mp3. The resulting code is shown below.

	````HTML
	<audio controls="controls">
		 <source src="http://media.ch9.ms/ch9/11d8/604b8163-fad3-4f12-9607-b404201211d8/KatanaProject.mp3" type="audio/mp3" />
	</audio>
	````

1. Add the following code at the bottom of the file.

	````JavaScript
	@section Scripts {
    <script>
        $(document).ready(function () {

        })
    </script>
	}
	````





