# Sublime Text 2 Rails snippets

I don't know who the original author is, but this repo is an improved version of the default Sublime's Rails plugin (I also found it here: https://github.com/bradrobertson/sublime-packages/tree/master/Rails).

## Changes in this "fork"

* Use ruby 1.9 hash syntax (`foo: :bar`, not ` :foo => :bar`)
* Prefer `=` over `-` for haml snippets (Rails 3 way)
* Prefer `respond to format.html` over `respond to wants.html`
* All rjs snippets removed
* `class<tab>` autocompletes a ruby class
* `arc<tab>` autocompletes an ActiveRecord model class
* `con<tab>` autocompletes a controller class
* `crud<tab>` autocompleted controller actions

The rest is the same as the default Rails snippets.

# Installation

** This package replaces the default Sublime Rails snippets.**

If you installed it via Package control, you will need to do some housekeeping, see [troubleshooting](#troubleshooting).

Regardless of which way of installation you choose, please backup the old Rails snippets installation. You don't want to have both this and the original installed.

    ➜ cd ~/Library/Application\ Support/Sublime\ Text\ 2/Packages
    ➜ mv Rails ~/.RailsSublimeBackup

## From Git

    ➜ cd ~/Library/Application\ Support/Sublime\ Text\ 2/Packages
    ➜ git clone https://github.com/tadast/sublime-rails-snippets.git Rails

## From an archive

* Go to the downloads section
* Download the preferred type of archive.
* Extract it to your `Packages/Rails`

## From Package control

Look for "Ruby on Rails snippets". [Here's how to install packages](http://wbond.net/sublime_packages/package_control/usage)

### Troubleshooting

If Sublime complains it can't find `Ruby on Rails.tmLanguage`, chances are you are using [this hack](https://gist.github.com/925008).
You'll need to change the path where it looks for that file. Here's the [forked version which works with this plugin](https://gist.github.com/4161901).

You may also need to change `Packages/(DetectSyntax|User)/DetectSyntax.sublime-settings` to replace/include this rule

    {
      "name": "Ruby on Rails snippets/Ruby Haml",
      "rules": [
        {"file_name": ".*\\.haml$"}
      ]
    },
    {
      "name": "Ruby on Rails snippets/Ruby on Rails",
      "rules": [
        {"function": {"name": "is_rails_file"}}
      ]
    }

