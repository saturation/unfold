# Notes for slides

1%%Here is our dear friend, the DOM Element.
1. Fade in a square, perhaps 200px.

Web design is a perpetual process of finding better ways of arranging DOM elements in the browser.

For so long, our only options were to float 1%%left or 2%%right
1. DE floats left
2. DE floats right

Or using a coordinate system with position.
1. DE moves up and down
2. DE moves left and right

However, all of the latest browsers have a new technology unlocking another dimension of possibility: CSS 3D Transforms.

Transforms let you move and rotate DOM elements along three axes of motion: 1%%4%%x, 2%%5%%y, and 3%%6%%z
1. DE moves along x axis (blue)
2. DE moves along y axis (green)
3. DE moves along z axis (red, use perspective)
4. DE rotates along x axis (blue, use perspective)
5. DE rotates along y axis (green, use perspective)
6. DE rotates along z axis (red, use perspective)

When combined with some settings that control perspective, you can create 3D figures out of regular DOM elements.

These perspective settings go on the container of the 3D elements.
1. {code} transform-style
2. {code} perspective - (animate the perspctive value on a 3D-transformed primitive)
3. {code} perspective-origin - (animate the perspctive value on a 3D-transformed primitive)

These transforms go on the element you want to transform
1. {code} translate
2. {code} rotate
3. {code} backface-visibility

Creating primitives

Since transforms are inherited by children, you can think of nested elements much like paper

Just align the two <code>transform-origin</code>s of nested elements to a common edge, and it "folds" like paper:
1. Show two DEs first in the same position then one folds 90° from a common edge
2. Now another folds out from the second, also 90°
3. The fourth folds out from the third, connecting to the first
4. The fifth folds out from the third, forming one side of the cube
5. The sixth folds out from the third, forming the other side and completing the cube
6. The first, second, and third joints open up more, revealing the "t" shape that an unfolded paper cube makes

You can simulate other more complex objects. This slinky is not a spiral, but numerous nested <code><div>s</code>
1. Demo slinky

You can superimpose transforms on top of real images
1. Demo tile

Combining with other CSS
1. Demo blur filter

DOM elements can be enhanced by JavaScript. Just write <code><span class="cube"></span></code> in your markup and have your script add [bottom, left, right, front, back] edges.
1. Make various minecraft blocks out of really simple markup+classes
2. *Maybe* make it so clicking a surface generates the new block on that surface

Playtime!
Set up a holodeck-type thing and offer six textfields to let the user transform a cube

The end

# Todos

- blur filter: convert to Sass, add real 3d perspctive and shift perspective origin based on cursor position
