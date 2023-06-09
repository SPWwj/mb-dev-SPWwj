<frontmatter>
  title: The Adventurer's Handbook to MarkBind
  layout: default.md
  pageNav: 4
  pageNavTitle: "Explorations"
</frontmatter>

<br>

<div class="px-2 py-5 mb-4 border-red">
  <div class="container">
    <h1 class="display-5 no-index">Greetings, Adventurers!<br>
    Prepare for your journey
    </h1>
    <p class="lead">Let the adventure begin...</p>
  </div>
</div>

---

# What just happened?

Congratulations, adventurer! You've just opened your _default_ ==#r#MarkBind## travel pack==. It's equipped with a set of navigation tools, including site and page navigation. We've also included a map to our User Guide to help you embark on your journey swiftly and smoothly.

<box type="tip">

Converting an existing explorer's diary or a docs folder into MarkBind? Use the `--convert` flag. Refer to the <a href="https://markbind.org/userGuide/markBindInTheProjectWorkflow.html#converting-existing-project-documentation-wiki" target="_blank">User Guide: MarkBind in the Adventure Workflow</a> for guidance.

If you prefer to start with a _minimal_ <tooltip content="i.e. with bare necessities">pack</tooltip>, use the `--template` flag with the "minimal" option. See <a href="https://markbind.org/userGuide/templates.html" target="_blank">User Guide: Templates</a> for instructions.

</box>

---

# Navigating your journey

Your _default_ travel pack comes pre-configured with core <a href="https://markbind.org/userGuide/components/navigation.html#navigation-components" target="_blank">Navigation tools</a>: a <tooltip content="Site Navigation">**siteNav**</tooltip>, a <tooltip content="Page Navigation">**pageNav**</tooltip>, a <tooltip content="Navigation Bar">**NavBar**</tooltip>, and a **Search Bar**. We've included <tooltip content="Landmark 1, Landmark 2, Landmark 3, Landmark 3a, Landmark 3b">five dummy landmarks</tooltip> to aid you. The **NavBar** also comes with a placeholder for your custom compass.

---

# Guide to MarkBind

Feel free to explore some of the maps built using MarkBind on our <a href="https://markbind.org/showcase.html" target="_blank">Showcase</a> page.

For instructions on navigating MarkBind sites and adding discoveries, refer to our comprehensive <a href="https://markbind.org/userGuide/gettingStarted.html" target="_blank">User Guide</a>. 

<box type="info">

Interested in contributing to MarkBind? Take a look at our <a href="https://markbind.org/devdocs/devGuide/devGuide.html" target="_blank">Developer Guide</a>!

</box>

<!-- <audio controls>
  <source src="mySong.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio> -->

<panel header="**Great beginnings in our User Guide**" expanded no-close>

##### **User Guide: Crafting Tales**

> Discover the variety of syntax schemes, formats, and custom MarkBind components that you can use in your MarkBind narrative.

More info in: _<a href="https://markbind.org/userGuide/authoringContents.html" target="_blank">User Guide → Crafting Tales</a>_

---

##### **User Guide: Journey Management**

> Learn how to modify journey properties, apply themes, and enable/disable magical aids for your MarkBind journey.

More info in: _<a href="https://markbind.org/userGuide/workingWithSites.html" target="_blank">User Guide → Journey Management</a>_

---

##### **User Guide: Full Syntax Reference**

> Refer to our Full Syntax Reference page to find a specific feature or component that you want to use in your MarkBind journey.

More info in: _<a href="https://markbind.org/userGuide/fullSyntaxReference.html" target="_blank">User Guide → Full Syntax Reference</a>_

</panel>

---
---

---

## Code: Map Configuration Example :earth_americas:

In the realm of digital exploration, code plays an essential role. MarkBind supports code snippets in various languages, enhancing the clarity of your guidelines or demonstrations. :+1:

Let's take a look at an XML configuration for a hypothetical map system:

```xml
<MapConfig>
  <Map type="world">
    <Name>Earth</Name>
    <Scale>1:50000000</Scale>
  </Map>
  <Markers>
    <Marker>
      <Name>BaseCamp</Name>
      <Coordinates>38.9072 N, 77.0369 W</Coordinates>
    </Marker>
    <Marker>
      <Name>Destination</Name>
      <Coordinates>27.9881 N, 86.9250 E</Coordinates>
    </Marker>
  </Markers>
</MapConfig>

```
<quiz>
  <question type="mcq">...</question>
  <question type="checkbox">...</question>
  <question type="blanks">...</question>
  <question type="text">...</question>
</quiz>
---
<qr-code 
    data="https://spirify.azurewebsites.net"
    size="10"
    margin="4"
    ec-level="H"
    color="red"
    background="white"
    type="svg"
    alt="Spirify QR Code"
    caption="Spirify QR Code"
    style="width:100%;height:100%;border:2px solid black;"
></qr-code>

## Adventure Essentials :mountain:

<box>
  This is your _default_ kit for the journey.
</box>

<box type="info">
  The info kit contains important informational scrolls.
</box>

<box type="warning">
  The warning kit has flares for alerting your team of potential dangers.
</box>

<box type="success">
  The success kit includes your rewards for successful expeditions.
</box>

<box type="important">
  The important kit carries crucial items that should never be left behind.
</box>

<box type="wrong">
  The wrong kit is a collection of failed attempts, reminding you of what to avoid.
</box>

<box type="tip">
  The tip kit gives you valuable advice for your exploration journey.
</box>

<box type="definition">
  The definition kit explains unfamiliar terms and signs you might encounter.
</box>

<box type="info" dismissible>
  The dismissible info kit includes facts that are nice to know but not crucial. Feel free to dismiss them if you are familiar.
</box>
<box type="success" header="#### Expedition Achievements :rocket:" icon-size="2x">
These are your accolades for surviving the toughest challenges and solving the most complex puzzles during your journey.

  <box type="warning" header="Remember, your journey is not over! Keep exploring! :pizza:" dismissible>
  You have conquered many challenges, but the world is vast and filled with untamed mysteries waiting for you.
  </box>
</box>


---

<panel header="Explorers Logbook, click to review!">
  Document your daily adventures, findings, encounters here...
</panel>

---

Your journey status:

<span class="badge bg-primary">Primary Objective</span>
<span class="badge bg-secondary">Secondary Task</span>
<span class="badge bg-success">Success Mark</span>
<span class="badge bg-danger">Danger Warning</span>
<span class="badge bg-warning text-dark">Caution Needed</span>
<span class="badge bg-info text-dark">Info Update</span>
<span class="badge bg-light text-dark">Minor Note</span>
<span class="badge bg-dark">Night Mode</span>
<br>Expedition Levels:
<span class="badge rounded-pill bg-primary">Level 1</span>
<span class="badge rounded-pill bg-secondary">Level 2</span>
<span class="badge rounded-pill bg-success">Level 3</span>
<span class="badge rounded-pill bg-danger">Level 4</span>
<span class="badge rounded-pill bg-warning text-dark">Level 5</span>
<span class="badge rounded-pill bg-info text-dark">Level 6</span>
<span class="badge rounded-pill bg-light text-dark">Level 7</span>
<span class="badge rounded-pill bg-dark">Level 8</span>

---
