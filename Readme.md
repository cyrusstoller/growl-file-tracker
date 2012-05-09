## Guard File Tracker

This uses `guard` and `growl` to keep track of any changes that are made in a given directory.

```
$ bundle exec guard # only additions
$ bundle exec guard # additions, moves, and deletions
```

I had trouble installing `growlnotify`

This is what I ended up using with `homebrew`

```
brew install https://raw.github.com/mxcl/homebrew/bd40f1e5f89fad962b021c827d56a9fdea0c847d/Library/Formula/growlnotify.rb
```