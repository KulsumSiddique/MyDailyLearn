## Flexbox

### Controlling the Alignment of the Elements

#### justify-content

`justify-content: ` work on how the remaining space in the container will be distributed around the flex elements if there is any remaining spaces in the container

It accepts `5` values:

1. `flex-start (default)`: align items to the beginning of the flex-container
2. `flex-end: ` align items to the end of flex container
3. `center: ` centers the content inside the flex container
4. `space-between: ` separates the content with equal spaces with no spaces at the beginning or at the end of the container
5. 



#### Flex with Responsive

```css
@media screen and (min-width: 40em) {
  .cards {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-top: -1em;
  }

/*
  .card { 
  	flex: 0 1 33%;
  }
*/

  .card {
    display: flex;
    flex: 0 1 calc(50% - 0.5em); // use percentage, similar as widtch: calc(33% - 1em);
    margin-bottom: 1em;
  }
}

@media screen and (min-width: 60em) {
  .cards {
    margin-top: inherit;
  }
  .card {
    flex: 0 1 calc(33% - 1em);
    margin-bottom: 2em;
  }
}
```

#### Shrink a Div Horizontally and Add 3 Dots

```css
flex-grow: 1;
white-space: nowrap;
overflow: hidden;
text-overflow: ellipsis;
```

[Ref1](https://meetrix.io/blog/posts/shrink-a-div-horizontally-and-add-3-dots.html)

[Ref2](https://css-tricks.com/flexbox-truncated-text/)

#### Properties That Control Alignment

- [justify-content](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content) -- controls alignment of all items on the main axis (x-axis)
- [align-items](https://developer.mozilla.org/en-US/docs/Web/CSS/align-items) -- controls alignment of all items on the cross axis (y-axis)
- [align-self](https://developer.mozilla.org/en-US/docs/Web/CSS/align-self) -- controls alignment of an individual flex item on the cross axis
- [align-control](https://developer.mozilla.org/en-US/docs/Web/CSS/align-content) -- described in the spec as for `packing flex lines`. Controls space between flex lines on the cross axis