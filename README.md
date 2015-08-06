# MDN WebGL

A collection of [WebGL](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API) utility functions to make it easier to explain code examples. The focus on these functions is clarity of communication over speed. 

## Content Kits

The following content kits use this collection of functions:

 * [Matrix Math for the Web](https://github.com/tatumcreative/mdn-matrix-math)
 * [Model View Projection](https://github.com/tatumcreative/mdn-model-view-projection)
 * [Lighting Models](https://github.com/tatumcreative/mdn-lighting-models)
 
## Performance Caveats

JavaScript written for realtime graphics tends to be written a little bit different than typical JavaScript. Memory allocation and garbage collection isn't normally as big of a deal in a more static application, but a WebGL visualization typically updates at 60 frames per second. At this rate any memory allocation comes with a cost and can create stutters in the frame rate when it is garbage collected.

These code samples do not take this into account for the sake of code clarity. For instance when working with matrices it's better to allocate the arrays beforehand, and re-use them, or swap between scratch arrays. The matrix operations should work on a target array rather than generate a new one. For a library that works this way check out [glMatrix](http://glmatrix.net/).

## Contributions

Pull requests are welcomed for any needed additions for MDN documentation.