# Initial view

**When** I open the LD interface

**Then** I see an empty page.

# Creating objects

**Given** I want to reconstruct something

**When** I press +

**Then** a shop appears

**Then** I select a datasource.




# When I want to leave a small message

**Given** I want to create a small and compact document, like a microblog.

**When** I type a message and press enter.

**Then** A living document is created.

**Given** the created document is to be displayed.

**Then** The rendered document will be compact.

# Re-use a field

**Given** I have some data to include.

**When** I create a new document.

**Then** I can select a data type.

**Given** I have created a document with a type.

**Then** I select the item on the shelf.

**Then** The item is inserted into the document at insertion position.


# Creating a thing

**Given** I want to create a 'thing'.

**When** I select 'Create thing'

**Then** I am asked for the thing's name

**Then** A new document is created.

**Then** The thing appears in the shelf.

**Then** The thing is inserted into the document with its own border.

# Outline view

**Given** I have a document

**Then** I select outline view

**Then** The documents structure is rendered in outline view

**Given** The document is in outline view

**When** I transpose the outline

**Then** The layout of the document change from top down to left-right

# Spreadsheet view

**Given** I have data documents and I want to mutate the data documents

**When** I select spreadsheet view

**Then** I see each document in its own cell.

**Given** I select an empty cell

**When** I press the equals key (=)

**Then** The **toolbox opens**

**Given** The toolbox is open and I have selected a document

**Then** Tools that support the document should be displayed.

**Given** I have selected a tool and the toolbox is open

**When** I select a tool

**Then** Then the tool is activated with the document and its output placed into the selected cell.

# Program document

**Given** I want to interact with some code.

**When** I create a code context.

**When** I select the program language

**Then** The document is now interactable as a program.

# Using Data from existing contexts

**Given** I have created a context that contains data and I want to use it in sourcecode.

**When** I click the 'Connect' button.

**Then** The 'Data connection' dialog pops up.

**When** I select the 'Use the data'.

**Then** A code context is inserted into the document.

**Then** I select the language of the code as Javascript

**When** I select the 'requirejs injection' interface of execution from a number choices.

**When** I click the Execute action, an orphan context appears on the shelf.


**Given** I have an orphan program context on the shelf and I want to include the output.

**When** I can select a representation of the data to display.

**Then** The data is inserted into the document in the format requested.


# Shelf

**Given** I select something from the shelf.

**Then** The shelf item is embedded into the document.

**Then** The shelf item requests some information that it might not already have.


# Nested List driven interface

**Given** I have written a list of things.

**Given** I want to provide more details about each item or expand what they are.

**Given** My list of things are ideas.

**When** I click an idea to inspect.

**Then** I can view the outputs for the item.


# Shell Bucket

**Given** I want to inspect the output of a terminal program.

**When** I pipe the output of the program into 'bucket'.

**Then** The output appears as an orphan

**Given** I want to breakdown the output and display it differently.

**Then** I can parse and process the output as data.

I would like to move the available 'events' that can be raised on different parts of the screen into the JSON and the algorithm out of the application and into a microservice.


 * A change is like a migration
 * The context server is just an accumulation of facts in different languages and syntaxes.

# Swipe

**Given** I have inserted some text, an image, a table or some data.

**Given** I am curious about what other visualizations of this data is available.

**When** I swipe to the left or the right.

**Then** I can browse different views.

# Hierarchy Swap

**Given** I have a data hierarchy.

**Given** I want to see the data from a different perspective.

**When** I swap the hierarchy.

**Then** The data re-organizes to show the data from a different perspective.

# Install an API

**Given** There is a service that I wish to use in my living document.

**Given** The service has a discovery mechanism such as HAL or RAML.

**When** I can make calls to the service

# Auto-annotation

**Given** I input some data that corresponds to a known format.

**When** The format is detected.

**Then** The data is annotated and becomes a first class citizen.

# Page Extraction

**Given** There is a webpage.

**Given** I want to use the webpage in some way.

**When** I paste the URL

**Then** LD may fetch a screenshot of the page and analyse the page for interesting features.


# Semantic operation search

**Given** I want to do something with something on the screen.

**When** I search a behaviour offered by a context.

**Then** I get a list of matching behaviours.

**When** I select a behaviour.

