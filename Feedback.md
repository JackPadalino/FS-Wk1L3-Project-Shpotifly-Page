### HOMEWORK 1 (Shpotifly Page)
Amazing work overall - this site looks super clean and well done. I love the direction you took it all in

HTML:
 Right now you have some very broad class names in your HTML, I’d recommend naming them based on what they represent instead of where they’re positioned in the HTML to keep things more readable
i.e. For the top section of your main area you have classes like “mainArea1Div” and “mainArea1Image” - it’d make more sense to name these after what they semantically represent (so “mainArea1Div” = “Playlist Container” and “mainArea1Image” = “PlaylistImage”). Doing this will make your CSS much easier to reason about without having to reference your HTML and will also help you share styles between different pages more fluidly (i.e. if you wanted to represent playlists on the users page as well, now you have a class name that can be used anywhere while still making sense)
In you’re HTML you’re sizing a lot of your texts based on using different header types - while this is extremely common to see it’s also a big anti-pattern and makes it difficult for things like web scrapers and screen readers to parse your site (so it’s worse for SEO since google can’t get a quick idea of what sections your site is cut into and it’s worse for accessibility). The rules of thumb are generally:
There should be one and only one h1 on the page at any time with content that sums up what the purpose of the page is
 Headers beyond that should represent unique sections of your site
 Paragraph tags represent longer bodies of text
(So for the most part you’re fine, all this means is that every h1 that isn’t your logo should probably be an h2. You can still size the h2 to be bigger than usual if you’d like)
I love how you’re using comments to separate notable sections of your page using comments - that goes a long way in making things look clean and organized

CSS
Your CSS for the most part looks great - the only big note I have is again, make sure you’re using classNames to represent why the styles exist and not where they are in the HTML. The other minor note is be careful of using combination operators such as > - they’re useful but they also have a tendency to cause side-effects in a way that’ll make debugging a pain to do. Once we reach react we’ll discover a much more comfortable way of handling styles that’ll abstract away a lot of those issues so look forward to that
If you want to make your page more responsive I’d focus on playing with the flex-wrap property a bit. The reason your page is scrollable right now is mostly because of the default margin that the browser gives the <body> tag - if you set that margin to 0 you should be in a more comfortable spot.
