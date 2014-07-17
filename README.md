jquery.scrolly
================

Overlay scrollbar for jQuery.

### Usage Example

Just add `data-scrolly="y"` to the element that you would like to have add an vertical overlay scrollbar on. The axis value can be `x`, `y`, or `xy`, e.g.

```
data-scrolly="x"  // Only horizontal scrollbar
data-scrolly="y"  // Only vertical scrollbar
data-scrolly="xy" // Both horizontal and vertical scrollbar's
data-scrolly      // Both horizontal and vertical scrollbar
```

### How does it work?

Scrolly will be initialized on mouseover and wraps the content of your element in the following html structure to produce the overlay scrollbar.

##### Before

    <div data-scrolly>
    	<h3>Heading</h3>
	    <p>My content</p>
	</div>

##### After
	    
    <div data-scrolly>
	    <div data-scrolly-viewport>
		    <h3>Heading</h3>
    		<p>Content</p>
	    </div>
    	<s data-axis="x"></s>
	    <s data-axis="y"></s>
    </div>

### No manual refresh needed

Scrolly listens to the `DOMSubtreeModified` and `propertychange` event on its child content and automatically updates the scrollbar width, height and position.

### Methods

All the methods below can be invoked through `$(el).scrolly(methodName, arg1, arg2, ...);`.

**update** (dx, dy, fromScrollbar)

Update the scroll position of the viewport. `dx` or `dy` reflects the changes of the horizontal or vertical scroll position of the viewport.

If `fromScrollbar` is set to `true`, `dx` and `dy` will be based on the scrollbar's position instead of the viewport's scroll position.

**axis** (mode)

Sets or gets the current axis. Values of `mode` can be `x`, `y` or `xy`.

**viewport**

Returns the viewport element.

**x** 

Returns the horizontal scrollbar.

**y** 

Returns the vertical scrollbar.

**enable** 

Enables overlay scrollbar.

**disable** 

Disables overlay scrollbar.

**reset** 

Destroy and reinitialize overlay scrollbar.


### License
Dual licensed under the [MIT](http://www.opensource.org/licenses/mit-license.php) and [GPL](http://www.gnu.org/licenses/gpl.html) licenses.

Plugin written by [Jensen Tonne](mailto:jensen.tonne@gmail.com).
