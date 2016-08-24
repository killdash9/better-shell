better-shell
=================

This package simplifies shell management by providing the following
commands.

`better-shell-shell`
--------------------

Cycle through existing shell buffers, in order of recent use.  If
there are no shells, one is created.

With prefix arg, bring up a shell on the same host and in the same
directory as the current buffer, choosing an existing shell if
possible.  The shell chosen is guaranteed to be idle (not currently
running a command).  It first looks for an idle shell that is already
in the buffer's directory.  If none is found, it looks for another
idle shell on the same host as the buffer.  If one is found, that
shell will be chosen and automatically placed into the buffer's
directory with a \"cd\" command.  Otherwise, a new shell is created on
the same host and in the same directory as the buffer.

`better-shell-remote-open`
--------------------------

Open a shell on a remote server, allowing you to choose from any host
you've previously logged into (uses your ~/.ssh/known_hosts file) or
enter a new host.

Installation
------------

I'm hoping to get this into melpa when I have time.  Here are my key bindings:

    (global-set-key (kbd "C-'") 'better-shell-shell)
    (global-set-key (kbd "C-;") 'better-shell-remote-open)

<!--

[![MELPA](https://melpa.org/packages/better-shell-badge.svg)](https://melpa.org/#/better-shell)

## Melpa Installation ##

    M-x package-install RET better-shell RET

Then add key bindings to your config, for example:

    (global-set-key (kbd "C-'") 'better-shell-shell)
    (global-set-key (kbd "C-;") 'better-shell-remote-open)

## `use-package` Installation ##

    (use-package better-shell
      :ensure t
      :bind (("C-'" . better-shell-shell)
             ("C-;" . better-shell-remote-open)))

-->