# Interesting Bugs and Patches

This file lists particularly interesting bugs or patches I've
encountered.

These issues are in no way a criticism of the code quality of these
projects, I just found them particularly intruiguing.

## That Should Never Happen

I once got a [segfault in a Rust program that did not use `unsafe`
anywhere](https://github.com/rust-lang/rust/issues/30081).

I once deleted [a single closing paren in
Emacs](https://github.com/emacs-mirror/emacs/commit/56da7add7845f0685dd6d5a1f7ae0a76cb2953da).

## Security

I found a way of getting [arbitrary code execution in Emacs just by
using tab
completion](https://yhetil.org/emacs/CAFXAjY5f4YfHAtZur1RAqH34UbYU56_t6t2Er0YEh1Sb7-W=hg@mail.gmail.com/). This
later became part of CVE-2024-53920 (see [writeup by Eshel
Yaron](https://eshelyaron.com/posts/2024-11-27-emacs-aritrary-code-execution-and-how-to-avoid-it.html)
who found much more serious variants).

## Crashing Mature Projects

I found a way of [segfaulting git
diff](https://lore.kernel.org/git/CAFXAjY7XcL1APhLRXU8TO96z=f7957f2ieK56dHVsXUay55vpg@mail.gmail.com/)
(fixed in [this git
commit](https://github.com/git/git/commit/85a9a63c9268b18b24f25f6a14d6ae9966c3566d)).

My [suggest.el
project](https://debbugs.gnu.org/cgi/bugreport.cgi?bug=25684)
uncovered [a way of segfaulting
Emacs](https://debbugs.gnu.org/cgi/bugreport.cgi?bug=25684).
