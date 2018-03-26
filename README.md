Chess in Elm
============

This is an experiment of porting [Chess in
Haskell](https://github.com/mtak/chess-hs). Elm and Haskell share a lot of
syntax and language features so this was fairly straight forward. The Haskell
code makes use of certain features not available in Elm, particularly
monads and list comprehensions.

There are three implementations:

* Collage uses Graphics.Collage to draw to an HTML canvas and to handle input
* Element uses Graphics.Element to draw using HTML divs and Graphics.Input to handle input
* VirtualDom uses [elm-html](https://github.com/evancz/elm-html) to using an HTML table and uses onClick events for input

You can try it out at http://eskilandreen.github.io/chess-elm/. You can build the code
by running eg `elm-make VirtualDom/Main.elm --output virtualdom.html` and
finding the resulting file in your browser, or you can try it out using code
you can either run it out by launching `elm-reactor` and navigating to
`http://localhost:8000/VirtualDom/Main.elm`.
