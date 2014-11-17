# metawidget-js

Metawidget is a pluggable Javascript Form Generator. It comes with plug-ins for many input formats...

 * JSON objects
 * JSON Schema
 * REST calls; etc
 
...and output targets...

 * Angular
 * Bootstrap
 * JQuery UI
 * JQuery Mobile
 * Node; etc
 
...or you can easily add your own.

## Quick Start

Using plain JavaScript, easily throw a JSON object at Metawidget:

    var person = {
        firstname: 'Homer',
        surname: 'Simpson',
        age: 36
    };

    var mw = new metawidget.Metawidget( document.getElementById( 'metawidget' ));
    mw.toInspect = person;
    mw.buildWidgets();

Or make it even easier with frameworks such as Angular:

    <metawidget ng-model="person"></metawidget>

Or JQuery Mobile:

    $( '#metawidget' ).metawidget().metawidget( 'buildWidgets', person );
    
Metawidget will generate all HTML boilerplate for your form, tailored to your preferred layout. Such as Bootstrap:

    <div class="form-group">
        <div class="col-sm-3 control-label">
            <label id="firstname-label" for="firstname">Firstname:</label>
        </div>
        <div class="col-sm-9">
            <input id="firstname" class="form-control" type="text">
        </div>
    </div>
    
Think how much error-prone typing this saves you! There's plug-in support for data binding, validation,
third-party widget libraries, and much more! 

## Examples

This repo is a collection of JavaScript UI generation examples. The main project is in the
[Metawidget repo](https://github.com/metawidget/metawidget). Please file issues and pull requests against that repo.

## Documentation

Documentation is available on the [Metawidget site](http://metawidget.org/).

## License

These examples are licensed under the BSD 2-Clause License (also know as the "Simplified BSD License"
or "FreeBSD License"). This is a permissive license. It allows redistribution and use in source and
binary forms, with or without modification. You can freely copy code from the examples, modify it and
redistribute it.

Metawidget itself is dual licensed under both the LGPL/EPL and a commercial license. See our
[licensing FAQ](http://metawidget.org/doc/faq/licensing.php).
