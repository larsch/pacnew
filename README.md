# pacnew - an enhanced `pacdiff`

`pacnew` is a system maintainance script for managing `.pacnew` files on an Arch
Linux installation. It scans for `.pacnew` files installed by package upgrads
and gives options to review difference, install it, delete it, or save for later
(`.pacstock`).

It improves on
[pacdiff](https://wiki.archlinux.org/title/Pacman/Pacnew_and_Pacsave#Third-party_utilities)
by adding commands to edit, diff without comments and save previous package
configuration for future review (.pacstock).

## Usage

```sh
% pacnew
```

## Example

```
root@host ~ # pacnew

/etc/mkinitcpio.conf.pacnew: install, move, remove, edit, skip, quit, diff, changes, help?
```

Pressing `h` for help:

<pre>
<ins>Status</ins>:
     current: /etc/mkinitcpio.conf
      pacnew: /etc/mkinitcpio.conf.pacnew
    pacstock: /etc/mkinitcpio.conf.packstock

<ins>Review</ins>:
     <ins>d</ins>iff: show difference from current to .pacnew (<ins>D</ins> to hide comments)
  <ins>c</ins>hanges: show changes from .pacstock to .pacnew (<ins>C</ins> to hide comments)

Actions:
  <ins>i</ins>nstall: replace current configuration with .pacnew (current moved to .pacsave)
     <ins>m</ins>ove: move .pacnew to .pacstock (save it)
   <ins>r</ins>emove: delete .pacnew permanently
     <ins>s</ins>kip: skip for now
     <ins>q</ins>uit: abort
</pre>

## Keyboard commands

  * <kbd>?</kbd>/<kbd>h</kbd> - show help
  * <kbd>d</kbd> - show diff between current and .pacnew
  * <kbd>D</kbd> - show diff between current and .pacnew, but hide comments
  * <kbd>c</kbd> - show changes between .pacstock and .pacnew
  * <kbd>C</kbd> - show changes between .pacstock and .pacnew, but hide comments
  * <kbd>e</kbd> - edit current configuration
  * <kbd>i</kbd> - install .pacnew as the current configuration (existing will be moved to .pacsave)
  * <kbd>m</kbd> - move .pacnew to .pacstock, saving it for future review
  * <kbd>r</kbd> - remove .pacnew (delete it)
  * <kbd>s</kbd> - skip without any change
  * <kbd>q</kbd> - quit


