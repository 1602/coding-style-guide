## Naming

- use camelCase everywhere, except constants which are `UPPER_CASE_WITH_UNDERSCORE`
- start constructor name with upper case letter
- do not use short variable names

## Spaces

- operators should be surrounded with spaces
- anonyous function should not have space between `function` and `(`
- maned function should have not have space between function name and `(`

## Identation

We use 4 spaces for identation. No deep identation, i.e. use this way:

```javascrtipt
    do.something.awesome(function(imdone) {
        imdone();
    });
```

instead of this

```javascrtipt
    do.something.awesome(function(imdone) {
                             imdone();
                         });
```

## Callback names

Use `done`, `next`, `callback`, `cb` or `fn` as callback param name.

## Callback context binding, using `self` and `that`

Do not use bind, do not save `this` in `self` or `that` variable. Use meaningful
variable name, for example:

```javascrtipt
Listing.prototype.update = function(done) {
    var listing = this;
    listing.products.update(function() {
        listing.update(done);
    });
};
```
