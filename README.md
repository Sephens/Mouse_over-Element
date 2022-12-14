# Mouseover Element
![Image](assets/img1.png)
1. You’ll see how JavaScript functions work and practice your JavaScript logic
2. It’s a fun beginner JavaScript project to do to liven up your user experience
3. Learn more about using random, functions, and event listeners.

Visit this site for see how it works: [visit-site](http://verdant-side.surge.sh)

### Key concepts covered:
1. Functions and if-else statements
2. Random
3. Event listeners

## Document.getElementById()
* The Document method `getElementById()` returns an Element object representing the element whose id property matches the specified string. 
* Since element IDs are required to be unique if specified, they're a useful way to get access to a specific element quickly.
__Syntax:__ `getElementById(id)`

### Parameters
__id__
>> The ID of the element to locate. The ID is case-sensitive string which is unique within the document; only one element may have any given ID.

### Return value
>> An Element object describing the DOM element object matching the specified ID, or null if no matching element was found in the document.


* If you need to get access to an element which doesn't have an **ID**, you can use `querySelector()` to find the element using any selector.

## HTMLCanvasElement.getContext()
* The HTMLCanvasElement.getContext() method returns a drawing context on the canvas, or null if the context identifier is not supported, or the canvas has already been set to a different context mode.

__Syntax__:
`getContext(contextType)`
`getContext(contextType, contextAttributes)`

`contextType`
* A **string** containing the context identifier defining the drawing context associated to the canvas. Possible values are:

* **`"2d",`** leading to the creation of a CanvasRenderingContext2D object representing a two-dimensional rendering context.
* **`"webgl"`** (or "experimental-webgl") which will create a WebGLRenderingContext object representing a three-dimensional rendering context. This context is only available on browsers that implement WebGL version 1 (OpenGL ES 2.0).
* **`"webgl2"`** which will create a WebGL2RenderingContext object representing a three-dimensional rendering context. This context is only available on browsers that implement WebGL version 2 (OpenGL ES 3.0). Experimental
* **`"bitmaprenderer"`** which will create an ImageBitmapRenderingContext which only provides functionality to replace the content of the canvas with a given ImageBitmap.

### contextAttributes __Optional__
You can use several context attributes when creating your rendering context, for example:

`const gl = canvas.getContext("webgl", {
  antialias: false,
  depth: false,
});`

#### 2d context attributes:

`alpha`
A boolean value that indicates if the canvas contains an alpha channel. If set to false, the browser now knows that the backdrop is always opaque, which can speed up drawing of transparent content and images.

`colorSpace` __Optional__
Specifies the color space of the rendering context. Possible values are:

`"srgb"` selects the sRGB color space. This is the default value.
"display-p3" selects the display-p3 color space.
desynchronized
A boolean value that hints the user agent to reduce the latency by desynchronizing the canvas paint cycle from the event loop

`willReadFrequently`
A boolean value that indicates whether or not a lot of read-back operations are planned. This will force the use of a software (instead of hardware accelerated) 2D canvas and can save memory when calling getImageData() frequently.

#### WebGL context attributes:

`alpha`
A boolean value that indicates if the canvas contains an alpha buffer.

`depth`
A boolean value that indicates that the drawing buffer is requested to have a depth buffer of at least 16 bits.

`stencil`
A boolean value that indicates that the drawing buffer is requested to have a stencil buffer of at least 8 bits.

`desynchronized`
A boolean value that hints the user agent to reduce the latency by desynchronizing the canvas paint cycle from the event loop

`antialias`
A boolean value that indicates whether or not to perform anti-aliasing if possible.

failIfMajorPerformanceCaveat
A boolean value that indicates if a context will be created if the system performance is low or if no hardware GPU is available.

`powerPreference`
A hint to the user agent indicating what configuration of GPU is suitable for the WebGL context. Possible values are:

`"default"`
Let the user agent decide which GPU configuration is most suitable. This is the default value.

`"high-performance"`
Prioritizes rendering performance over power consumption.

`"low-power"`
Prioritizes power saving over rendering performance.

`premultipliedAlpha`
A boolean value that indicates that the page compositor will assume the drawing buffer contains colors with pre-multiplied alpha.

`preserveDrawingBuffer`
If the value is true the buffers will not be cleared and will preserve their values until cleared or overwritten by the author.

`xrCompatible`
A boolean value that hints to the user agent to use a compatible graphics adapter for an immersive XR device. Setting this synchronous flag at context creation is discouraged; rather call the asynchronous WebGLRenderingContext.makeXRCompatible() method the moment you intend to start an XR session.

### Return value
* A rendering context which is either a
`CanvasRenderingContext2D `for `"2d"`,
`WebGLRenderingContext` for `"webgl"` and `"experimental-webgl"`,
`WebGL2RenderingContext`for `"webgl2"` or
`ImageBitmapRenderingContext` for `"bitmaprenderer"`.
* If the contextType doesn't match a possible drawing context, or differs from the first contextType requested, null is returned.

## window.innerWidth;
* The *read-only Window property* `innerWidth` returns the interior width of the window in pixels. This includes the width of the vertical scroll bar, if one is present.
* More precisely, `innerWidth` returns the width of the window's layout **viewport**. The interior height of the window—the height of the layout viewport—can be obtained from the innerHeight property.
>> #### Layout viewport
>> The layout viewport is the viewport into which the browser draws a web page. Essentially, it represents what is available to be seen, while the visual viewport represents what is currently visible on the user's display device.

### Math.ceil()
* The Math.ceil() function always rounds up and returns the smaller integer greater than or equal to a given number. `Math.ceil(x)`

### Math.round()
* The Math.round() function returns the value of a number rounded to the nearest integer. `Math.round(x)`

### Math.floor()
* The Math.floor() function always rounds down and returns the largest integer less than or equal to a given number.

### Math.random()
* The Math.random() function returns a floating-point, pseudo-random number that's greater than or equal to 0 and less than 1, with approximately uniform distribution over that range — which you can then scale to your desired range. The implementation selects the initial seed to the random number generation algorithm; it cannot be chosen or reset by the user.








