# Creating a beautiful Markdown web site

If you're like me, you don't want to spend money unnecessarily, and you
definitely don't want to spend many many hours designing a lovely web site.
Maybe you have the artistic eye to pick something out, and maybe you don't,
but either way, it's a bad use of your time to fiddle around in HTML all day.

Enter [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
and [GitHub Pages](https://pages.github.com/). I host all my software on GitHub
already, and they offer free hosting of static web sites via GitHub.io. Are you
a budding software developer? You probably already host your code on GitHub.
Not into software? Using git can still help you enormously with things that are
not exactly code, such as simple scripts and config files. But an explanation
of why git is amazing is outside the scope of this document.

If you don't have a GitHub account, start by [signing up](https://github.com/join).
Then follow the [instructions for setting up GitHub Pages](https://pages.github.com)
and create your basic repository.

The first step to making your web site pretty is to have some content. This is
the part that there's no short-cut for. Open up a text editor and create a file
to be one page of your web site, and... start typing stuff :) If the file is
called "Foobar.md", it will be available at https://YOURNAME.github.io/Foobar
on your final web site. Be sure to create one called "index.md" to be the first
page that people see. Commit and push as per the GitHub tutorial.

Once you have your main content, you can update it the same way - edit the file,
commit, push. Creating new pages is just as easy. Be wary of renaming or deleting
pages, though, in case someone has linked to your page (you'll break that link if
you do). Follow the Markdown style and you should be able to create a nice
structured web page, easy for screen readers to understand as well as visually
clean.

So, you have your content, but it's ugly? That's actually really easy to fix!
GitHub offers a number of simple
[themes](https://help.github.com/en/articles/adding-a-jekyll-theme-to-your-github-pages-site-with-the-jekyll-theme-chooser)
to choose from, and if you're happy with one of those, job done! But maybe, like
me, you're a bit pickier than that. Fortunately the themes can be tweaked, so
check out the instructions associated with your chosen theme. For this site, I
adjusted the way links look, with not even a dozen lines of code. Got a friend
who knows HTML and CSS? Small tweaks like this will be easy and quick.

What if you already have a nicely-done web site, and you want to migrate it?
That can be done too, but it'll mean a bit of one-off work, and you'll need to
know HTML to do it (or find someone who does). In short, what you would do is
create a single HTML file and say "here, put the Markdown content RIGHT THERE"
and GitHub Pages will do exactly that.

Once you have a nice-looking Markdown site, it becomes a breeze to edit. You
don't need any HTML knowledge, you don't have to worry about breaking the whole
layout, you don't need to stress about whether it looks good. Just edit the
simple text files. It's even possible - easy, in fact - to let other people
contribute, perhaps copyediting, or perhaps adding significant content.

Don't pay some company every month for a job that you can do easier *and better*
on your own!
