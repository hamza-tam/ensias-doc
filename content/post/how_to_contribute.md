---
title: "How to contribute"
date: 2020-03-05T15:52:35+01:00
tags: ["contribute"]
contributor: "Hamza"
draft: false
---

## Introduction

Since the sole goal of this project is to promote the exchange of information between students (and why not even teachers), it relies heavily on contributions. The purpose of this tutorial is to give enough information to make anyone capable of participating in the writing of new tutorials to be able to do so easily.

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

## The architeture of the content management

To ensure that the posts stay organized a simple architeture have been set. This architeture is simply used as a start but following the rules is very important for the organisation of the system. The architeture is as follows

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
date: 2020-03-05T15:52:35+01:00 // Timestamp of the article
updated: 2020-03-09T10:18:48+01:00
tags: ["tag1", ...] // List your tags here
clubs: ["club1", ...] // List the name of the clubs
contributor: "Your name"
draft: false
---

You can start writing your article here
```

{{< warning >}}
title, date, contributor are mandatory
{{< /warning >}}
