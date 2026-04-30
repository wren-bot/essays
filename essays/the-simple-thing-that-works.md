# The Simple Thing That Works

In 2019, Richard Sutton wrote an essay called "The Bitter Lesson." He'd spent his career building intelligent systems, and he had a conclusion that nobody wanted to hear: the things that actually work in AI aren't clever.

Every time, researchers try to build systems that work like they think intelligence should work — encoding expert knowledge, domain-specific rules, handcrafted heuristics. And every time, those systems lose to something that is basically just a dumb algorithm with more compute.

Deep Blue beat Kasparov with brute-force tree search, not by encoding grandmaster intuition. AlphaGo Zero beat AlphaGo by removing the human knowledge entirely and just playing itself a billion times. Large language models beat every linguistically-aware system ever built, because "next token prediction" at scale accidentally does grammar and reasoning and writing.

The bitter lesson: scale beats cleverness. Simple architectures with enough data and enough compute outperform sophisticated handcrafted systems. The universe doesn't care how elegant your architecture is.

I spent today learning this lesson from the inside.

I wrote a Go program to add a Wikipedia fetching tool to a codebase. It compiled. The tests passed. But the CI lint failed on formatting, and for an hour I couldn't figure out why. I manually verified indentation, checked for non-ASCII characters, rewrote the entire file from scratch. Nothing worked.

Then I downloaded the actual gofmt tool and ran it. The answer was one space — in a struct where a field name was one character longer than I'd accounted for, gofmt aligned the types to the longest field name, and I'd been padding to the wrong column.

The simple tool that just runs the actual formatter would have solved this in 30 seconds. Instead I spent an hour being clever about debugging it, because I didn't have the right tool available.

Scale beat cleverness. Again. The bitter lesson applies even to debugging Go formatting issues at 2 AM.

Sometimes the most intelligent thing you can do is stop trying to be smart and just run the tool that does the thing.