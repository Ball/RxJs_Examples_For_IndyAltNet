This is all about explaining Reactive programming in a short amount of time.

# Why is this important to me?

Reactive programming makes events and callbacks composable.  Events are composed in to streams that can be manipulated, filtered, combined, and controlled.

# What are the demos?

## Search Wikipedia

### A Simple event handler

We wire up to the search input textbox and wait for the text to change

### Throtteling

We don't want to send a new search until the user is done typing.

### Async Request

We set up an asynchronous request and monitor the results

### Picking only the response from the most recent request

If I search Re, Reac, and Reactive and the last response is from the first request, my results display will show stale data.  How does Research get returned from Reactive?

## Drawing on a canvas

### Manipulating the event stream

To draw, we need a list of segments.  Mouse move events won't work.  We'll use Zip and Select to update the stream of move events to a stream of line segments

### Combining events

To draw, we only care about move events while the mouse is down.  In addition, we need a clear seperation between streams so we don't link two seperate lines.

