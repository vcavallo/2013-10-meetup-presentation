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

"ok, the end - and for anyone who just woke up, that was the presentation on how to make 20 million dollars on the internet"

-----

# Main points

- Proper documentation
- Importance of testing re: gems
- License and contributions
	- open source and pull requests. again the importance of tests (this time your contributors' tests)
- ~~Semantic version~~
- Travis (ruby version support)
- ~~Respect to the global load path~~
	- ~~directory structure~~
- ~~Changelog, updating version, etc.~~

-----

# Topics / Slides

## The basic building blocks

- Bundler and Rake
- directory structure
	- global load path
- a smart .gemspec file
	- use of VERSION constant (will be mentioned later)
- Changelog - which segues into…

## Semantic Versioning

- What it is and how to use it
- in practice - the use of a VERSION constant 
	- aside from making the .gemspec smarter, this bakes the concept of your gem's version right into the code, rather than relying on RubyGems.org. there are other platforms for sharing gems.  You want the version to be an aspect of the software, not the distribution platform
- not gonna get into all the details of semantic versioning, but basically:
	- MAJOR.MINOR.PATCH
	- major versions either are not backwards compatible to you want to declare a big release change
	- minor versions are backwards compatible and probably introduce a new feature or similar change
	- patch versions fix bugs or make other very minor changes

## Travis

- probably not hugely important early on? 
- Continuous Integration - after any commit, Travis will build the project in various contexts - along with running tests - to make sure that it isn't broken. Working solo this isn't a really big deal, but i'd imagine that on a larger team you'd want to know immediately if a recent commit broke the code, exactly which commit did it (and **who** did it!)

## Testing

- Always important! Doubly-so for gems and other public releases.
- the obvious: allows you to make sure that your updates and refactors are not breaking code. 
- the slightly less obvious: allows prospective users to:
	1. verify that your code is borked.
	2. 











