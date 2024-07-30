https://www.youtube.com/watch?v=heXQnM99oAI&t=5547s


its more than a text editor. intellisense. 
aesthetics. 
over 100 tips and tricks. 

10x developer. 

workflows
extensions
plugins.
Most productive editor. 
Make the VS code work for you. 


Productive VS code, 

-> control panel, ctrl+shift + P
-> file navigation ctrl + p

commit the code to git hub, 


you can push code to github using the command pallete. 
you can literally do everything on vScode editor, no need of terminal at all. 


Getting started, 
customize your setup


UI of VS code, 
Interface, 
down at the bottom is status bar, purple color
left, activity bar: explorer, Search, Git Icon, Debug and Extension. 


command pallete, 
used very widely. 

Install themes, dark theme preferably. 
material icon theme. 
you can research for more extensions on your own. 


Fonts, 
ctrl shift p, settings UI format. 
search for font family, and update the font with, 
'Cascadia Code',  Consolas, 'Courier New', monospace

font size 16
line height  26
ligature, in Json file, make it true. 
mouse wheel zoom for font, make this true. 

other additional five settings, 
tab size, 2
rulers: 
"editor.rulers": [
 80
]
render indent guides, Indentation lines display. 
word wrap, turn on
cursor blinking, smooth


get to know VS code, 
skip, if you know it already.  foundational feature. 

Editor, 
explorer, 
creating files and folders using the UI .

refresh, reload. 

Open editors, 
all the opened files in a window with opened files list. 

**Outline** is more like the breadcrumbs, 
explore this more, this has more interesting things. 


Extension, advanced new file installation, 

Editor, features of editor, 
breadcrumbs, 
mini map, 

side by side editing.  click the tab drag it to the right. for side by side view. 
you can always move the tabs, and redrag them back to editor. 

you can use the same file in two windows, use the first one as a reference and make edits by looking at the same file contents at different location.


Enable preview of editor, uncheck workbench editor: Enable Preview from quick open

last thing, start up state, no need of this, to check off. uncheck the option within the editor. 


settings UI, start up editor, make this newUntitled file. 

you can set the default language as well whenever you open a new file. Use Javascript as its your domain


Intellisense, 
diff between text editor vs IDE, 


(integrated development environment)
added features over the text editor. 
intellisense, -code completion. 
param info
quick info

built in intellisense for javascript files. 

find and replace, 
search option 1(Inline within the editor), press ctrl F and search for a text and by pressing enter multiple times, you can move through the matching list. 

search option 2(within the activity bar), search all the files within the project. you can also mention the files you want to exclude. 


option enter is ALT ENTER, always remember. (Multi cursor editing). 

Go to section, 


#starts from here

Peek when you right click on function name, variable, or variable., Peeking at what definition looks like. 
you can also edit that peek contents. changes are auto saved. 

Go To, 

GoTo Definition. 
Find all references, on the side bar, all the places ou can click through. 

right click and rename symbol to change the name. 
right click, peek, Peek definition. definition of the inline. 

you can even edit the code which is auto saved. 

find and replace thing stuffs. 
lot of powerful stuff's. 


Refactoring. 

He takes an example of airTablePost.

renaming a function, control shift M to find all the uses of the function in the entire project. 


right click Find all references, this also includes the comment, 
right click, find all implementation, 
	shows how the code has been defined. 

Extensions and customization in VScode: 
	prettier



	less extensions you have the faster your VS code works. 
	you can disable extensions and enable whenever you need them. 
	
control shift p for command pallete and type recommended extensions, you can recommend your extension with your team mates, when you share the code with your team mates, it automatically asks if they want to install the extensions recommended.


settings syn, 
use your github account to sync with the settings in each of your machine. 

I have a question if I have two different accounts of VS code, I want to sync the settings from one to another. How to do it. ??
check with meta.ai, it has better answer. 

this settings synchronization also includes extensions as well. 

snippets are a big part of VS code platform: 


control shift p and insert snippet, 
 opens up the snippet pallette, you can search for snippet files. 

JavaScript (ES6) code snippets extension to install. 

you can also use the search pallete to find the snippets. 
control shift p and type imp or imd or ima and hit enter. 


control shift p - configure user snippets. 
New Global snippet file, 


```javascript
{

 // Place your global snippets here. Each snippet is defined under a snippet name and has a scope, prefix, body and

 // description. Add comma separated ids of the languages where the snippet is applicable in the scope field. If scope

 // is left empty or omitted, the snippet gets applied to all languages. The prefix is what is

 // used to trigger the snippet and the body will be expanded and inserted. Possible variables are:

 // $1, $2 for tab stops, $0 for the final cursor position, and ${1:label}, ${2:another} for placeholders.

 // Placeholders with the same ids are connected.

 // Example:

 "Print to console": {

  "scope": "javascript,typescript",

  "prefix": "log",

  "body": [

   "console.log('$1');",

   "$2"

  ],

  "description": "Log output to console"

 }

}
```

[[Emmet]], use it on a daily basis. 
create a cheat code. 

refer this video, code faster with emmet.
Faster coding with emmet. even css. 

cheat sheet, such a big topic. 

emmett simply means snippets. 

command line interface, CLI, 
adding vs code functionality to your terminal, 

HTML/CSS Workflow, 
built in features, 
emmet, 
code folding - clicking on the arrows, folds that particular code of block. 

color picker 
css class definition hovers, 

settings,
auto closing tags, 
auto updating tags, linked editing, turn on. 
linked editing, 
wrap attributes, go to settings, find wrap attributes. go ahead and change that to force. 


autoformatting, 
autosaving, 


HTML/CSS Extensions, 

color highlight: icon for the color picker. search for color highlight install and enable. 
check the html file for icon. 

css peek:  extension used is css peek. pranaygp.vscode-css- pranay prakash
on right clicking on the class name it should open up the style.css. 
you can also peek the definition. editing also saves there and here. 

HTML end tag labels: html end tag label extension install go back to html file, 

click to get multi curson on a tag lets say a paragraph tag and then hit enter it will just show you with that. helps with debugging the code. 

code spell check: code spell check extension used to highlight any text that is not spelled correctly. this highlighting is auto. you dont have to have anything. helpful when typing text. 


HTML CSS support:  HTML CSS SUPPORT extension. 
go to settings and find css stylesheets. opens up a window for edit in settings.json and there enter this cdn link within "https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css
" and you have all the tailwind classes in your intellisense. 

intellisense with css classes. 


2:20mins


the Node and Npm workflow.


extensions, 
npm npm extension deprecated.  2:23mins.
gitignore,
npm intellisense
version lens
Import cost






















Keep the settings tab always open you know. 




































current length 2:02hrs, 
Total 5:55hrs.


























