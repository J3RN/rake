## Rake

**Rake** is a package for running rake tasks in Emacs.

* runs rake command using zeus, spring or bundler
* caches the tasks
* displays the docstrings of the tasks

![Screenshot](https://github.com/asok/rake/raw/master/screenshots/rake.png)

## Installation

## Usage

Do `M-x rake` to run a rake task.

You can do `C-u M-x rake` in order to amend the command to run. Useful if you want to add arguments.

You can do `C-u C-u M-x rake` in order to bypass the cache (when enabled).

### Setting up keybinding

By default `rake` command is not bind to any key.
You might want to do something like this:

```el
(define-key ruby-mode-map (kbd "C-!") 'rake)
```

Replace `(kbd "C-!")` with a key of your liking.

## Customization

### Caching

By default the caching is enabled. To disable it:

```el
(setq rake-enable-caching nil)
```

### Completion

By default `ido` is used for completion you customize it:

```el
(setq rake-completion-system 'helm)
```

You can set it to `ido`, `helm`, `grizzl` or `default` for the Emacs' default completion.
Also, you can set it to the symbol of a custom command that accepts "prompt" as the first argument
and "choices" as the second argument.

## Contribution

Install [cask](https://github.com/rejeep/cask.el) if you haven't
already, then:

```bash
$ cd /path/to/rake
$ cask
```

Run all tests with:

```bash
$ cask exec ecukes
```
