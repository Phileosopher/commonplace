
## code vs documentation

Apply all of our pragmatic principles to documentation as well as to code.
- PRAGMATIC PROGRAMMER IS GOOD FOR THIS AS WELL??

Times you need to present the same documentation in different formats: a printed document, Web pages, online help, or perhaps a slide show. The typical solution relies heavily on cut-and-paste, creating a number of new independent documents from the original. This is a bad idea: a document's presentation should be independent of its content. If you are using a markup system, you have the flexibility to implement as many different output formats as you need. You can choose to have <H1>Chapter Title</H1> generate a new chapter in the report version of the document and title a new slide in the slide show. Technologies such as XSL and CSS can be used to generate multiple output formats from this one markup.

As long as your original markup is rich enough to express all the concepts you need (including hyperlinks), translation to any other publishable form can be both easy and automatic. You can produce online help, published manuals, product highlights for the Web site, and even a tip-a-day calendar, all from the same source-which of course is under source control and is built along with the nightly build.

## DRY principle

Suppose we have a specification that lists the columns in a database table. We'll then have a separate set of SQL commands to create the actual table in the database, and probably some kind of programming language record structure to hold the contents of a row in the table. The same information is repeated three times. Change any one of these three sources, and the other two are immediately out of date. This is a clear violation of the DRY principle. To correct this problem, we need to choose the authoritative source of information. This may be the specification, it may be a database schema tool, or it may be some third source altogether. Let's choose the specification document as the source. It's now our model for this process. We then need to find a way to export the information it contains as different views-a database schema and a high-level language record, for example.

[Nicolò Pignatelli](https://hackernoon.com/this-is-not-the-dry-you-are-looking-for-a316ed3f445f)
(2018) This is not the DRY you are looking for

[Jamie Wong](http://jamie-wong.com/2013/07/12/grep-test/)
(2013) Too DRY - The Grep Test

## Heuristic for contenteditable rich-text editors

Editor should:

Be stable

Be open source

Handle soft breaks

Be able to manipulate styles on block level elements

Be able to manipulate styles on inline level elements

Be able to manipulate classes on block level elements

Be able to manipulate classes on inline level elements

Be able to alter custom attributes on block level elements

Be able to alter custom attributes on inline level elements

Cache the selection

Have iframing capabilities as well as inline mode capability

Change the tag type of nodes

Clear the format

Have a concise api

Support various module loaders

  AMD & Common.js

Should have an organization backing the service and have a potential paid support plan

Should copy & paste from Microsoft word
