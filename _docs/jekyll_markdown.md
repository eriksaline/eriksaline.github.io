# Where things are
source:       .
destination:  ./_site
plugins_dir:  ./_plugins
layouts_dir:  ./_layouts
data_dir:     ./_data
includes_dir: ./_includes
collections:  null

# Handling Reading
safe:         false
include:      [".htaccess"]
exclude:      []
keep_files:   [".git", ".svn"]
encoding:     "utf-8"
markdown_ext: "markdown,mkdown,mkdn,mkd,md"

# Filtering Content
show_drafts: null
limit_posts: 0
future:      false
unpublished: false

# Plugins
whitelist: []
gems:      []

# Conversion
markdown:    kramdown
highlighter: rouge
lsi:         false
excerpt_separator: "\n\n"
incremental: false

# Serving
detach:  false
port:    4000
host:    127.0.0.1
baseurl: "" # does not include hostname

# Outputting
permalink:     date
paginate_path: /page:num
timezone:      null

quiet:    false
defaults: []

# Markdown Processors
rdiscount:
  extensions: []

redcarpet:
  extensions: []

kramdown:
  auto_ids:       true
  footnote_nr:    1
  entity_output:  as_char
  toc_levels:     1..6
  smart_quotes:   lsquo,rsquo,ldquo,rdquo
  enable_coderay: false

  coderay:
    coderay_wrap:              div
    coderay_line_numbers:      inline
    coderay_line_number_start: 1
    coderay_tab_width:         4
    coderay_bold_every:        10
    coderay_css:               style
    
    
VARIABLE
site
Sitewide information + configuration settings from  _config.yml. See below for details.
page
Page specific information + the YAML front matter. Custom variables set via the YAML Front Matter will be available here. See below for details.
content
In layout files, the rendered content of the Post or Page being wrapped. Not defined in Post or Page files.
paginator
When the paginate configuration option is set, this variable becomes available for use. See Pagination for details.    


site.time
The current time (when you run the jekyll command).
site.pages
A list of all Pages.
site.posts
A reverse chronological list of all Posts.
site.related_posts
If the page being processed is a Post, this contains a list of up to ten related Posts. By default, these are the ten most recent posts. For high quality but slow to compute results, run the  jekyll command with the --lsi (latent semantic indexing) option. Also note GitHub Pages does not support the lsi option when generating sites.
site.static_files
A list of all static files (i.e. files not processed by Jekyll's converters or the Liquid renderer). Each file has three properties: path,  modified_time and extname.
site.html_pages
A subset of `site.pages` listing those which end in `.html`.
site.html_files
A subset of `site.static_files` listing those which end in `.html`.
site.collections
A list of all the collections.
site.data
A list containing the data loaded from the YAML files located in the _data directory.
site.documents
A list of all the documents in every collection.
site.categories.CATEGORY
The list of all Posts in category CATEGORY.
site.tags.TAG
The list of all Posts with tag TAG.
site.[CONFIGURATION_DATA]
All the variables set via the command line and your _config.yml are available through the site variable. For example, if you have url: http://mysite.com in your configuration file, then in your Posts and Pages it will be stored in site.url. Jekyll does not parse changes to _config.yml in watch mode, you must restart Jekyll to see changes to variables.


page.content
The content of the Page, rendered or un-rendered depending upon what Liquid is being processed and what page is.
page.title
The title of the Page.
page.excerpt
The un-rendered excerpt of the Page.
page.url
The URL of the Post without the domain, but with a leading slash, e.g.  /2008/12/14/my-post.html
page.date
The Date assigned to the Post. This can be overridden in a Post’s front matter by specifying a new date/time in the format YYYY-MM-DD HH:MM:SS (assuming UTC), or YYYY-MM-DD HH:MM:SS +/-TTTT (to specify a time zone using an offset from UTC. e.g. 2008-12-14 10:30:00 +0900).
page.id
An identifier unique to the Post (useful in RSS feeds). e.g. /2008/12/14/my-post
page.categories
The list of categories to which this post belongs. Categories are derived from the directory structure above the _posts directory. For example, a post at /work/code/_posts/2008-12-24-closures.md would have this field set to ['work', 'code']. These can also be specified in the YAML Front Matter.
page.tags
The list of tags to which this post belongs. These can be specified in the YAML Front Matter.
page.path
The path to the raw post or page. Example usage: Linking back to the page or post’s source on GitHub. This can be overridden in the YAML Front Matter.
page.next
The next post relative to the position of the current post in site.posts. Returns nil for the last entry.
page.previous
The previous post relative to the position of the current post in site.posts. Returns nil for the first entry.