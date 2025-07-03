# On the Elegance of Recursive Growth

> "Simplicity is prerequisite for reliability." — E.W. Dijkstra

This project demonstrates what happens when mathematics meets computation in its purest form: a fractal tree that grows through the simple act of recursion. Like all beautiful algorithms, it does exactly one thing and does it perfectly.

## The Algorithm

At its heart lies a deceptively simple recursive function:

```javascript
function branch(len) {
  line(0, 0, 0, -len);
  translate(0, -len);
  
  if (len > 10) {
    rotate(angle);
    branch(len * lengthFactor);
    rotate(-2 * angle);
    branch(len * lengthFactor);
  }
}
```

From this elementary building block emerges complexity that would be impossible to describe imperatively. Each branch spawns two children, each smaller than its parent by a constant factor. The angle oscillates with time, creating a living, breathing organism that demonstrates the profound truth that simple rules can generate infinite complexity.

## The Beauty

What makes this particularly elegant is not what it does, but what it doesn't do. There are no special cases, no edge conditions, no state to manage. The tree grows naturally from the mathematics of the problem itself. The recursion terminates when branches become too small to matter, and the animation emerges from a single changing parameter.

The visual result is a tree that sways in an imaginary wind, its branches reaching toward a sky that exists only in the mathematics of sine waves and recursive calls.

## Running

Open `fractal.html` in any modern browser. The tree will appear immediately, growing from the bottom of the screen, demonstrating that the most profound ideas often require the least explanation.

*"The competent programmer is fully aware of the strictly limited size of his own skull; therefore he approaches the programming task in full humility."* — E.W. Dijkstra
