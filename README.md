# Code2English
Code2English helps developers, UX designers and others fill in data shipped with code with a better natural language.

It simply ingests your *SQL code* and *HTML* and produces a better HTML or *plain sentences*.

It better would be multilingual, because why not ? 

Technically, it is a tiny JS standalone (browser) app, that scans a SQL or an HTML file, detects *input fields* with their *types* and finally suggests sentences to be put for final users.

Technically, again, it uses regex to discover:

- Input tags in HTML and based on a simple logic, propose a sentence
- And the same goes for SQL columns. Sentences suggested would be used everywhere you want later in any form of application (back-end or front-end)

In instance a boolean type of input like a radio box, would be interpreted as: *Do you like A or B*
The thing is simple, here is an example:

Having this HTML code:

```
Show Checkboxes
<form action="/action_page.php">
  <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">
  <input type="checkbox" id="vehicle2" name="vehicle2" value="Car">
  <input type="checkbox" id="vehicle3" name="vehicle3" value="Boat">
  <input type="submit" value="Submit">
</form>
```

--- Code2English suggests the followings ---

```
Show Checkboxes
<form action="/action_page.php">
  <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">
  <label for="vehicle1"> I have a bike</label><br>
  <input type="checkbox" id="vehicle2" name="vehicle2" value="Car">
  <label for="vehicle2"> I have a car</label><br>
  <input type="checkbox" id="vehicle3" name="vehicle3" value="Boat">
  <label for="vehicle3"> I have a boat</label><br><br>
  <input type="submit" value="Submit">
</form>
```

---OR---

```
Show Checkboxes
<form action="/action_page.php">
  <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">
  <label for="vehicle1"> I choose a bike</label><br>
  <input type="checkbox" id="vehicle2" name="vehicle2" value="Car">
  <label for="vehicle2"> I choose a car</label><br>
  <input type="checkbox" id="vehicle3" name="vehicle3" value="Boat">
  <label for="vehicle3"> I choose a boat</label><br><br>
  <input type="submit" value="Submit">
</form>
```
...

## todo:

Everything is in progress and nothing is pushed yet except this readme.

- build essential regex expressions to detect tags
- build an AI to suggest sentences, and wrap them in HTML
- build a UI for this


