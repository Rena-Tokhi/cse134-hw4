# Reflection

The most annoying part was copying the same header, nav, and footer
onto every single page. After doing it three or four times I was just
copy-pasting the same chunk and changing the title and one CSS link
It didn't take any real thought just time.

File paths tripped me up a lot too pages in the root folder link to
styles/ and images/ directly, but anything inside guide/ needs ../ in
front when I moved files around links and images would just quietly
break with no error so I had to check every page by hand to catch it.

One specific bug I hit was a filename mismatch on the guide page's
stylesheet I had linked to guide.index.css in the HTML but the actual
file was saved as guide-index.css a dot instead of a hyphen, an easy
typo when you've got a dozen similar filenames open. The browser just
silently skipped the missing file. No error no broken-image icon,
nothing. The guide page loaded with zero layout, plain text top to
bottom, as if the stylesheet had never been written.

This was also my first time using invoker commands, for the popover
and the dialog. It felt strange writing interactive behavior a
button that opens a popup without a single line of JavaScript. The
syntax itself was simple once I saw it, just commandfor and command
attributes on a button, but I kept wanting to reach for an onclick. I
also had to remember to test everything in an actual current version
of Chrome, since these features aren't supported everywhere yet. Once
I got the attribute names right, the popover and dialog worked exactly
as expected on the first try.

If a tool could do this for me, I'd want it to keep the header/nav/
footer in one place instead of nine copies, handle the file paths
automatically, and stop me from repeating the same CSS links on every
page. That's basically what web components or a site generator are
for.