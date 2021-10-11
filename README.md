# Vue Js Commands


## DIRECTIVES
COMMAND | DESCRIPTION
------------ | -------------
<code>v-text</code> | uses the property as the text value of the element
<code>v-html</code> | uses the property as the text value of the element, interpreting HTML
<code>v-if</code> | show an element only if the conditional is true
<code>v-else</code> | shows an alternative element if the preceding v-if is false
<code>v-else-if	</code> | adds an else if block for a v-if construct
<code>v-show</code> | similar to v-if, but adds the element to the DOM even if falsy. Just sets it to display: none.
<code>v-for</code> | iterates over an array or iterable object
<code>v-on</code> | listen to DOM events
<code>v-bind</code> | reactively update an HTML attribute
<code>v-model</code> | sets up a two-way binding for form inputs. used in form elements, updates the model when the user changes the form field value
<code>v-once</code> | applies the property just once, and never refreshes it even if the data passed changes


<code>v-bind</code> and <code>v-on</code> have a shorthand format:
```git
<a v-bind:href="url">...</a>
<a :href="url">...</a>
```

```git
<a v-on:click="doSomething">...</a>
<a @click="doSomething">...</a>
```

## CONDITIONALS
You can embed a conditional in an expression using the ternary operator:
```git
{{ isTrue ? 'yes' : 'no' }}
```

## Working with form elements
To make the model update when the change event occurs, and not any time the user presses a key, you can use <code>v-model.lazy</code> instead of just <code>v.model</code>.

Working with input fields, <code>v-model.trim</code> is useful because it automatically removes whitespace.

And if you accept a number instead than a string, make sure you use <code>v-model.number</code>.


## Modifying events
I use <code>click</code> as an example, but applies to all possible events

<code>v-on:click.native</code> trigger a native DOM event instead of a Vue event
<code>v-on:click.stop</code> stop the click event propagation
<code>v-on:click.passive</code> makes use of the passive option of addEventListener
<code>v-on:click.capture</code> use event capturing instead of event bubbling
<code>v-on:click.self</code> make sure the click event was not bubbled from a child event, but directly happened on that element
<code>v-on:click.once</code> the event will only be triggered exactly once
<code>v-on:submit.prevent</code>: call <code>event.preventDefault()</code> on the triggered submit event, used to avoid a form submit to reload the page


## Mouse event modifiers
<code>v-on:click</code> .left triggers only on left mouse button click
<code>v-on:click</code> .right triggers only on right mouse button click
<code>v-on:click</code> .middle triggers only on middle mouse button click


## Submit an event only if a particular key is pressed
<code>v-on:keyup.enter</code>
<code>v-on:keyup.tab</code>
<code>v-on:keyup.delete</code>
<code>v-on:keyup.esc</code>
<code>v-on:keyup.up</code>
<code>v-on:keyup.down</code>
<code>v-on:keyup.left</code>
<code>v-on:keyup.right</code>


## Keyboard event modifiers
Only trigger the event if a particular keyboard key is also pressed:

<code>.ctrl</code>
<code>.alt</code>
<code>.shift</code>
<code>.meta</code> (cmd on Mac, windows key on Win)

v-bind

<code>v-bind .prop </code>bind a prop instead of an attribute
<code>v-bind .camel</code> use camelCase for the attribute name
<code>v-bind .sync </code>a syntactic sugar that expands into a <code>v-on</code> handler for updating the bound value.


## Lifecycle Hooks
<code>beforeCreate</code> called before the app is created
<code>created</code> called after the app is created
<code>beforeMount</code> called before the app is mounted on the DOM
<code>mounted</code> called after the app is mounted on the DOM
<code>beforeDestroy</code> called before the app is destroyed
<code>destroyed</code> called after the app is destroyed
<code>beforeUpdate</code> called before a property is updated
<code>updated</code> called after a property is updated
<code>activated</code> called when a kept-alive component is activated
<code>deactivated</code> called when a kept-alive component is deactivated


## Built-in components
Vue provides 5 built-in components:

<code><component></code>
<code><transition></code>
<code><transition-group></code>
<code><keep-alive></code>
<code><slot></code>
  
  

