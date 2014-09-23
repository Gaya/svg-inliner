SVG-inliner
===========
Creates inline HTML <svg> from an external SVG (sprite) in an <img /> tag.

It extracts the correct SVG element from an SVG sprite if the child's id is put after a `#` in the `src` attribute of
the image.

Install
-------
If you want to use SVG inliner in node.js and include with CommonJs:

    npm install svg-inliner

Or download the `svg-inliner.js` JavaScript file in the root and place in your project.

Single file usage
-----------------

Consider the following HTML:

    <img id="svg-image" src="path/to/svg.svg" />

Apply SVG-inliner with the following JavaScript:

    new SVGInliner(document.querySelectorAll("#svg-image"));

SVG Sprite usage
----------------

Image tag in HTML with id of targeted element:

    <img id="svg-sprite" src="path/to/svg-sprite-file.svg#id-of-element" />

Use the following JavaScript to get the targeted child of the sprite:

    new SVGInliner(document.querySelectorAll("#svg-sprite"));