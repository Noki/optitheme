# Optitheme for Hugo

## Motivation

I started using Hugo quite some time ago. I heavily modified the theme to fit my needs and thought it's time to create a theme that fits my needs.

## Requirements

- [ ] Layout and Content
	- [x] Cookie consent at bottom
	- [x] Footer with privacy, imprint, terms of service
	- [x] Automatic TOC for long pages
	- [ ] Responsive images (modify figure template)
	- [x] Breadcrumbs
	- [ ] 404-Page
	- [x] Multi language support with translations
	- [ ] Meta data for author
	- [ ] Teasertext for content listings
	- [ ] Social sharing
		- [ ] Facebook
		- [ ] Twitter

- [ ] CSS
	- [x] CSS-grid module layout
	- [x] CSS-only off canvas menu
	- [ ] SCSS for e.g. colors configurable using params in config file
	- [ ] Print CSS

- [ ] Performance
	- [x] No external JavaScript libraries
	- [x] No external Fonts
	- [x] Minified HTML
		- [x] Disable Hugo Generator inject
	- [x] Minified CSS
	- [ ] Minified JavaScript
	- [ ] Minified Images	
	- [ ] Font-Awesome
		- [ ] Only required icons

- [ ] Audits and best practice
	- [ ] Validates in W3C
	- [ ] Pass Mobile friendly test
	- [ ] Score 100% in Google Lighthouse
		- [ ] Best practice
		- [ ] Progressive Web App
		- [ ] Best practice
		- [ ] Accessability
		- [ ] SEO 

- [ ] SEO
	- [x] self referencing canonical tag
	- [x] sitemap.xml	
		- [ ] do not include noindex in sitemap.xml
	- [x] robots.txt
		- [x] reference sitemap.xml
	- [x] Meta-Robots via front matter
	- [x] SEO Title via front matter
	- [x] Meta description via front matter
	- [ ] Schema.org markup

- [ ] Business / 
	- [x] Analytics
		- [x] anonymize IP
	- [ ] Adsense
	
- [ ] Documentation

## Template Settings

```
theme = "optitheme"
baseurl = "https://example.com/"
title = "Optitheme"
defaultContentLanguage = "en"
LanguageCode = "en"

paginate = 3
disableHugoGeneratorInject = true
disableKinds = ["taxonomyTerm"]
canonifyurls = true
enableRobotsTXT = true
timeout=20000
enableGitInfo = true

googleAnalytics = ""

[params]
	privacyPolicy = "privacy.html"

[languages]
    [languages.en]
		weight = 1
        languageName = "English"
        languageCode = "en"
		url = "/"		
		title = "Optitheme - EN"

    [languages.de]
		weight = 2
        languageName = "Deutsch"
        languageCode = "de"
        url = "/de/"
		title = "Optitheme - DE"	
		
[menu]
	[[menu.main]]
		identifier = "about"
		name = "About Optitheme"
		pre = ""
		url = "/about/"
		weight = -110

	[[menu.main]]
		identifier = "de/about"
		name = "Über Optitheme"
		pre = ""
		url = "/de/about/"
		weight = -110	

[taxonomies]
  categories = "categories"	
		
[privacy]
  [privacy.googleAnalytics]
    anonymizeIP = true
    disable = false
    respectDoNotTrack = false
    useSessionStorage = false

[imaging]
	resampleFilter = "Lanczos"
	quality = 80
	anchor = "smart" 
	
[sitemap]
	filename = "sitemap.xml"
	
[frontmatter]
	date = ["date", "publishDate", "lastmod", ":git"]
```


## Content Settings

Here is an example for front matter for a content. Please note: `true` and `false` should not be written in quotes to have an effect.

```
---
title: "Title"
description: "Description"
ot_seo_title: ""
ot_meta_description: ""
# ot_meta_robots: "noindex"
# ot_showdate: false
# ot_showads: false
# ot_showtoc: false
# ot_showlist: false
# ot_showinlist: false

date: 2018-08-29T00:00:00Z
# lastmod: 2018-08-29T00:00:00Z
# publishDate: 2018-08-29T00:00:00Z
# expiryDate: 9999-12-31T00:00:00Z

# draft: true
# url: /example-url.html

# categories:
#   - "example"
#   - "hello"

# menu:
#   main:
#     name: "Name in main menu"
#    weight: 4
#   footer:
#     name: "Name in footer menu"
#    weight: -1
---
```
