# \<dom-custom-repeat\>


## Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your element locally.

## Example

```js
static get properties() {
  return {
    users: {
      type: Array,
      value: [{name: 'Someone'}]
    }
  };
}
```

```html
<ul>
    <dom-custom-repeat items="[[users]]" as="user">
        <template>
            <li>[[user.name]]</li>
        </template>
    </dom-custom-repeat>
</ul>
```


```html
<ul>
    <li>
        Someone
    </li>
</ul>
```

## Viewing Your Element

```
$ polymer serve
```

## Properties

### items

Define the array to iterate

### as

Define the model for the element iteration

### indexAs

Define the model for the index iteration


## Methods

### render

Force to render the template

## Events

### dom-changed

Dispatched when the items changed, and return the new array in detail.
