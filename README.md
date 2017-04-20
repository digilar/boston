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

