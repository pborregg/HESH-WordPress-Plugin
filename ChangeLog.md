# Changelog

## 2.2.4
* fixed bug: Allow Multiple Instances of CodeMirror on a page #71
* fixed bug: js error when custom post type does not support 'editor' feature #62

## 2.2.3
* A patch for WP 4.9. No more double editors in theme/plugin editors.

## 2.2.2
* fixed bug: github updater in production issue #52
* updated Codemirror to latest release version

## 2.2.1
* fixed bug: editor was not stopping when switching between visual editor and text. reverted fix for #50

## 2.2.0
* added search & replace with dialog
* added highlighing options
* added auto-close tags and brackets option
* added code-folding option
* added scrollbars option
* added keyMap options
* added _Default_ and _None_ themes
* fixed bug: made tab management agnostic to tab count and names - #50

## 2.1.0
* added search #31
* add highlighting for `<!--nextpage-->` #15 
* fixed bug: #51 Theme and Plugin Editor not working

## 2.0.1
* fixed bug: #29 esc key weirdness
* fixed bug: #30 don't steal editor focus from title on _'Add New Post'_
* fixed bug: #43 scrollbar appears in middle of text editor
* fixed bug: #45 toolbar can be too big

## 2.0.0
* The HESH editor now has parity with the standard WP text editor, including compatibility with the _'Enable full-height editor and distraction-free functionality'_ (The last option located under '_Screen Options_' tab at the top of the page).
	* Behavior with full _'Enable full-height editor and distraction-free functionality' __enabled__:
		* The fullscreen button enables '_distraction-free_' mode. All other controls on the screen fade away.
		* The editor has a dynamic height based on its text content. This is the '_full height editor_'. The editor still has a min-height of 300px.
		* The editor toolbar fixes to the top of the screen while scrolling down the editor's length.
	* Behavior with full _'Enable full-height editor and distraction-free functionality' __disabled__:
		* The fullscreen button puts the editor into the traditional fullscreen mode.
		* The editor has a '_content resize handle_' in the bottom right. Dragging this will resize the editor's height with a min-height of 70px.
		* The editor content vertically scrolls within the resizable height.
* Syntax highlighting on Theme and Plugin Editor pages.
	* Dynamically picks the right file type for highlighting.
* Fixed bug: native wp editor buttons work on content. No longer overwrites with emulating buttons
* __Settings:__
	* added an extendable settings panel
	* saves settings to WordPress user profile
	* added more text customization settings
* Fixed some release bugs in [issue 24](https://github.com/mukhortov/HESH-WordPress-Plugin/issues/24)

## 1.7.2
* fixed bug: pre v5.4 php was causing an error - `func_that_returns_array()['index']` syntax is [not allowed](http://php.net/manual/en/language.types.array.php#example-105)
* fixed bug: CodeMirror not initializing properly when new user tries to edit post for the first time
* fixed bug: CodeMirror no longer trying to load on "All Posts" and "All Pages"
* fixed bug: Font and theme were reset to default when switching to the visual editor and back

## 1.7.1
* fixed bug: return key would create two new lines and ignore indent
* fixed bug: wp native "Add Media" button was not working
* added version string to .css and .js resources for cache-busting purposes

## 1.7.0
* Ctrl-S / Cmd-S saving will now select "Save Draft" if the post has not been published yet
* Switched to an [npm](https://www.npmjs.com/) and [grunt.js](http://gruntjs.com/) based build so new versions of CodeMirror can be applied easier
* Updated CodeMirror to its latest version
* Fixed FireFox bug: `<select>` dropdown would not display due to `::active` state `transform` property
* Fixed bug: toolbar covering text at small screen width
* Fixed bug: `switchEditors is undefined`
* Updated Css for wp 4.5
* Added all available CodeMirror themes
* Added syntax highlighting:
	- for WordPress shortcodes
	- for `<!--more-->` tags and their variants
	- _NEW_ CodeMirror modes: `shortcode.js` & `wordpresspost.js`
* Now calling `hesh.js` in an anonymous wrapper so it won't pollute the global namespace
* Now initializing `hesh.js` in an async compliant way
* Refactored php to enqueue javascript in the WordPress friendly way
* Tested with WordPress 4.5.2
* Tested in all modern desktop browsers on OSX and Windows 10

## 1.6.9
* Fixed issues with switching editor modes in WP 4.3

## 1.6.7
* Added paragraph tag button, it's visible only when the visual editor is disabled
* Added minimum editor window height for the full-height mode

## 1.6.6
* Added minimum editor window height for the full-height mode

## 1.6.5
* Fixes for full-height mode
* Fixed the issue with a hidden first line on smaller screens

## 1.6.4
* Fixed the issue with a hidden first line on smaller screens

##1.6.3
* Fixed editor window height and resize handler
* "headers already sent" issue

## 1.6.2
* Compatibility with WP 4.0
* Fixed fullscreen mode

## 1.6.0
* You can change font size in the editor
* Fixed issue with restoring cursor position
* Updated CodeMirror library
* Some minor improvements

## 1.5.0
* Updated CodeMirror library
* Some minor improvements

## 1.4.8
* Add Link button now works with page selector window
* Some minor improvements

## 1.4.7
* You can now select Light or Dark editor color theme

## 1.4.6
* Fixed issue when "Add Media" button stopped working
* Fixed editor resize bug in Visual mode.

## 1.4.5
* Bug fixing

## 1.4.4
* Add Media button now works correctly in Text mode
* Fixed jumping cursor issue when ‘:’, '{', '}' keys are pressed

## 1.4.3
* Fixed jumping cursor issue when ‘/’ key is pressed.

## 1.4.2
* Fixed a focus bug

## 1.4.1
* Toggle fullscreen mode with F11/Esc hotkeys
* Publish Post/Page hotkeys Ctrl + S / Cmd + S
* Fixed some bugs for IE 8
* Added development files to the zip bundle

## 1.4.0
* New fullscreen mode
* Remembers tab state
* Editor resize handler
* Code refactoring and minification for better loading performance

## 1.3.2
* Updated CodeMirror library
* Increased loading performance
* Match brackets

## 1.3.0
* CodeMirror library updated to version 3.02
* Added quick-tags toolbar buttons
* Preserve the scroll position after update or page reload

## 1.2.1
* vertical resize for the editing box (works on FireFox, Chrome, Safari).
* not working buttons/tags was hidden

## 1.2
Bug fix:
* plugin does not work in new post/page.

## 1.1
Bug fix (thanks to collinprice):
* when user has the visual editor disabled this plugin does not show up.

## 1.0
Initial release.