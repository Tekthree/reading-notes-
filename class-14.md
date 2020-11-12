# Reading Notes
### class 14


## What google learned from its quest to build the perfect team

- analysing and improving individual workers is a practice known as "employee performance optimization"

- Havard business review found that the time spent by managers and employees in collaborative activities had ballooned by 50 percent over the last two decades

- Silicon Valley, software engineers are encouraged to work together, because studies show that groups tend to innovate faster

- It was almost impossible to find any evidence that the composition of a team made any difference. 

- No strong patterns for top performing groups

- Researchers concluded that what distinguished the good teams from the dysfunctional groups was how teammates treated one another

- good teams, members spoke in roughly the same proportion

- As long as everyone got a chance to talk, the team did well

- the good teams all were skilled at intuiting how others felt based on their tone of voice, their expressions and other nonverbal cues.


## CSS transforms 

- CSS3 brought in new ways to position elements. Now general layout techniques can be revisited with alternative ways to size, position, and change elements

- The transform property comes in two different settings, two-dimensional and three-dimensional

```
div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}
```

- Elements may be distorted, or transformed, on both a two-dimensional plane or a three-dimensional plane

- transform property accepts a handful of different values. Rotate value provides the ability to rotate an element from 0 to 360 degrees

```
.box-1 {
  transform: rotate(20deg);
}
.box-2 {
  transform: rotate(-55deg);
}
```

- As previously mentioned, the default transform origin is the dead center of an element, both 50% horizontally and 50% vertically

```
.box-1 {
  transform: rotate(15deg);
  transform-origin: 0 0;
}
.box-2 {
  transform: scale(.5);
  transform-origin: 100% 100%;
}
.box-3 {
  transform: skewX(20deg);
  transform-origin: top left;
}
.box-4 {
  transform: scale(.75) translate(-10px, -10px);
  transform-origin: 20px 50px;
}
```

- fade in effect

```
.fade
{
        opacity:0.5;
}
.fade:hover
{
        opacity:1;
}

```

- change color

```
.color:hover
{
        background:#53a7ea;
}
```

- grow and shrink

```
.grow:hover
{
        -webkit-transform: scale(1.3);
        -ms-transform: scale(1.3);
        transform: scale(1.3);
}

```


- square to circle

```
.circle:hover
{
        border-radius:50%;
}

```


-
