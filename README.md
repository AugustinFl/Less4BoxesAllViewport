# Less4BoxesAllViewport

Exercise 1)

- Solution a using nth-child(n) selector and positioning:<br> 
    position: fixed;<br>
    top: 0; left: 0<br>
    top: 0; right: 0<br>
    bottom: 0; left: 0<br>
    bottom: 0; right: 0<br>

- Solution b - improvement to use only top and left<br>
    top: 0; left: 0<br>
    top: 0; left: 50%<br>
    top: 50%; left: 0<br>
    top: 50%; left: 50%<br>

Less approach:<br>
- Solution c - implementing mixins<br>
.mixin(@top: 0; @left: 0;) {<br>
            top: @top;<br>
            left: @left;<br>
}<br>
And then calling it for each child:<br>
    .mixin();
    .mixin(0,50%);<br>
    .mixin(50%,0);<br>
    .mixin(50%,50%);<br>
