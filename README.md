# migrate-up and migrate-down commands
Uses FZF to retrieve a list of your Rails migrations, sorts them by their filename (so that most recent is at the bottom), and allows you to easily migrate that file up or down using `bin/rails db:migrate:up VERSION=...` or `bin/rails db:migrate:down VERSION=...` using the chosen file's schema version.

## Prerequisite
- You must have [`fzf`](https://github.com/junegunn/fzf) installed.
- You need to be in your Rails app's directory
- `bin/rails` must exist in your Rails app directory

## Install
Copy the `migrate-up` and `migrate-down` scripts to a folder that is in your PATH. I use `~/bin/` and make sure I have the following in my `~/.zshrc` or `~/.bashrc` file:

```shell
export PATH=$HOME/bin:$PATH
```

Then, from your Rails app directory, simply run either `migrate-up` or `migrate-down` and select a file from the list using the arrow keys, or start typing to use FZF's fuzzy-finder search.
