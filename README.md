## Notes

## Setup the Buffer Project

Treat your main project as another remote.

  Start main project: clone remote -> local

  Start buffer: clone local -> buffer

## Pulling in Changes

git pull (same as ever)

## Dispensing Changes to Main

~/c/d/repo-buffer (master|✔) $ git log --graph --oneline master..develop
*   4f4ce2e (develop) Merge branches 'feature-b' and 'feature-c' into develop
|\
| * 8272017 Rubidium
| * 632b5da Radon
| * 9a6c9e6 Osmium
| * 6eeb996 Lutetium
| * bedd555 Sulfur
| * d93b502 Indium
| * bd6eaf1 Francium
| * d8132a7 Hassium
| * e69cec1 Dubnium
| * 4cc774a Krypton
* | 7dae8b9 red
* | 7ac2438 blue
* | db5d2b7 green
* | 6ce46f9 yellow
* | dc2b193 blue
* | dddf286 violet
* | ca4c2e7 orange
* | c0680e4 yellow
* | ce4fb05 indigo
* | a5512cb yellow
|/
* 94e9224 Change six tricky Livermorium
* 588ad97 Add five helpful Neptunium
* c62dbca Remove three violet plumeria
* 349da5d Remove eight green anemone
* 23a9c35 Add two nasty freesia
* 0c8ec64 Add two helpful Lanthanum
* 6dc42c3 Change five blue Gallium
* b73d7fc Change nine indigo Platinum
* 8986a30 Add six helpful Neon
* 0e84ebd Add nine green Argon
* f7691c4 Add readme and notes

commit 4f4ce2e7fc163bd684cfd2975431ce1c11c26e80 (HEAD -> develop)
Merge: 7dae8b9 8272017
Author: Jeremy Greer <jex.grizzle@gmail.com>
Date:   Tue Jan 21 10:24:45 2020 -0800

    Merge branches 'feature-b' and 'feature-c' into develop

diff --cc glitter
index 0db6c60,39b131f..9862239

I want to dispense these a bit at a time.
* 94e9224
* 7dae8b9 red
* 8272017 Rubidium


I can mark the history with branches afterward (one, two, three).

~/c/d/repo-buffer (three|✚1) $ git log --graph --oneline master..develop
*   4f4ce2e (develop) Merge branches 'feature-b' and 'feature-c' into develop
|\
| * 8272017 (HEAD -> three) Rubidium
| * 632b5da Radon
| * 9a6c9e6 Osmium
| * 6eeb996 Lutetium
| * bedd555 Sulfur
| * d93b502 Indium
| * bd6eaf1 Francium
| * d8132a7 Hassium
| * e69cec1 Dubnium
| * 4cc774a Krypton
* | 7dae8b9 (two) red
* | 7ac2438 blue
* | db5d2b7 green
* | 6ce46f9 yellow
* | dc2b193 blue
* | dddf286 violet
* | ca4c2e7 orange
* | c0680e4 yellow
* | ce4fb05 indigo
* | a5512cb yellow
|/
* 94e9224 (one) Change six tricky Livermorium
* 588ad97 Add five helpful Neptunium
* c62dbca Remove three violet plumeria
* 349da5d Remove eight green anemone
* 23a9c35 Add two nasty freesia
* 0c8ec64 Add two helpful Lanthanum
* 6dc42c3 Change five blue Gallium
* b73d7fc Change nine indigo Platinum
* 8986a30 Add six helpful Neon
* 0e84ebd Add nine green Argon
* f7691c4 Add readme and notes

Once I'm ready to push to origin (dispense a change), I want to rebase it so my
private history is gone.

Get back to the point I want to share.
  git checkout one

Rebase to destination, rewriting my private history.
  This will mess up any merges we've done with this already.