**Then** The behaviour is ran against the context.

# Using multiple data sources together

**Given** I have created a number of distinct fields.

**Given** I want to use these fields in some way together.

**When** I press '=' in the semantic autocomplete.

**Then** A search field pops up and allows me to search for a field.

**When** When I search for a field by typing some of its content or its name.

**Then** The matching fields are displayed in a list.

**When** I click on or press enter while the matching field is selected.

**Then** The chosen field is added to added to a graph diagram showing the input data sources.

**Given** I have selected more than one field and all the fields have appeared in the diagram.

**Then** A list of available matching operations appears in a list with an description of what they do.

This is an example of context as an explorable web. The tool shows you what you could possible doing with minimal effort.

# Living document services

 * template service
 * code execution service
 * source identification
 * text annotator/feature extraction

# Easy text diff

Fixing something and sending someone the difference should be easier for normal users to do.

# Grunt task visualization

 * Insert 'fake' grunt and record all calls.
 * Try to match loaded NPM modules to init data.
 * Draw a pipeline UI.
 * Treat filenames/folders as 'things' that can be operated on in the UI.

# Json waveguide

# Github interception layer

 * To distribute all repositories things to other machines (just in case github dies)

# Code mobility

MODEL
```
var items = [{'name': 'blah'}];

items.draw();

items.on('click.delete', function () { // do something })
items.on('click.edit', function () { // do something })

items.on('paint', function () {
  server.update(items);
  items.trigger('');
})
```

# Computing is a co-ordination problem

Computing is massive logistic and co-ordination problem.

# In document promises

Can be used to spin up things.

 * 'There is a process'
 * 'There is a file'
 
These become true when created in the living document.

# Template microservice

Render arbitrary template with data.

curl -X POST -H"Content-Type: application/json" http://localhost:1446/render/mustache -d @- < example-template.txt 

# Oplookup

curl -X POST -H"Content-Type: application/json" http://localhost:7474/db/data/cypher -d @- < example-oplookup.txt

```
MATCH (a:Type)-[:Input]->(op:Operation)-[:Output]->(out:Type) WHERE a.name IN ["JSON", "Mustache HTML"] RETURN DISTINCT op, out
```

# Code block detection

The following code, as written or pasted should be detected as a block to be identified accordingly. The ruby should be detected as a ruby block.

```
See the following code

p = Hash.new
p.blah = 6

puts p
```

* do we need incremental bayesian detection?

# Feature extraction

Data embedded in the following should be detectable:

 * dates, times
 * names
 * named entity transducer/coreference
 * gazetters annotation

(phone number.jape)


# Shell buckets

 * User pipes data into program called 'bucket'
 * Data gets put into a database.
 * Living Documents gets notified, perhaps via web socket that there is now data available at URL. This may be a generic URL notification mechanism.

# Mouseover Data Matching

When a user interacts with a piece of onscreen data, the data has a unique identifier.

A number of user interfaces match this data as in, they can use this data to create a user interface.

This idea came about from being able to mouseover a piece of information, such as a noun and then suddenly view what a friend thinks of it. (FrienDB) I visualize this as a graph and then another graph merging with it and then another interface popping up to represent it.

# Scrollog

A scrollog is application, a log file viewer that as you scroll down the file, it presents the key interesting facts in widgets around the log file as you go. This is possible through efficient realtime parsing of onscreen elements as you go down. The key is to summarize what is visible.

Crocodile log clips. If a build is started and a server log would be useful while something is running, it should be possible to capture a part of the log starting and ending.


# Concatenative (Language) Documents

This does not mean concatenating documents together. This means for the components on a page to work out what is possible to do on that page depending on the components.

# Ouruobos Test

In sites with complex flows, render all pages at once.

# Concurrent Interface

Interact with different versions of the same data in realtime. (Tabular, Outliner, Spreadsheet, Exploration)

# Query Edit

Treat the UI and the queries that generate the UI ojects as separated tools and projects.

# Smart Fields

Fields that understand various formats of data for dates etc. 'Tomorrow' 'yesterday', '15th March' '15/03/1990'

# Log Stream Processing

Render boxes to signify different things happening in a log.

# Flat Lists

Describe complicated nested data structures as flat lists:

