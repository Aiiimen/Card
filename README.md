# Card

>*Three Different hover animation applied to cards using shapes and translate options.*

A card is a flexible and extensible content container. It includes options for headers and footers, a wide variety of content, contextual background colours, and powerful display options.
For this project – I used 3 cards to display different content that can be used by an agency to help get illustrators, designers and developers jobs. 
The card holds a title, description, CTA to hire them and an illustration that animates when the user is on a hover state. 



#### Tools and Assets Used
---

- Fonts: Staatliches & Roboto Mono
- colour Pallete: #FFCC4C, #61DFAD, #EF334A
- Illustrations: [humaaans](https://www.humaaans.com/)

---

#### The HTML Structure
The structure of the card is broken down into 4 *divs*. These are children of **.card**. 
The first element **.card-text** contains the title and description. **.card-image** contains the illustration itself and lastly, **.circle** is a div that it styled into different shapes.

```html
<div class="card">
    <div class="card-text">
      <h1> illustrators </h1>
      <p> hire a selection of award winning illustrators. </p>
      <a href="."> hire now </a>
    </div>
    <div class="card-image">
      <img src="assets/images/standing-16.png" />
    </div>

    <div class="circle circle-illustrators"></div>
  </div>
```

#### Styling 
The card is a rectangle shape achieved by setting the *height* to *640px* and *width* to *440px*. As the animation will held inside of **.card** it is important to set its *position* to *relative* and set *overflow* to *hidden*.

```css
.card{
  position: relative;
  width: 44px;
  height: 640px;
  overflow: hidden;
}
```
#### Illustrators: on hover
The shape of the first is a circle that *scales* x 15 upon hover and changes the *opacity* to *1* from *0.5*. A *transition* of *ease-in-out* was applied to the *transform* for smoother effect.

``` css
transition: all 400ms ease-in-out

```

``` css
.circle:hover{
  transform: scale(15);
  opacity: 1;
}
```

#### Designers: on hover
The designer card is a square was achieved by setting the *border-radius* to *0*. Same *transform* was applied to the element upon hover. 

``` css
.circle-designers{
  background-color: #61DFAD;
  border-radius: 0;
}

```

#### Developers: on hover
The animated element for developers card was *rotated* by *45 deg*. Upon *transition* the rotated shape will *scale* and at the same time with *rotate* back to *0 degrees* with *400ms*.

``` css
.circle-developers{
  background-color: #EF334A;
  transform: rotate(45deg);
  border-radius: 0;
  }
```












