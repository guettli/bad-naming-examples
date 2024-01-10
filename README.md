# Bad Naming Examples

> There are only two hard things in Computer Science: cache invalidation and naming things.
> 
> -- Phil Karlton

I usually prefer to list positive things. However, when it comes to naming things, this approach doesn't work.

Good names are simply obvious and clear. They blend in seamlessly since the name aligns perfectly with the context.

That's why I've listed some examples of bad naming (in the context of software development) here.

# General

# test

To give something the name "test" is allways a bad idea.

Later you want to search for the string in your configuration, your code or your logs .... and then you are lost.

In non-trivial projects the term "test" will appear thousand times.

Using the prefix "test" is fine, but please add some more charaters!

Example: "test-of-reconnect"

If you search for that string, then you won't get duplicate results.

# Product Names

## pre-commit.com

[pre-commit.com](//pre-commit.com) is a fantastic tool that ensures you don't inadvertently commit items into Git that you didn't intend to.

However, its name is too general. When I use my favorite search engine to look up a specific feature (e.g., "pre-commit foo"), I encounter numerous irrelevant results.

For most, "pre-commit" primarily refers to the **Git** pre-commit hooks.

## Kind

[kind](https://kind.sigs.k8s.io/) stands for "Kubernetes in Docker".


Its name can be misleading due to its generality. Searching for "kind foo" might not yield the desired results.

Furthermore, in the context of Kubernetes, the yaml manifests contain entries like "Kind: Pod", which is an entirely different concept.

Grrr.


# Related

* [Thomas WOL: Working out Loud](https://github.com/guettli/wol)

# Feedback

I love feedback and I love to hear from you. Just create an issue and tell me what's on your mind.

