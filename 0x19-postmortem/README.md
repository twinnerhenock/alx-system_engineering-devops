# Postmortem/Incident-Report/

## "This site may harm your computer"

If you did a Google search between 6:30 a.m. PST and 7:25 a.m. PST this morning, you likely saw that the message "This site may harm your computer" accompanied each and every search result. This was clearly an error, and we are very sorry for the inconvenience caused to our users.

What happened? Very simply, human error. Google flags search results with the message "This site may harm your computer" if the site is known to install malicious software in the background or otherwise surreptitiously. We do this to protect our users against visiting sites that could harm their computers. We maintain a list of such sites through both manual and automated methods. We work with a non-profit called StopBadware.org to come up with criteria for maintaining this list, and to provide simple processes for webmasters to remove their site from the list.

We periodically update that list and released one such update to the site this morning. Unfortunately (and here's the human error), the URL of '/' was mistakenly checked in as a value to the file and '/' expands to all URLs. Fortunately, our on-call site reliability team found the problem quickly and reverted the file. Since we push these updates in a staggered and rolling fashion, the errors began appearing between 6:27 a.m. and 6:40 a.m. and began disappearing between 7:10 and 7:25 a.m., so the duration of the problem for any particular user was approximately 40 minutes.

Thanks to our team for their quick work in finding this. And again, our apologies to any of you who were inconvenienced this morning, and to site owners whose pages were incorrectly labelled. We will carefully investigate this incident and put more robust file checks in place to prevent it from happening again.

Thanks for your understanding.

But of course, it will never occur again, because we never make errors and GOD is with us:).
