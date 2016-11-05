# `git svn` extension for Magit

This package provides basic support for `git svn`, a Git command
that aims to provide bidirectional operation between a Subversion
repository and Git.  See its manual page `git-svn(1)` for more
information.

When `magit-svn-mode` is turned on then the unpushed and unpulled
commit relative to the Subversion repository are displayed in the
status buffer, and `N` is bound to a popup with commands that wrap
the `git svn` subcommands `fetch`, `rebase`, `dcommit`, `branch`
and `tag`, as well as a few extras.

To enable the mode in a particular repository use:

    cd /path/to/repository
    git config --add magit.extension svn

To enable the mode for all repositories use:

    git config --global --add magit.extension svn

To enable the mode globally without dropping to a shell:

    (add-hook 'magit-mode-hook 'magit-svn-mode)

If you are looking for native SVN support in Emacs, then have a
look at `psvn.el` and info node `(emacs)Version Control`.
