---
Title: Solarized Colors for Haskell
Desription: Precision colors for machines and people, Haskell-format
Author: Ethan Schoonover, Tobias Florek
Created: 2012 Mar 11
Modified: 2012 Mar 11

---

Solarized Colors for Haskell
============================

Solarized is a nice-looking colorscheme. See the [Solarized homepage] for
details. This file simply assigns each color to a haskell variable of the form
solarizedColor, where Color is the first-letter-uppercased colorname.

How does it look like
---------------------

![solarized xmonad](https://github.com/ibotty/solarized-xmonad/raw/master/solarized-base01-red.png)

Most colors you see are from vim though.

How to configure XMonad to use them
-----------------------------------

A minimal `~/.xmonad/xmonad.hs` file might look like that.

```haskell
import XMonad
import Solarized

main = do
  xmonad defaultconfig {
      normalBorderColor = solarizedBase01
    , focusedBorderColor = solarizedRed
  }
```

To let XMonad find the Solarized module, just copy/link Solarized.hs to
`~/.xmonad/lib/`, i.e.:
      $ [ -d ~/.xmonad/lib ] || mkdir  ~/.xmonad/lib
      $ ln -s /path/to/solarized-xmonad/Solarized.hs ~/.xmonad/lib/Solarized.hs

