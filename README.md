# bower-angular-translate-loader-partial

angular-translate-loader-partial bower package

### Installation

````
$ bower install angular-translate-loader-partial
````

### Differnt from previous version

urlTemplate now uses angular $interpolate, so you can use filters on part and lang variables. There are built-in filters; language and country, which parse a locale code(e.g. EN, en, en_US, en_us, en_US.UTF8). But, you have to use {{ }} rather than { }.
````
function($translateProvider, $translatePartialLoaderProvider) {
    $translateProvider.useLocalStorage();
    $translatePartialLoaderProvider.addPart('bigdad');
    $translateProvider.useLoader('$translatePartialLoader', {
        urlTemplate: '/lang/{{part | lowercase}}_{{lang | language | lowercase}}.json'
    });
    $translateProvider.determinePreferredLanguage();
}]);
````
