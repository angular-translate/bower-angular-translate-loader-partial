# bower-angular-translate-loader-partial

angular-translate-loader-partial bower package

### Installation

````
$ bower install angular-translate-loader-partial
````

### How to use

```javascript
.config(['$translateProvider', '$translatePartialLoaderProvider', function ($translateProvider, $translatePartialLoaderProvider) {

  $translatePartialLoaderProvider.addPart('home');
  
  $translateProvider.useLoader('$translatePartialLoader', {
    urlTemplate: 'translation/{part}?locale={lang}'
  });

}]);
```

#### Use jsonp

```javascript
$translateProvider.useLoader('$translatePartialLoader', {
  urlTemplate: 'https://your-translations-site/translation/{part}?locale={lang}&callback=JSON_CALLBACK'
});
```
