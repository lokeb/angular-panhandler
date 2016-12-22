![pannable](https://lokeb.github.io/angular-pannable/images/brand.jpg)
==================

<p align="center" style="text-align: center;">
    <img src="https://lokeb.github.io/angular-pannable/images/demo.gif" alt="Demo"/>
</p>

Pan Directive for Angular.js - Drag to scroll behavior

### [Documentation](https://lokeb.github.io/angular-pannable/)

### Usage

Add ```pannable``` as an attribute to the element on which you would like to enable panning.  Thats it!  If you would like to make sure your inner content fits to a certain size, you can specify a ```pannable-content-{width|height}``` attribute.


### Advanced Usage

If you need to disable panning (temporarily) for some of the content elements,
you can set the `pannable-preventPan` attribute on the pannable element to true.

This is useful in the case that you would like to enable drag-n-drop
for some elements within the pannable area.

### Example

Javascript

```javascript
angular.module('pannableExamples', ['pannable'])
    .controller('Example1', function Example1($scope) {
      $scope.gridItems = generateGrid(30);
    });
```

HTML

```html
<div ng-app="pannableExamples">
  <div ng-controller="Example1">
    <div class="container">
      <div pannable pannable-content-width="100em">
        Stuff to pan around!
      </div>
    </div>
  </div>
</div>
```

### Prevent Example

HTML

```html
<div ng-app="pannableExamples">
  <div ng-controller="Example1">
    <input name="preventPan" type="checkbox" ng-model="preventPanCheck" />
    <label for="preventPan">Prevent Panning</label>
    <div class="container">
      <div pannable content-width="100em" pannable-prevent-pan="{{ preventPanCheck }}">
        Stuff to pan around!
      </div>
    </div>
  </div>
</div>
```

### Prevent Pan on item

HTML

```html
<div ng-app="pannableExamples">
  <div ng-controller="Example1">
    <input name="preventPan" type="checkbox" />
    <label for="preventPan">Prevent Panning</label>
    <div class="container">
      <div pannable content-width="100em">
        <div class="iDoNotWantToScroll iCannotScroll"></div>
      </div>
    </div>
  </div>
</div>
```

### Add an Initial Pan for X and Y Axes

HTML

```html
<div ng-app="pannableExamples">
  <div ng-controller="Example1">
    <input name="preventPan" type="checkbox" />
    <label for="preventPan">Prevent Panning</label>
    <div class="container">
      <div pannable content-width="100em" pannable-offset-x="-20em" pannable-offset-y="-10em">
        <div class="iDoNotWantToScroll iCannotScroll"></div>
      </div>
    </div>
  </div>
</div>
```

### Development

For development, you will need node.js installed.

After that, run the following from the repo directory

```bash
npm install grunt-cli bower -g
npm install
bower install
grunt
```

Should get you going!


### License

MIT License


### Contributors and Acknowledgements

Thanks goes out to the creator of original project [panhandler](https://github.com/nnnnathann/angular-panhandler).