Summarize complex objects with simple explanations of what they should be expanded to.

"2 adults"
ASTRAL commands

# Consultant Housing

# Flipangle

 * Put in business need, i.e, a cost
 * Then inside this cost, put in what it pays for
 * can flip using hierarchy swap
 
# A page request corresponds to a database in memory, just filled and emptied at different times


# Reverse templating/code matching

 * DOM structure -> converted into a different DOM structure


# Hierarchy Swap Map/Reduce

Collecting/manipulating data between similar tags

# Visual Queuing

Like the sims, when you click tasks that take a long period of time, they queue up.

# Visual Process map

Diagram of various steps on the screen like a map. If some steps can be completed in a different order then they are connected in a loop (criss crossed)

Should be styled like a London underground map but going left to right.

# In browser CSS fix

Tweak until fix, then persist style back to stylesheet on server.

# Semantic Text Lasso

# Multiple backends for data in a living document

insert data in dot, stored in Neo4j or SPARQL

# Computer holism

Computers from a birds eye view

# Form to database

# Living Document Architecture


 * Creating a context creates an unnamed HTTP resource and inserts a reference to it.
 
 - UX
   - Data rotation
     - Clicking 'Rotate' may change the orientation of data from portrait to landscape
     - Swiping left and right might change the visualisation of data
   - Automatic layouts
     - Bin packing place items on the screen
   - DOM Mutation
     - Shouldn't have to worry about creating complex animations or visualizations manually. Should be possible to just define the beginning and end states.
   - Semantic autocompletion
     - Depending on the position in a file or document, relevant actions should be 'offered'
   - Semantic Lasso
     - The ability to 'connect' things together by clicking or highlighting something and then dragging a line to another selection or click.  This might prompt for a definition of the connection.
   - Concurrent interface
     - The same data structure should be manipulatable by multiple 'live' editors.
     - Spreadsheet view, outline view
 - integration
   - I want people to feel empowered to start sharing and managing things in whatever way they think of.
     - Perhaps one day I feel like sharing a movie I just watched.
       - By doing this, I've actually created a category of information: 'just watched'.
       - How should a 'just watched' be displayed?
       - I create a 'template' or 'stencil' for how this should look. (the ability for everyone to create templates)
       - My friends receive the same information.
       - I specify that in response to my 'just watched' I want people to be able to 'comment',  'recommend'.
       - I decide to insert an image, I search for an image of the filmcover.
       - Whenever someone sees my feed or living document, they see the filmcover and my name.
     - Another day I have some interesting data on my terminal. I want to monitor it and share it with other people.
       - I pipe the output into a 'shellbucket'.
       - I can now manipulate the data and change how it might be displayed.
   - Should be possible to interact with a variety of ecosystems
   - Should distill the problems of forums, wikis, word processed documents to a flexible data structure
   - Integrate existing ecosystems
     - remotejs
     - unhosted
     - online fiddle websites - 'jsfiddle', 'dotnet fiddle'
     - code execution - REPLs
   - Enable quick use of package managers
     - bower
     - pip
     - rubygems
     - npm
     - corslit
   - HATEOAS
     - consume third party APIs
     - SOAP
 - collaboration
   - Existing social network attempt at https://github.com/fuz/socialnet
   - Multimedium social network
     - Simplified to a 'transit layer' where users could decide on how to actually share data perhaps over email, http, BitTorrent.
     - Packets should be extendable 

# Layered DB

 * Can we read a database output from the protocol into a more efficient data structure for local querying? Such as into redis?

# View generation and database query optimizer technology

Databases support many powerful mechanisms to make querying data more efficient. Can't we do the same on UIs?

Rather than querying for data, we would actually be querying for views. Views would be declarative.

If you know what will be rendered by a given application state, can you generate views (and data) more lazily and update it less frequently and with less code than what is traditionally required?

Based on how different one widget is to another, can you transform one into another more cheaply than construction one from scratch?

select page.state where event.type == 'keypress' and event.key == 'enter'
insert into todos set title = event.text
select * from todos
select * from todos where complete == true
select * from todos where complete == false





# DOT server

find way to pipe text to dot and stream the resulting svg


# Scan document

 * find new links
  * to create page shadows
 * find lists
 * generate dynamic assets inside the file
 * break up page into blocks

