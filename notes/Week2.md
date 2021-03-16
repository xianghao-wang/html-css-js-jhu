#### Week2

##### Anatomy of CSS Rule

* CSS rule

  * Selector
  * Declaration
    * property
    * value

* Stylesheet: a collection of CSS rules

  

##### Style Placement

* Style placement

  *  affects which style declaration overwriters other style declarations

  * Three placements

    * **inline CSS** (for quick testing)
    * **head CSS** (usually override external ones)
    * **external CSS** (preferred)

    

##### Conflict Resolution

* Cascading algorithm

  * **Origin precedence**: last declaration wins, because HTML is preocessed sequentially top to bottom
    * Note: for precedence, think external CSS as declared at the spot where it's linked
  * **Declaration merge**: If there is no conflict, declarations merge into one

  * **Inheritance**: child elements inherit CSS declartions of their parent elements
  * **Specificity**: more specific selectior combination wins
    * Note: CSS rule labelled by ***!important*** wins
    * Details: https://www.w3schools.com/css/css_specificity.asp



##### Styling Text

* Font-family: https://www.w3schools.com/cssref/css_websafe_fonts.asp
* Font-size
  * Aboslute: px
  * Relative
    * n%: increase to n%  of browser default font size
    * n em: increase to n times of current font size



##### Box Model

* box-sizing (**It is not inheritant**)
  * **border-box**: the specific size is the sum of content, padding and border (preferred)
  * **content-box**: the specific size is only the content size
    * e.g. ***width: 300px***: only means the content width is 300px, rather than the whole box
* Margin
  * Margins are **cumulative horizontally** 
  * Margins **collapse vertically**
    * larger margin wins
    * parent margin wins than child margin 
      * **Note: add vertical border or padding to parent box can prevent margin from collapsing.** As long as something solid sits between the parent and child, both margins will be used.
* Universal selector: ***\****
* When content overflows from the box, we should spicify attribute ***overflow***
  * ***hidden***: cut the content out of the box
  * ***scroll***: the content is scrollable
  * ***auto***: the content is only scrollable when it overflows



##### Layout

* Floating

  * Effects

    1. Elements assigned with floating would be out of regular document flow

    2. margin of child elements would not collapse

  * ***clear***: resume regular document flow

* **Static Positioning**: normal document flow, default for all, except html tag.

  * positioning offsets are ignored

* **Relative Positioning**: element is positioned relative to its position in normal document flow

  * Offsetting the relative container element offsets its contents as well
  * **Note: Element is not taken out of the normal document flow. Even if moved, its original spot is preserved **

* **Absolute Positioning**: All offsets are relative to the position of the closest ancestors which has positioning set on it, other than static
  * Element is taken out of the norma document flow
  * **Note: By default, *html* element is the only element that has non-static positioning set on it (relative)   **



##### Media Query

* The conditions of different media queries cannot overlap range boundaries.
* Usually we provide basic styling and then add or change them to each media query



##### Reponsive Design

* Definition: site designed to adapt its layout to the viewing environment by using fluid, proportion-based grids, flexible images and CSS media queries.
  * Site's layout adapts to the size of the device
  * Content verbosity or its visual delivery may change
* **12-column grid layout**: each layout occupy 1 / 12 = **8.3%**
* Turn off default mobile zooming, so that responseive design will apply
  * ***<meta name="viewport" content="width=device-width, initial-scale=1">***



##### Bootstrap

* the most popular HTML, CSS and JS framework for developing responsive , mobile first projects on the web
  * mobile first: PLAN mobile from the start
  * CSS framework is mobile ready
* Complaints
  * **Too big, too bloated**, a lot of features you will probably never use
    * Solutions: 1. use selective download 2.write your own that's more targetted and smaller

* Bootstrap Grid System basics
  * need to be include ***container*** or ***container-fluid***
  * ***col-SIZE-SPAN***
    * ***SIZE***
      * Screen width range identifier
      * Columns will collapse below the width unless another rule applies
    * ***SPAN***
      * How many column elements should span (in 12-column grid layout)
      * Values: 1 throught 12
  * all columns must be inside ***.row***
  * SIZE identifier identifies at which breakpoint specified column spans will be ignored and all elements will collapse (stack)
  * if no other rules apply, spcifying ***.col-SPAN*** will keep that layout no matter what the size of the screen