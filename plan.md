# What is this talk for?
Anyone can build a gem! …is what this presentation would be called if I was teaching you how to build a gem. But that is relatively straightforward and there are tons of tutorials which can leave you with a finished gem in about 10 minutes or less. *Because* gem-building is so accessible, I'm interested in what separates a 'pro' gem from an 'amateur' gem - and I don't mean in the functionality of what the gem does. I'm talking the meta-layer of everything else *but* the gem's functionality.  

###Things like:

- documentation
- tests
- proper license
- environment-awareness
- versioning
- clarity about Ruby version support
- general responsibility to the public

As we make the transition from fiddlers to deployers, these are some of the things we should keep in mind. That said, don't ever stop building, no matter how janky your code is. make it work, *then* make it right.


-----

# Main points

- Proper documentation
- Importance of testing re: gems
- License and contributions
	- open source and pull requests. again the importance of tests (this time your contributors' tests)
- Semantic version
- Travis (ruby version support)
- Respect to the global load path
	- directory structure
- Changelog, updating version, etc.

-----

# Topics / Slids

## The basic building blocks

- Bundler and Rake
- directory structure
	- global load path
- a smart .gemspec file
- use of VERSION constant
- Changelog

# 










