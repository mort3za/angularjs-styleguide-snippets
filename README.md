# angularjs-styleguide-snippets package

A set of AngularJS snippets based on John Papa's style guide. Forked from angularjs-styleguide-snippets by Jason Miazga, Plus some updates and fixes. + ngComponent

'inject dependencies' removed from snippets because you can use @ ngInject and it's a life saver. Try it (`gulp-ng-annotate` or `grunt-ng-annotate`)  

### Snippets

You can use the following snippets in JavaScript.
New: `ngcomponent`!

##### ngmodule
```
(function() {
    'use strict';

    angular
        .module('${1:app}', [
            '${2:dependencies}'
        ]);
})();
```

##### ngcomponent
```
(function() {
    'use strict';

    /* @ngInject */
    var ${1:Component} = {
            templateUrl: '${2:templateUrl}',
            controllerAs: 'vm',
            controller: Controller
    }

      /* @ngInject */
      function Controller(){
            var vm = this;

      }

      angular
            .module('app')
            .component('${1:Component}', ${1:Component});
})();
```


##### ngcontroller
```
(function() {
    'use strict';

    /* @ngInject */
    function ${2:Controller}() {
        var vm = this;
        activate();

        function activate() {

        }
    }

    angular
        .module('${1:app}')
        .service('${2:Controller}', ${2:Controller});
})();
```

##### ngfactory
```
(function() {
    'use strict';

    /* @ngInject */
    function ${2:factory}() {
        var factory = {
            ${4:function}: ${4:function}
        };
        return factory;

        function ${4:function}() {

        }
    }

    angular
        .module('${1:app}')
        .factory('${2:factory}', ${2:factory});
})();
```

##### ngdirective
```
(function() {
    'use strict';

    /* @ngInject */
    function ${2:directive}() {
        var directive = {
            restrict: '${3:EA}',
            templateUrl: '${4:templateUrl}',
            scope: {
            },
            link: linkFunc,
            controller: ${5:Controller},
            controllerAs: 'vm',
            bindToController: true
        };

        return directive;

        function linkFunc(scope, el, attr, ctrl) {

        }
    }

    /* @ngInject */
    function ${5:Controller}() {
        var vm = this;
        activate();

        function activate() {

        }
    }

    angular
        .module('${1:app}')
        .directive('${2:directive}', ${2:directive});
})();
```

##### ngservice
```
(function() {
    'use strict';

    /* @ngInject */
    function ${2:Service}() {
        return {
            ${4:function}: ${4:function}
        };

        function ${4:function}() {

        }
    }

    angular
        .module('${1:app}')
        .service('${2:Service}', ${2:Service});
})();
```

##### ngfilter
```
(function() {
    'use strict';

    function ${2:filter}() {
        return ${2:filter}Filter

        function ${2:filter}Filter(${3:params}) {
            return ${3:params};
        }
    }

    angular
        .module('${1:app}')
        .filter('${2:filter}', ${2:filter});
  })();
```
