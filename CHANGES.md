v1.1.0 2014-04-27 La Forclaz (VS)
---------------------------------

- Fix `S.switch` rank's initialisation.
- Add `E.l{1,2,3,4,5,6}`, lifting combinators on events.
- Add `E.Option.{some,value}`.
- Add `S.{Float,Int}.{zero,one,minus_one}`. 
- Add `S.Bool.{zero,one}`.
- Add `S.Option.{none,some,value}`.
- Add `{S,E}.on` equivalent to `{S,E}.when_`.
- Deprecate `{S,E}.when_` (syntax error prone). 

v1.0.1 2014-04-21 La Forclaz (VS)
---------------------------------

- Fix `S.bind`. 
- Use package builder topkg for distribution.

v1.0.0 2014-04-02 La Forclaz (VS)
---------------------------------

- OPAM friendly workflow and drop OASIS support.
- Add `S.bind`.

The following changes are incompatible.

- Add support for update steps, see the `React.Step` module. Allows to
  specify simultaneous primitive signal updates and event occurences.
  The functions returned by `{S,E}.create` now have an optional
  `?step` argument; if unused the previous semantics is preserved.
- Add support for strong stops, can be used on platforms where weak
  arrays are not to prevent leaks. The function `{E,S}.stop` now have
  an optional `?strong` argument; if unused the previous semantics is
  preserved.
- Change signature of `S.switch`. Any existing call `S.switch ~eq s es` can 
  be replaced by `S.(switch ~eq (hold ~eq:( == ) s es))`.


v0.9.4 2012-08-05 Lausanne
--------------------------

- OASIS 0.3.0 support.


v0.9.3 2012-03-17 La Forclaz (VS)
---------------------------------

- OASIS support.


v0.9.2 2010-04-25 Lausanne
--------------------------

- Fix a bug in weak heap implementation (thanks to Jake Donham for reporting
  and a discussion about the fix).


v0.9.1 2010-04-15 Paris
-----------------------

- Added `E.retain` and `S.retain`.
- A few `List.map` where replaced by `List.rev_map`. 
- Fixes to `breakout.ml` to make it work on vte based terminals.


v0.9.0 2009-01-19 Lausanne
--------------------------

- First release.
