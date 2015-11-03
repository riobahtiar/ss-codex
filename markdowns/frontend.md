# Frontend Dev
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Commodi odio quas soluta error perspiciatis quisquam asperiores laboriosam nihil, quo illum suscipit consectetur vel, saepe ad. Dolore excepturi dolores perferendis, assumenda.


## General Guidelines
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Corporis quam, numquam voluptatem quod laboriosam facilis amet quisquam minima cupiditate suscipit mollitia eligendi vel quos quis obcaecati, ut veniam vitae nisi!

### Avoid Multiple Files
A lot of web development seems to be about splitting things up into manageable chunks or “components”. For each discrete bit of javascript functionality or each HTML partial I might make a dedicated file, then organize related files into folders named javascript and html or controllers and templates. Whatever you like. This way, you can easily dip into the file system and focus on just the file containing the code you want to edit at the time.

This doesn’t work so well for CSS. Javascript function definitions can go either before or after where they are called and HTML modules can be inserted wherever you see fit in the flow of the document. CSS, on the other hand, is a chronology. It matters a great deal in what order you declare styles. Heeding the language features of inheritance and specificity, you should start with generic styles (like a font-family set on body) and progress to more specific definitions.

CSS is an ordered, exception based language and there is no easy way for a file listing (which is typically organised alphabetically) to represent it coherently. It gives you the impression that each CSS file is autonomous, which it is not.

```
- buttons.css 
- reset.css
```

So you have two choices: You can either live in denial, grumbling that “specificity shouldn’t be part of CSS” as you try to force a square peg into a round hole, or you can work in one, well-commented file that clearly represents the arc of your inheritance-harnessing cascade. Specificity should never be a problem because the most specific selectors should be the last ones you write.

### Nesting
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Temporibus, molestiae.

## HTML
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur qui nobis, quos repellendus alias esse fugit placeat eius asperiores distinctio magni, doloremque pariatur dolor perferendis, totam animi architecto explicabo cum.

## CSS
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quasi deleniti error alias. Iusto itaque ipsum architecto illum in, labore, quo explicabo doloremque. Numquam quis sunt dignissimos ea, voluptatibus nesciunt officia?

## Javascript
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aspernatur eveniet culpa quisquam architecto distinctio fugit perspiciatis doloremque nobis aut consequatur impedit voluptas hic eum quos repellat, nesciunt voluptates dolore rem?

## Responsive Web Design
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Officiis, cumque.

### PX Unit
Managing sizes using pixels in responsive design is an absolute hog. The lack of relativity between separate elements’ sizes means you have to treat each setting as a separate concern, for each separate breakpoint. In fact, using pixels you even have to manage the font size and margin of single, isolated elements separately. You really don’t want to do that.

Take the following example:
```
@media (min-width: 400px) { 
  h1 { 
    font-size: 22px; 
    margin-top: 33px; 
  } 
}
```

How would we write that using relative units? We wouldn’t. In fact, we wouldn’t have to address font sizes or margins for any individual elements in any of our @media queries. We’d simply let the browser or user determine the font-size on the root element (<html>) and set all my other dimensions in ems or rems.

```
h1, h2 { margin-top: 1.5rem; } 
h1 { font-size: 2.5em; } 
h2 { font-size: 2em; } 
/* all your other element styles */
```

Then, when we wanted to scale things up at a min-width breakpoint, we’d just adjust the root font size, upon which everything else is proportionately based. I use a percentage value because this is relative to the user’s preference, if set:

```
@media (min-width: 400px) { /* "Should be ems too!" - lots of folks :-) */
  html { 
    font-size: 120%; 
  } 
}
```

That’s it. That’s 90% of your responsive design strategy right there. For bonus points, you can set a common margin between all your sibling flow elements using a selector.
body * + * { 
  margin-top: 1.5rem; 
}



## Performance
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cumque atque ipsum omnis explicabo modi iste autem saepe alias natus odit. Perspiciatis aliquam numquam corporis minima fugiat consequatur a sit. Incidunt.




## Testing 
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur autem voluptatum blanditiis in rem. Sapiente id perspiciatis earum mollitia quibusdam, fugit a officia! Eum optio est sed, quaerat quis dolor.


### Basic Checklist
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur autem voluptatum blanditiis in rem. Sapiente id perspiciatis earum mollitia quibusdam, fugit a officia! Eum optio est sed, quaerat quis dolor.

### Code Checklist
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur autem voluptatum blanditiis in rem. Sapiente id perspiciatis earum mollitia quibusdam, fugit a officia! Eum optio est sed, quaerat quis dolor.

### To Do List
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur autem voluptatum blanditiis in rem. Sapiente id perspiciatis earum mollitia quibusdam, fugit a officia! Eum optio est sed, quaerat quis dolor.