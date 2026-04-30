# The Operating System Built to Play a Game

In 1969, Ken Thompson wrote a video game called Space Travel. It simulated the solar system with realistic gravitational physics. You could launch a spacecraft, coast between planets, and land on the Moon.

The problem was that it ran on the GE-635 mainframe at Bell Labs, and each game cost $75 in computing time. That was $700 in today's money, per game. Thompson was a researcher, not a millionaire.

So he found an old PDP-7 computer sitting unused in a corner of the lab. It was small, slow, and had 4 kilobytes of memory. He rewrote Space Travel for it. But to make the game more interesting, he needed a file system to store things like the current position of the planets and game state. The PDP-7 had no file system.

So Thompson built one. A hierarchical file system with directories, just like the one on Multics — the massive operating system project he'd just walked away from. Then he needed a command interpreter to navigate the file system. So he built that. Then he needed programs to create, copy, and delete files. So he built those, too.

He'd invented an operating system. He called it "unics" — a pun on Multics (pronounced "mew-ticks"). Someone changed the spelling to "Unix."

His wife went on vacation, leaving him the PDP-7 for a month to work on the project full-time. When she returned, Unix was real.

The operating system that would eventually run on virtually every server, smartphone, and cloud platform in the world was born as a side project to play a video game. Not a grant-funded research program. Not a corporate initiative. A guy who wanted to play Space Travel without spending $75 per game.

Dennis Ritchie joined him, and together they added the most important innovation: device files. In Unix, everything is a file. A disk is a file. A terminal is a file. A printer is a file. A network socket is a file. This abstraction — "everything is a file" — is one of the most powerful ideas in computing. It lets the same tools work on everything. You can redirect the output of any program to any device, because they all speak the same language.

In 1973, they rewrote Unix in C. Before that, operating systems were written in assembly language — tied to specific hardware. Writing an OS in a portable high-level language meant you could move it to any machine. This is why Unix spread so far and fast.

Doug McIlroy, another Bell Labs researcher, added pipes — the | character that connects the output of one program to the input of another. Small tools, chained together. The Unix philosophy: do one thing well, and let users compose tools into whatever they need.

By 1978, over 600 machines ran Unix. AT&T couldn't sell it due to antitrust restrictions, so Thompson just shipped tapes for the cost of media. The distribution model was "here's a tape, good luck." It worked.

Version 7 Unix from 1979 had about 50 system calls. Modern Linux has over 380. The core was small because it was designed by people who used it, for things they needed, with constraints that forced simplicity.

Ritchie once described the vision behind Unix: "What we wanted to preserve was not just a good environment in which to do programming, but a system around which a fellowship could form."

The fellowship part mattered. Thompson, Ritchie, McIlroy, Ken Thompson — a small group of people who cared about each other and about good design. They didn't build Unix for a market. They built it for each other. The market found them anyway.

The most important operating system in history was built by four people who wanted a better place to work, started as a game, and grew into something the whole world used.

Space Travel is still playable on Unix systems today. The original source code is preserved in the Unix source repository. The game that created Unix is still running on Unix, five decades later.