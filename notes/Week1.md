

#### Week 1

* HTML: Hypertext Markup Language
  * Hypertext: the text that can be linked to other sites
  * Markup: annotate the meaning of contents e.g. heading, paragraph or link
  * Language: must follow the specific syntax
* Technologies
  * HTML: structure
  * CSS: style e.g. colors
  * JavaScript: behaviour
* HTML tags can be lowercase or uppercase in HTML5
* Content mode
  * **Block-level elements**
    * render to begin on a new line (by default)
    * May contain inline or other block-level elements
    * Roughly flow content (HTML5 category)
  * **Inline elements**
    * render on the same line
    * may only contain other inline element
      * Note: **a** can contain block-level elements
    * Roughly phrasing content (HTML5 category)

* **Semantic**: relating to meaning in language or logic
* **Semantic HTML element**: implies some meaning to the content
  * understanding the meaning of content surrounded by a semantic element better
  * may help search engine ranking e.g. SEO 
  * Well chosen content of H1 element is crutial to SEO
* HTML entity references
  * 3 characters you should always escape
    * <: \&lt;
    * \>: \&gt;
    * &: \&amp;
  * Make serveral words stay in the same line
    * Non-breaking space: **\&nbsp;** (不换行空格) 
    * Usage: word1**\&nbsp;**word2**\&nbsp;**word3
  * Advantages
    * avoid rendering issue
    * safeguard against more limited character encoding e.g. **"** can be replaced by **\&quote;**

##### Create Links

* a tag is both a block-level and inline element in HTML5

##### Images

* Specify **width** and **height** attributes of img tag can prevent the loaded image from jumpping in
* It is a good idea to spicify **width** and **height** of img element
