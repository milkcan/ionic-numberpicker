##Introduction:

This is a `ionic-numberpicker` bower component which can be used with any Ionic framework's application.

It is based on the 'ionic-timepicker' and 'ionic-datepicker' by https://github.com/rajeshwarpatlolla 


##Prerequisites.

1) node.js, npm, ionic, bower and gulp.

##How to use:

1) In your project repository install the ionic time picker using bower

`bower install ionic-numberpicker --save`

2) Give the path of  `ionic-numberpicker.bundle.min.js` in your `index.html` file.

````html
<!-- path to ionic/angularjs js -->
<script src="lib/ionic-numberpicker/dist/ionic-numberpicker.bundle.min.js"></script>
````    

3) In your application module inject the dependency `ionic-numberpicker`, in order to work with the `ionic-numberpicker` component

````javascript
angular.module('modulename', ['ionic', 'ionic-numberpicker']){

}
````

4) Use the below format in your template's corresponding controller

````javascript
$scope.numberPickerObject = {
    inputValue: 0, //Optional
    minValue: -9007199254740991,
    maxValue: 9007199254740991,
    precision: 3,  //Optional
    decimalStep: 0.25,  //Optional
    format: "DECIMAL",  //Optional - "WHOLE" or "DECIMAL"
    unit: "",  //Optional - "m", "kg", "℃" or whatever you want
    useNgTouch: false,  //Optional - set true in conjunction with using ngTouch (see below)
    titleLabel: 'Number Picker',  //Optional
    setLabel: 'Set',  //Optional
    closeLabel: 'Close',  //Optional
    setButtonType: 'button-positive',  //Optional
    closeButtonType: 'button-stable',  //Optional
    callback: function (val) {    //Mandatory
    timePickerCallback(val);
  }
};
````

5) Add directive to your html template similar to:

````html
<div class="item item-input">
    <span class="input-label">Weight</span>
    <ionic-numberpicker input-obj="numberPickerObject">
      <button class="button button-positive order-button">
        <i class="ion-archive"></i>
      </button>
    </ionic-numberpicker>&nbsp;
    <b>{{ weight }} {{ weightType }}</b>
</div>
````

6) (optional) Install 'ngTouch' by https://github.com/nglar/ngTouch to get (pseudo-)autorepeat increment/decrement feature on touch panels. Also, remember to set useNgTouch to true.

##Versions:

### 2) v1.1
- Fixed issue with floating point math
- Added support for negative numbers

### 1) v1.0
- Number picker functionality has been implemented

##License:
[MIT](https://github.com/milkcan/ionic-numberpicker/blob/master/LICENSE.MD "MIT")

##Contact:
email : matt@milkcan.io

##Other Links:
- [GitHub](https://github.com/milkcan/ionic-numberpicker)
- Rate it or Comment : [Ionic Marketplace](http://market.ionic.io/plugins/numberpicker)
