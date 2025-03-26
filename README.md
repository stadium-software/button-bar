# Button Bars

Use a Button Bar to combine the triggers for a number of related features into one interface element. 

https://github.com/stadium-software/button-bar/assets/2085324/07ca94ed-7f60-433f-9f56-7b785c62c5b6

## Version 
1.0 - initial

1.1 Upgraded for Stadium 6.12+; converted px to rem; moved icon example to stylesheet

# Setup

## Application Setup
1. Check the *Enable Style Sheet* checkbox in the application properties

## Page Setup
1. Drag a *Flexbox* or a *Container* control to the page 
2. Add a class called "stadium-button-bar" into the control classes property
3. Drag some *Button* controls into the control
4. Add any text you wish to show on the buttons into the text property

## Button Icons
To display icons in buttons

1. Add a class to the button classes property (e.g. pointer-icon-left)
2. Add some CSS to the stylesheet to specify how to display the icon in the button (more examples in the example application)

Example
```css
.pointer-icon-left button {
    background-repeat: no-repeat;
	background-size: 16px;
	padding-left: 26px;
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='1em' height='1em' viewBox='0 0 24 24'%3E%3C!-- Icon from Material Symbols by Google - https://github.com/google/material-design-icons/blob/master/LICENSE --%3E%3Cpath fill='%23ffffff' d='M11.7 18q-2.4-.125-4.05-1.85T6 12q0-2.5 1.75-4.25T12 6q2.425 0 4.15 1.65T18 11.7l-2.1-.625q-.325-1.35-1.4-2.212T12 8q-1.65 0-2.825 1.175T8 12q0 1.425.863 2.5t2.212 1.4zm1.2 3.95q-.225.05-.45.05H12q-2.075 0-3.9-.788t-3.175-2.137T2.788 15.9T2 12t.788-3.9t2.137-3.175T8.1 2.788T12 2t3.9.788t3.175 2.137T21.213 8.1T22 12v.45q0 .225-.05.45L20 12.3V12q0-3.35-2.325-5.675T12 4T6.325 6.325T4 12t2.325 5.675T12 20h.3zm7.625.55l-4.275-4.275L15 22l-3-10l10 3l-3.775 1.25l4.275 4.275z'/%3E%3C/svg%3E");
	background-position: center left 6px;
}
```

## CSS
The CSS below is required for the correct functioning of the module. Variables exposed in the [*button-bar-variables.css*](button-bar-variables.css) file can be [customised](#customising-css).

### Before v6.12
1. Create a folder called "CSS" inside of your Embedded Files in your application
2. Drag the two CSS files from this repo [*button-bar-variables.css*](button-bar-variables.css) and [*button-bar.css*](button-bar.css) into that folder
3. Paste the link tags below into the *head* property of your application
```html
<link rel="stylesheet" href="{EmbeddedFiles}/CSS/button-bar.css">
<link rel="stylesheet" href="{EmbeddedFiles}/CSS/button-bar-variables.css">
``` 

### v6.12+
1. Create a folder called "CSS" inside of your Embedded Files in your application
2. Drag the CSS files from this repo [*button-bar.css*](button-bar.css) into that folder
3. Paste the link tag below into the *head* property of your application
```html
<link rel="stylesheet" href="{EmbeddedFiles}/CSS/button-bar.css">
``` 

### Customising CSS
1. Open the CSS file called [*button-bar-variables.css*](button-bar-variables.css) from this repo
2. Adjust the variables in the *:root* element as you see fit
3. Stadium 6.12+ users can comment out any variable they do **not** want to customise
4. Add the [*button-bar-variables.css*](button-bar-variables.css) to the "CSS" folder in the EmbeddedFiles (overwrite)
5. Paste the link tag below into the *head* property of your application (if you don't already have it there)
```html
<link rel="stylesheet" href="{EmbeddedFiles}/CSS/button-bar-variables.css">
``` 
6. Add the file to the "CSS" inside of your Embedded Files in your application

**NOTE: Do not change any of the CSS in the 'button-bar.css' file**

## Upgrading Stadium Repos
Stadium Repos are not static. They change as additional features are added and bugs are fixed. Using the right method to work with Stadium Repos allows for upgrading them in a controlled manner. 

How to use and update application repos is described here: [Working with Stadium Repos](https://github.com/stadium-software/samples-upgrading)