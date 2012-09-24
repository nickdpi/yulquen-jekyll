# Yulquen
### An HTML and CSS framework for prototyping interactions

Yulquen is a hack of [Skeleton](http://www.getskeleton.com), a responsive CSS framework, to fit some common ways that interaction designers and other sundry UX folk prototype websites and applications. It provides some functionality for annotations and forms, with all of the styling CSS removable for handoff or more custom tweaks.

## Presuppositions

- You have __passing fluency in writing HTML and CSS__. Yulquen deliberately doesn't contain JavaScript, so you can use whatever library you want.
- You are okay either with __Skeleton being your production framework__, or with rewriting the HTML and CSS later. Yulquen is meant to remove the pain of rewriting the same layout and behavior in code, so the latter seems a bit disingenuous.
- You are okay with the whole thing being a __static site__, with no templating functionality included.

## How to Use

Yulquen contains three CSS files:

- __wireframe.css__: All of your CSS should go here. If you want to preserve CSS in your handoff, make another stylesheet and put your CSS there instead.
- __base.css__: All of Skeleton’s styling, typography, and CSS reset. Provides a good start.
- __skeleton.css__: The responsive hoo-hah that makes your grid and provides reflow for mobile layouts.

### Jekyll tweaks

This is a hack of Yulquen for supporting [Jekyll](http://jekyllrb.com), a static site library in Ruby. This assumes you have a modicum of working knowledge of how Jekyll works. You should probably also know how to get Ruby running on a system (especially your own!) and how to install Jekyll as a gem on it.

In this existing system, only one template exists for you to fill with various page content. You might want to hack it to reflect many different page states, such as whether a user has logged in to a web application.

Yulquen's templates have a few variables particular to it:

- __location__: Should correspond to a similar notation on your site map.
- __hidetemplate__: If set to _true_, all annotations on the main template (denoted as .template.annotation) will be suppressed. You should use this for all pages where you don't want to re-explain all of the annotations in a page's header and footer.
- __anno__: This is where your annotations go. They need to be indented with _spaces_ (not tabs!) for Jekyll to parse multiple lines correctly. Sadly, Markdown doesn't appear to support the name="" attribute, or it'd be written in that. One day.

### During handoff:

- Delete base.css and wireframe.css.
- Remove all instances of sup.annotation and div.annotations.
- Enjoy your new reality of barebones minimalism.

## In conclusion

This is ridiculously alpha, and comes with no support. You should probably know what you're doing when it comes to reading front end code. I have no idea what I am doing, so feel free to make a pull request and make this better.

Read more at [Yulquen's official site](http://nickd.org/yulquen/). [Share your uses of Yulquen](mailto:nickd@nickd.org) and I'll put together a gallery sometime.

## Future tweaks

- Better looking forms
- Right-aligned, responsive side labels
- Site map page
- Data model page

## License

Yulquen is licensed under [WTFPL version 2](http://sam.zoy.org/wtfpl/), except for Skeleton's CSS files, which are slightly modified and licensed under the [MIT license](http://opensource.org/licenses/mit-license.php), and you should probably respect that.