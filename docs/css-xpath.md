<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/logos/COMETAROCKS_LogoEslog_Y_W.png">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
  <img alt="Shows a black logo in light color mode and a white one in dark color mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>

<br />

# Selectors table of contents

Co.meta uses "{selectors}" to navigate around a page. Whenever Co.meta references to "{selector}", this can either be a CSS-selector or xpath selector. This makes the usage of Co.meta really nice.

XPath selectors are very powerful as one can use simple calculations as well as Contains or Substr operations.

Here are the most frequently used xpath selectors:

* //*[contains(.,"FooBar")] ... selects anything that contains FooBar as innerHtml
* //*[contains(@class,"FooBar")] ... selects anything that contains a class name FooBar

If you are familiar with xpath and want to see details, go directly to the xpath topic you are looking for or read through the introduction of HTML and CSS before.

1. [How is an HTML page structured?](#how-is-an-html-page-structured)
2. [What are CSS selectors?](#CSS_SE)
3. [What is XPath](#XPATH_SE)
4. [Using XPath](#USEXP_SE)
    1. [Descendant selectors](#DES_XP)
    2. [Attribute selectors](#ATT_XP)
    3. [Order selectors](#ORD_XP)
    4. [Siblings](#SIB_XP)
    5. [Jquery selectors](#JQU_XP)
    6. [Other selectors](#OTH_XP)
    7. [Steps and axes](#STAX_XP)
    8. [Prefixes](#PRF_XP)
    9. [Predicates](#PRD_XP)
    10. [Operators](#OPE_XP)
    11. [Using nodes](#NOD_XP)
    12. [Indexing](#IND_XP)
    13. [Chaining order](#COR_XP)
    14. [Node functions](#NFC_XP)
    15. [Boolean functions](#BFC_XP)
    16. [Type conversion](#TFC_XP)
    17. [String functions](#SFC_XP)
    18. [Axes](#AXE_XP)
    19. [Unions](#UNI_XP)
5. [Support](#SUPPORT_SE)

<br/>

### 1. How is an HTML page structured?

In the world everything is classified to discern one thing from another. For instance, someone can have a cat as a pet which in order to be identified and distinguished from the a different cat, is given a name, a gender, a breed, etc. The same thing happens with websites, as each element has its type, class, name, id, etc. Behind the scenes of a webpage there is a source code written in HTML language and the result will vary depending of what tag is used or what properties are given to this.

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/webpage.png" width="600px">

### 2. What are CSS selectors?<a name="CSS_SE"></a>

Whenever you want to design or edit an webpage, you will a specific tool to said task. Css selectors are a tool to decide which element of the HTML code needs to be selected. This method can be used to call any component expected to be interacted with or be modified by the user. Knowing that, the user must learn a set of rules and the patterns used to select the desired elements. Here are a few basic examples:

<table>
    <tr>
        <th>Selector</th>
        <th>Example</th>
        <th>Example description</th>
    </tr>
    <tr>
        <td>element</td>
        <td>p</td>
        <td>Selects all < p > elements</td>
    </tr>
    <tr>
        <td>.class</td>
        <td>.intro</td>
        <td>Selects all elements with class="intro"</td>
    </tr>
    <tr>
        <td>#id</td>
        <td>#firstname</td>
        <td>Selects the element with id="firstname"</td>
    </tr>
    <tr>
        <td>[attribute]</td>
        <td>[target]</td>
        <td>Selects all elements with a target attribute</td>
    </tr>
    <tr>
        <td>::nth-child(n)</td>
        <td>p:nth-child(2)</td>
        <td>Selects every < p > element that is the second child of its parent</td>
    </tr>
<table>

### 3. What is XPath?<a name="XPATH_SE"></a>

XPath stands for XML Path. It’s a query language that helps identify elements from an XML document. It uses expressions that navigate into an XML document in a way that can be traced from the start to the intended element—like forming a path from the start. Despite being harder to learn and master, XPath has multiple advantages over CSS selectors:

- Creating in XPath is more flexible than in CSS Selector.

- When you don’t know the name of an element, you can use contains to search for possible matches.

- Queries are compact, easy to type and read and easily parsed and can return any number of results, including zero.

- Queries accept multiple conditions. This is specially useful with dynamic elements like for example translated texts.

- It can be used in JavaScript, Java, XML Schema, PHP, Python, C, C++, and lots of other languages.

### 4. Using XPath<a name="USEXP_SE"></a>

At first glance learning XPath might seem a little bit complex, but once mastered, it transforms into a very powerful tool. Here is a list of the XPath selectors and its equivalent to CSS selectors:

### Descendant selectors<a name="DES_XP"></a>

Descendant selectors are used to specify the starting point of a selection.

<table>
    <tr>
        <th>XPATH</th>
        <th>Equivalent</th>
    </tr>
    <tr>
        <td>//h1</td>
        <td>h1</td>
    </tr>
    <tr>
        <td>//div//p</td>
        <td>div p</td>
    </tr>
    <tr>
        <td>//ul/li</td>
        <td>ul > li</td>
    </tr>
    <tr>
        <td>//ul/li/a</td>
        <td>ul > li > a</td>
    </tr>
    <tr>
        <td>//div/*</td>
        <td>div > *</td>
    </tr>
    <tr>
        <td>:root</td>
        <td>/</td>
    </tr>
    <tr>
        <td>/body</td>
        <td>:root > body</td>
    </tr>
</table>

Example:

- _//div//span_

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/Ex1.png">

### Attribute selectors<a name="ATT_XP"></a>

Attribute selectors are used to specify the attributes of the elements to be selected.

<table>
    <tr>
        <th>XPATH</th>
        <th>Equivalent</th>
    </tr>
    <tr>
        <td>//*[@id="id"]</td>
        <td>#id</td>
    </tr>
    <tr>
        <td>//*[@class="class"]</td>
        <td>.class</td>
    </tr>
    <tr>
        <td>//input[@type="submit"]</td>
        <td>input[type="submit"]</td>
    </tr>
    <tr>
        <td>//input[@type="submit"]</td>
        <td>a#abc[for="xyz"]</td>
    </tr>
    <tr>
        <td>//a[@rel]</td>
        <td>a[rel]</td>
    </tr>
    <tr>
        <td>//a[starts-with(@href, '/')]</td>
        <td>a[href^='/']</td>
    </tr>
    <tr>
        <td>//a[ends-with(@href, '.pdf')]</td>
        <td>a[href$='pdf']</td>
    </tr>
    <tr>
        <td>//a[contains(@href, '://')]</td>
        <td>a[href*='://']</td>
    </tr>
    <tr>
        <td>//a[contains(@rel, 'help')]</td>
        <td>a[rel~='help']</td>
    </tr>
</table>

Example:

- _//div[@class]_

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/Ex2.png">

### Order selectors<a name="ORD_XP"></a>

Order selectors are used to specify the index of the element to be selected inside of a node.

<table>
    <tr>
        <th>XPATH</th>
        <th>Equivalent</th>
    </tr>
    <tr>
        <td>//ul/li[1]</td>
        <td>ul > li:first-of-type</td>
    </tr>
    <tr>
        <td>//ul/li[2]</td>
        <td>ul > li:nth-of-type(2)</td>
    </tr>
    <tr>
        <td>//ul/li[last()]</td>
        <td>ul > li:last-of-type</td>
    </tr>
    <tr>
        <td>//li[1][@id="id"]</td>
        <td>li#id:first-of-type</td>
    </tr>
    <tr>
        <td>//*[1][name()="a"]</td>
        <td>a:first-child</td>
    </tr>
    <tr>
        <td>//*[last()][name()="a"]</td>
        <td>a:last-child</td>
    </tr>
</table>

Example:

- _//div[4]_

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/Ex3.png">

### Siblings<a name="SIB_XP"></a>

Sibling selections are an extension of the descendant selectors.

The adjacent sibling selector (+) is used to select and element that is directly after another specific element.

The general sibling selector (~) selects all the elements that are next siblings of a specified element.

Sibling elements must have the same parent element, and 'adjacent' means 'immediately following'.

<table>
    <tr>
        <th>XPATH</th>
        <th>Equivalent</th>
    </tr>
    <tr>
        <td>//h1/following-sibling::ul</td>
        <td>h1 ~ ul</td>
    </tr>
    <tr>
        <td>//h1/following-sibling::ul[1]</td>
        <td>h1 + ul</td>
    </tr>
    <tr>
        <td>//h1/following-sibling::[@id="id"]	</td>
        <td>h1 ~ #id</td>
    </tr>
</table>

Example:

- _//div/following-sibling::span_

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/Ex4.png">

### Jquery selectors<a name="JQU_XP"></a>

The following XPath selectors have the same functionality as if you were to use JQuery to select an element.

<table>
    <tr>
        <th>XPATH</th>
        <th>Equivalent</th>
    </tr>
    <tr>
        <td>//ul/li/..</td>
        <td>$('ul > li').parent()</td>
    </tr>
    <tr>
        <td>//li/ancestor-or-self::section</td>
        <td>$('li').closest('section')	</td>
    </tr>
    <tr>
        <td>//a/@href</td>
        <td>$('a').attr('href')</td>
    </tr>
    <tr>
        <td>//span/text()</td>
        <td>$('span').text()</td>
    </tr>
</table>

Example:

- _//div/@class_

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/Ex5.png">

### Other selectors<a name="OTH_XP"></a>

<table>
    <tr>
        <th>XPATH</th>
        <th>Equivalent</th>
    </tr>
    <tr>
        <td>//h1[not(@id)]</td>
        <td>h1:not([id])</td>
    </tr>
    <tr>
        <td>//button[text()="Submit"]</td>
        <td>Text match</td>
    </tr>
    <tr>
        <td>//button[contains(text(),"Go")]</td>
        <td>Text match (substring)</td>
    </tr>
    <tr>
        <td>//product[@price > 2.50]</td>
        <td>Arithmetic</td>
    </tr>
    <tr>
        <td>//ul[*]</td>
        <td>Has children</td>
    </tr>
    <tr>
        <td>//ul[li]</td>
        <td>Has children (specific)</td>
    </tr>
    <tr>
        <td>//a[@name or @href]</td>
        <td>Or logic</td>
    </tr>
    <tr>
        <td>//a | //div</td>
        <td>Union (joins results)</td>
    </tr>
</table>

Example:

### Steps and axes<a name="STAX_XP"></a>

A step in XPath is the name of the element or the function used for the query.

An axis represents a relationship to the context (current) node and is used to locate nodes relative to that node on the tree.

<table>
    <tr>
        <th>Axis</th>
        <th>Example</th>
        <th>Explanation</th>
    </tr>
    <tr>
        <td>Axe /</td>
        <td>//ul/li/a</td>
        <td>Selects an element directly below the main element</td>
    </tr>
    <tr>
        <td>Axe //</td>
        <td>//[@id="list"]//a</td>
        <td>Selects an element below the main element, not necessarily directly below</td>
    </tr>
    <tr>
        <td colspan="3">Separate your steps with /. Use two (//) if you don’t want to select direct children.</td>
    </tr>
    <tr>
        <td>Prefix //</td>
        <td>//hr[@class='edge']</td>
        <td>Starts the selection from any element</td>
    </tr>
    <tr>
        <td>Prefix ./</td>
        <td>./a</td>
        <td>Starts the selection from a position relative to a previously selected element</td>
    </tr>
    <tr>
        <td>Prefix /</td>
        <td>/html/body/div</td>
        <td>Starts the selection from the first line of the code</td>
    </tr>
</table>

Example:

- _/html/body/cometa/header/div[1]/div[1]/div[1]_

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/Ex6.png">

### Predicates<a name="PRD_XP"></a>

Predicates are used to find a specific node or a node that contains a specific value. They are always embedded in square brackets.

<table>
    <tr>
        <th>Example</th>
        <th>Explanation</th>
    </tr>
    <tr>
        <td>//div[true()]<br/>//div[@class="head"]<br/>//div[@class="head"][@id="top"]</td>
        <td>Restricts a nodeset only if some condition is true. They can be chained.</td>
    </tr>
</table>

Example:

### Operators<a name="OPE_XP"></a>

<table>
    <tr>
        <th>Operator</th>
        <th>Example</th>
    </tr>
    <tr>
        <td>=</td>
        <td>//a[@id = "xyz"]</td>
    </tr>
    <tr>
        <td>!=</td>
        <td>//a[@id != "xyz"]</td>
    </tr>
    <tr>
        <td>+, -, *, div, =, mod</td>
        <td>//a[@priceA + @priceB]</td>
    </tr>
    <tr>
        <td>>, <, <=, >=</td>
        <td>//a[@price > 25]</td>
    </tr>
    <tr>
        <td>and</td>
        <td>//div[@id="head" and position()=2]</td>
    </tr>
    <tr>
        <td>or</td>
        <td>//div[(x and y) or not(z)]</td>
    </tr>
</table>

### Indexing<a name="IND_XP"></a>

These are different ways to select and element on a specified index.

<table>
    <tr>
        <th>XPATH</th>
        <th>Explanation</th>
    </tr>
    <tr>
        <td>//a[1]</td>
        <td>Returns the first < a > tag</td>
    </tr>
    <tr>
        <td>//a[last()]</td>
        <td>Returns the last < a > tag</td>
    </tr>
    <tr>
        <td>//ol/li[2]</td>
        <td>Return the second < li > tag</td>
    </tr>
    <tr>
        <td>//ol/li[position()=2]</td>
        <td>Returns the second < li > tag, works the same way as the previous one</td>
    </tr>
    <tr>
        <td>//ol/li[position()>1]</td>
        <td>Returns all the < li > tags starting from the second coincidence</td>
    </tr>
</table>

Example:

- _//div[last()]_

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/Ex7.png">

### Chaining order<a name="COR_XP"></a>

In a XPath query the order is very important as it will affect the final result. The following examples will return different values.

- a[1][@href='/']

- a[@href='/'][1]

Example:

- _//div[1]/div_

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/Ex8.png">

- _//div/div[1]_

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/Ex9.png">

### Node functions<a name="NFC_XP"></a>

<table>
    <tr>
        <th>XPATH</th>
        <th>Explanation</th>
    </tr>
    <tr>
        <td>name()</td>
        <td>//[starts-with(name(), 'h')] <br/>Returns the elements whose name equals to 'h'</td>
    </tr>
    <tr>
        <td>text()</td>
        <td>//button[text()="Submit"]<br/>Returns the elements which have 'Submit' as inner text</td>
    </tr>
    <tr>
        <td>lang(str)</td>
        <td>Checks if the element has the same language as the specified and returns true or false</td>
    </tr>
    <tr>
        <td>namespace-uri()</td>
        <td>Checks if the element has the same namespace-uri as the specified and returns true or false</td>
    </tr>
    <tr>
        <td>count()</td>
        <td>//table[count(tr)]<br/>Counts the amount of nodes in a node-set and returns an integer</td>
    </tr>
    <tr>
        <td>position()</td>
        <td>//ol/li[position()=2]<br/>Returns a number equal to the context position from the expression evaluation context</td>
    </tr>
</table>

Example:

- _//span[text()="co."]_

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/Ex10.png">


### Boolean functions<a name="BFC_XP"></a>

<table>
    <tr>
        <th>XPATH</th>
        <th>Explanation</th>
    </tr>
    <tr>
        <td>not(expr)</td>
        <td>button[not(starts-with(text(),"Submit"))]<br/>Returns the elements that do not satisfy the inputted conditions</td>
    </tr>
</table>

Example:

- _//span[not(text()="co.")]_

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/Ex11.png">

### Type conversion<a name="TFC_XP"></a>

<table>
    <tr>
        <th>XPATH</th>
        <th>Explanation</th>
    </tr>
    <tr>
        <td>string()</td>
        <td>Converts the result into a string</td>
    </tr>
    <tr>
        <td>number()</td>
        <td>Converts the result into a number</td>
    </tr>
    <tr>
        <td>boolean()</td>
        <td>Converts the result into true or false</td>
    </tr>
</table>

### String functions<a name="SFC_XP"></a>

<table>
    <tr>
        <th>XPATH</th>
        <th>Explanation</th>
    </tr>
    <tr>
        <td>contains()</td>
        <td>font[contains(@class,"head")]<br/>Checks if the element contains the specified string</td>
    </tr>
    <tr>
        <td>starts-with()</td>
        <td>font[starts-with(@class,"head")]<br/>Checks if the element starts with the specified string</td>
    </tr>
    <tr>
        <td>ends-with()</td>
        <td>font[ends-with(@class,"head")]<br/>Checks if the element ends with the specified string</td>
    </tr>
    <tr>
        <td>concat(x, y)</td>
        <td>Concatenates and returns 2 specified strings</td>
    </tr>
    <tr>
        <td>//*[contains(lower-case(@name),'ear')]</td>
        <td>This DOES NOT work with the selenium x-path implementation (yet). You can use translate to achieve lower-case or upper-case. Example: `//*[translate(.,'HOME','home')='home']`. This example matches any kind auf "HoMe" with "home". This is very powerful, when you see text on your screen, where you do not know, if it has been transformed with CSS rules. So, if you are looking at text to match, you might always want to make sure that it is matched case insensitive.</td>
    </tr>
    <tr>
        <td>substring-before(str, sub)</td>
        <td>Returns the string that is part of a given string before a given substring. <br/>substring-before("01/02", "/") returns 01</td>
    </tr>
    <tr>
        <td>substring-after(str, sub)</td>
        <td>Returns the string that is part of a given string after a given substring. <br/>substring-after("01/02", "/") returns 02</td>
    </tr>
    <tr>
        <td>translate(str, abc, XYZ)</td>
        <td>Evaluates a string and a set of characters to translate and return the translated string. str is the string to evaluate, abc is the string of characters that will be replaced, XYZ is the string of characters used for replacement; the first character in XYZ will replace every occurrence of the first character in abc that appears in str.<br/>
        < xsl:value-of select="translate('The quick brown fox.', 'abcdefghijklmnopqrstuvwxyz', 'ABCDEFGHIJKLMNOPQRSTUVWXYZ')" / > will return 'THE QUICK BROWN FOX.' <br/> < xsl:value-of select="translate('The quick brown fox.', 'brown', 'red')" / > will return 'The quick red fdx.'</td>
    </tr>
    <tr>
        <td>normalize-space(string)</td>
        <td>Remove leading and trailing white-spaces from a string, replaces sequences of whitespace characters by a single space and returns the result string</td>
    </tr>
    <tr>
        <td>string-length(string)</td>
        <td>Returns the amount of characters in a given string</td>
    </tr>
</table>

Example:

- _//div[string-length("abc")]_

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/Ex12.png">

### Unions<a name="UNI_XP"></a>

In XPath it is possible to join two or more independent queries into a single one

//button[not(starts-with(text(),"Submit"))] | button[not(starts-with(text(),"Send"))]

The previous query returns all buttons that do not contain 'Submit' or 'Send' as inner text.

Example:

- _//div/div/div/div | //span_

<img src="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/Ex13.png">

<br/>

As you can see, aside from the already existing CSS selectors XPath offers a greater amount of selection options vastly expanding the querying possibilities. Furthermore, as XPath can be used in many different programming languages, it can become a very useful, flexible and powerful tool in software developing and testing.

### 5. Support<a name="SUPPORT_SE"></a>
For further questions or issues, please contact us at our email <tec_dev@cometa.rocks> or via Discord https://discord.gg/e3uBKHhKW5
