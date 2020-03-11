---
title: "How to contribute"
date: 2020-03-05T15:52:35+01:00
tags: ["contribute"]
contributor: "Hamza Tamenaoul"
draft: false
---

## Introduction

Since the sole goal of this project is to promote the exchange of information between students (and why not even teachers), it relies heavily on contributions. The purpose of this tutorial is to give enough information to make anyone capable of participating in the writing of new tutorials to be able to do so easily.

To have an idea about the syntax, visit the [syntax guide]({{< ref "contribute_syntax.md" >}}).

## Prerequisites

The following things should be installed on your machine:

- Git
- Hugo (Optional)

## Procedure to contribute

You'll need to follow the following steps to be able to contribute to the project:
1. Fork the [Github](https://github.com/hamza-tam/ensias-doc/) repository
1. Pull the new forked Repository
1. Write your article according to the next sections
1. Make a pull request to the repository
1. Wait for the merge ;)

## The architecture of the content management

To ensure that the posts stay organized a simple architecture has been set. This architecture is simply used as a start but following the rules is very important for the organization of the system. The architecture is as follows

{{< fileTree >}}
* content
  * club
  * post
{{< /fileTree >}}

### Club

contains the posts related to clubs. All the posts in this folder should be prefixed by the name of the club. **consistency is key** for the sake of extensibility of the platform. 

{{< note >}}
Don't forget to prefix the posts
{{< /note >}}

### post

This folder contain all the tutorials. Any post not related to any club should be stored in this folder.


{{< warning >}}
Use meaningful long names for posts
{{< /warning >}}


## The basic skeleton of a post

A post markdown file should have the following skeleton to be perfectly integrated in the system:

```
---
title: "A meaningful title"
date: 2020-03-05T15:52:35+01:00 
tags: ["tag1", "..."] 
clubs: ["club1", "..."] 
contributor: "Your name"
draft: false
---

You can start writing your article here
```

{{< warning >}}
title, date, contributor are mandatory
{{< /warning >}}

You can remove either the tag or the club name if it's not useful.

{{< note >}}
Don't forget to clean this template (Change the date, the tag and club names).
{{< /note >}}

## Suggestions or modification

Any suggestions or contribution is welcomed. 

For suggestions, problems, or modification requests open an issue in the Github repository.

For contributions, just make a pull request describing the modification made.
