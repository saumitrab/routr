Routr [![Build Status](https://travis-ci.org/ouchtown/routr.svg?branch=master)](https://travis-ci.org/ouchtown/routr) [![Dependency Status](https://david-dm.org/ouchtown/routr.svg)](https://david-dm.org/ouchtown/routr)
=========

Routr library is an implementation of router-related functionalities that can be used for both server and client.

Usage
-----
For more detailed examples, please check out [example applications](https://github.com/ouchtown/routr/tree/master/examples);

```
var Router = require('routr'),
    router,
    route;

var router = new Router({
    view_user: {
        path: '/user/:id',
        method: 'get',
        foo: {
            bar: 'baz'
        }
    }
});

route = router.getRoute('/user/garfield');
if (route) {
    // this will output:
    //   - "view_user" for route.name
    //   - {id: "garfield"} for route.params
    //   - {path: "/user/:id", method: "get", foo: { bar: "baz"}} for route.config
    console.log('[Route found]: name=', route.name, 'params=', route.params, 'config=', route.config);
}

```


License
-------
This software is free to use under the Yahoo! Inc. BSD license.
See the [LICENSE file][] for license text and copyright information.

[LICENSE file]: https://github.com/ouchtown/routr/blob/master/LICENSE.md

Third-pary open source code used are listed in our [package.json file]( https://github.com/ouchtown/routr/blob/master/package.json).

