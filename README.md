# Sublime Text 2 Rails snippets

I don't know who the original author is, but this repo is an improved version of https://github.com/bradrobertson/sublime-packages/tree/master/Rails

# Changes in this "fork"

* Use ruby 1.9 hash syntax (`foo: :bar`, not ` :foo => :bar`)
* Prefer `=` over `-` for haml snippets (Rails 3 way)
* Prefer `respond to format.html` over `respond to wants.html`
* All rjs snippets removed
* `class<tab>` autocompletes a ruby class
* `arc<tab>` autocompletes an ActiveRecord model class
* `con<tab>` autocompletes a controller class
* `crud<tab>` autocompleted controller actions