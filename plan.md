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

###things to mention:

- it's all about expectations and consistency. think about when you use some new application - there, you're probably done thinking about it because it doesn't take much forethought. you expect it to work. 

-----

# Main points

- ~~Proper documentation~~
- ~~Importance of testing re: gems~~
- ~~License and contributions~~
	- ~~open source and pull requests. again the importance of tests (this time your contributors' tests)~~
- ~~Semantic version~~
- ~~Travis (ruby version support)~~
- ~~Respect to the global load path~~
	- ~~directory structure~~
- ~~Changelog, updating version, etc.~~

-----

# Topics / Slides

## The basic building blocks

- Bundler and Rake are your friend for this. there are also plenty of gems to help create proper skeletons. i didn't use them.
- directory structure, naming, conventions, etc.
	- global load path. very important. - a good example of why best-practices matter.
- a smart .gemspec file
	- use of VERSION constant (will be mentioned later)
	- proper dependencies (especially if using older version of gems, use `~>`)
- Changelog (it's also just fun to look back at this! like reading an old journal. learn from your own past.) - which segues into…

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
	1. verify that your code is not borked.
	3. allow for easy contribution (we'll come back to this soon)
	2. get a quick sense of the API ("it should make you a pizza. it should ask what toppings you want.") thanks to RSpec's nice readable format. (we'll come back to this even sooner)
- simplecov - it is a great feeling to see 100% test coverage AND all passing tests. 

## Documentation

- as mentioned in testing, documentation is important.
- Why? how many times have you read the documentation for a piece of software to see how to use it? like a million. that's how you know how to use it. 
- for something simple like a gem it's not the end of the world, but you don't know where the project will go. add proper documentation early and it will grow with the project. 
- it helps you write code. change your psuedocode into documentation as it comes to life. it's not that hard. 
- it's just the community best-practice rule. it's part of releasing software. things need instructions.

## Contributions

- this seems like a good place to mention a license. use one. the MIT license can be used by all. be sure to mention your contributors.
- make it clear in your readme with a "contributions" section. request that those interested fork, submit a pull request, update the changelog and write tests. 
- their tests will increase your confidence in their work as well as explain what they set out to do. 
- the more you adhere to general best practices, the easier it is for others to guess how your gem works and contribute in a normalized way. 








