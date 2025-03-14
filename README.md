# Bad Naming Examples

> There are only two hard things in Computer Science: cache invalidation and naming things.
> 
> -- Phil Karlton

I usually prefer to list positive things. However, when it comes to naming things, this approach doesn't work.

Good names are simply obvious and clear. They blend in seamlessly since the name aligns perfectly with the context.

That's why I've listed some examples of bad naming (in the context of software development) here.

# General

## test

Naming something just "test" is always a bad idea.

Later, when you want to search for the string in your configuration, your code, or your logs, you'll be lost.

In non-trivial projects, the term "test" will appear thousands of times.

Using the prefix "test" is fine, but please add some more characters!

Example: "test-of-reconnect"

If you search for that string, you won't get duplicate results.

# Some expamles

## pre-commit.com

[pre-commit.com](//pre-commit.com) is a fantastic tool that ensures you don't inadvertently commit items into Git that you didn't intend to.

However, its name is too general. When I use my favorite search engine to look up a specific feature (e.g., "pre-commit foo"), I encounter numerous irrelevant results.

For most, "pre-commit" primarily refers to the **Git** pre-commit hooks.

## Kind

[kind](https://kind.sigs.k8s.io/) stands for "Kubernetes in Docker".

Its name can be misleading due to its generality. Searching for "kind foo" might not yield the desired results.

Furthermore, in the context of Kubernetes, the yaml manifests contain entries like "Kind: Pod", which is an entirely different concept.

Grrr.

## Longhorn: Node

Kubernetes uses the term "node". Longhorn uses the same term for their CustomResourceDefinitionn for Kubernetes nodes which gets used by Longhorn. Technically there is no issue, since
Kubernetes uses "Group Version Kind" to address resources, but for humans it can be confusing.

Longhorn should have used a different term.

## TOKEN

If write a tool which connects to some API and it needs a token, it is common to read that from an environment variable.

Do not call that env var TOKEN. This is too generic. Sooner or later your application might connect to a second service.

If you need a token to connect to service Foo, then call it FOO_TOKEN.

## Github action: fetch-depth: 0

```yaml
      - name: Checkout repository
        uses: actions/checkout@latest
        with:
          fetch-depth: 0
```

For me `0` means nothing, or at least only little. 

Upstream docs:

>  0 indicates all history for all branches and tags.

This is confusing. I guess many people think "Checkout zero history", when they read that....

# Related

* [Thomas WOL: Working Out Loud](https://github.com/guettli/wol)

# Feedback

I love feedback and I love to hear from you. Just create an issue and tell me what's on your mind.
