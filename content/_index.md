---
title: "ENSIAS Doc"
---

# **Welcome to ENSIAS Doc !!**

## What is ENSIAS Doc

ENSIAS Doc is a wiki for ENSIAS engineering school. Its aim is to provide the foundation for students to have access to a lot of resources and information about the school education.

All of the information presented will be for the sake of knowledge sharing and information gathering.

## Suggestions or modifications

Any suggestions or contribution is welcomed. 

For suggestions, problems, or modification requests open an issue in the Github repository.

For contributions, just make a pull request describing the modification made.

## Global architecture

This small project is a statically generated website. Its global architecture as follows:

```
+--------+     +--------+     +------+     +---------+
| Github | --> | Gitlab | --> | Hugo | --> | Publish |
+--------+     +--------+     +------+     +---------+
```

Any new commit to the master branch on the Github Repo is loaded into Gitlab CI/CD, where a Hugo pipeline is run to generate the website artifact. 
