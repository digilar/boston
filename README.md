Digilär css
======
##Guidelines

* Use classes instead of IDs (Avoid uneccessary specificity)
* Mobile first and responsive
* Add classes according to simplified BEM (Block Element Modifier)

	Simplified BEM

	```
	.prefix-block {}
	.prefix-block-element {}
	.prefix-block-element--modifier {}

	.b-list {}
	.b-list-item {}
	.b-list-item--selected {}
	```
	
* States: selected, opened, closed, disabled
* Separate js and style classes. Do not style js classes. --modifier level is used both by js and css
* As a rule of thumb, avoid unnecessary nesting in SCSS. At most, aim for three levels. If you cannot help it, step back and rethink your overall strategy (either the specificity needed, or the layout of the nesting). example to avoid:

	```
	Do not
	.list {
		styles..
		li {
			styles..
			a {
				styles..
				color:blue;
			}
		}
	}

	```

	```
	Do
	.list {
		styles..
	}

	.list-item {
		styles..
	}

	.list-link {
		styles..
	}

	```
	Prefer direct descendant selectors by default, and use as little specificity as possible

	```
	.ok-list {
		styles..
		> li {
			styles..
		}
	}
	```

### Spacing

* Use one tab to indent.
* Put spaces after : in property declarations.
* Put spaces before { in rule declarations.
* Put line breaks between rulesets.
* When grouping selectors, keep individual selectors to a single line.
* Place closing braces of declaration blocks on a new line.
* Each declaration should appear on its own line for more accurate error reporting.

### Formatting

* Use // for comment blocks (instead of /* */).
* Avoid specifying units for zero values, e.g., margin: 0; instead of margin: 0px;

### Documenting

Each element should have this comment structure to generate a styleguide.

~~~
/*
##Name
  Description
```
Markup
```
*/
~~~

# Structure

Global
------
Common and core

Example files

* functions.scss
* mixins.scss
* colors.scss
* variables.scss

Base
------

Styling and profiling of html common elements

~~~
.b-block-element {
	// Styles
}
~~~

Example files

* reset.scss
* tables.scss
* lists.scss
* blockquote.scss
* typography.scss
* buttons.scss
* forms.scss
* etc.scss

Components
------
Custom and common components of UI

~~~
.c-block-element {
	// Styles
}
~~~
Example files

* alert.scss
* modal.scss
* dropdown.scss
* etc.scss

Layout
------
Layout are the core UI parts

```
.l-layout {
	// Styles
}
```
Example files

* toolbar.scss
* sidebar.scss
* etc.scss

Templates
------
Custom css for specific templates

```
.nameoftemplate {
	// Styles
}
```
Example files

* toolbar.scss
* sidebar.scss
* etc.scss

Widgets
------
Layout for widgets 

```
.w-layout {
	// Styles
}
```
Example files

* numberline.scss
* probability.scss
* etc.scss

Grid
------
Grid for structuring content

```
.g-container {
	// Styles
}
```

* grid.scss


Helpers
------
Css that speeds up production e.g display:flex

```
.h-helper {
	// Styles
}
```

* flexbox.scss
* positions.scss
* spacing.scss
* etc.scss

Animations
------
Them sassy animations!

```
.ani-animation {
	// Styles
}
```
* entrances.scss
* exits.scss
* positions.scss
* in-place.scss

