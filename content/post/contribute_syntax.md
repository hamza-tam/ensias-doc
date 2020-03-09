---
title: "Syntax guide for post writing"
date: 2020-03-09T11:52:35+01:00
tags: ["contribute"]
contributor: "Hamza Tamenaoul"
draft: false
---

## Headings

```
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

## Text

```
*This text will be italic*
_This will also be italic_

**This text will be bold**
__This will also be bold__

_You **can** combine them_
```

*This text will be italic*

_This will also be italic_

**This text will be bold**

__This will also be bold__

_You **can** combine them_

## Lists

### Unordered

```
* Item 1
* Item 2
    * Item 2a
    * Item 2b
```

* Item 1
* Item 2
    * Item 2a
    * Item 2b

### Ordered

```
1. Item 1
1. Item 2
1. Item 3
    1. Item 3a
    1. Item 3b
```

1. Item 1
1. Item 2
1. Item 3
    1. Item 3a
    1. Item 3b

## Links

```
https://cupper-hugo-theme.netlify.com/

[Cupper hugo theme](https://cupper-hugo-theme.netlify.com/)
```

https://cupper-hugo-theme.netlify.com/

[Cupper hugo theme](https://cupper-hugo-theme.netlify.com/)

## Blockquotes

```
As Kanye West said:

> We're living the future so
> the present is our past.
```

As Kanye West said:

> We're living the future so
> the present is our past.

## Tables

```
| Animal  | Sounds |
|---------|--------|
| Cat     | Meow   |
| Dog     | Woof   |
| Cricket | Chirp  |
```

| Animal  | Sounds |
|---------|--------|
| Cat     | Meow   |
| Dog     | Woof   |
| Cricket | Chirp  |

## Inline code

```
This `<html>` tag is inline code.
```

This `<html>` tag is inline code.

## Block code

````
This

```
<html>
```

tag is block code. 
````

This

```
<html>
```

tag is block code. 


## blockquote

```
{{</* blockquote author="Carl Jung" */>}}
Even a happy life cannot be without a measure of darkness, and the word happy would lose its meaning if it were not balanced by sadness. It is far better to take things as they come along with patience and equanimity.
{{</* /blockquote */>}}
```

{{< blockquote author="Carl Jung" >}}
Even a happy life cannot be without a measure of darkness, and the word happy would lose its meaning if it were not balanced by sadness. It is far better to take things as they come along with patience and equanimity.
{{< /blockquote >}}

## note

```
{{</* note */>}}
This is a note! It's something the reader may like to know about but is supplementary to the main content. Use notes when something may be interesting but not critical.
{{</* /note */>}}
```

{{< note >}}
This is a note! It's something the reader may like to know about but is supplementary to the main content. Use notes when something may be interesting but not critical.
{{< /note >}}

## warning note

```
{{</* warning */>}}
This is a warning! It's about something the reader should be careful to do or to avoid doing. Use warnings when something could go wrong.
{{</* /warning */>}}
```

{{< warning >}}
This is a warning! It's about something the reader should be careful to do or to avoid doing. Use warnings when something could go wrong.
{{< /warning >}}

## cmd

```
{{</* cmd */>}}
hugo server --gc
{{</* /cmd */>}}
```

{{< cmd >}}
hugo server --gc
{{< /cmd >}}

## code

```
{{</* code numbered="true" */>}}
<div [[[role="dialog"]]] [[[aria-labelledby="dialog-heading"]]]>
  <button [[[aria-label="close"]]]>x</button>
  <h2 [[[id="dialog-heading"]]]>Confirmation</h2>
  <p>Press Okay to confirm or Cancel</p>
  <button>Okay</button>
  <button>Cancel</button>
</div>
{{</* /code */>}}

1. The dialog is only announced as a dialog if it takes the `dialog` ARIA role
2. The `aria-labelledby` relationship attribute makes the element carrying the `id` it points to its label
3. The close button uses `aria-label` to provide the text label "close", overriding the text content
4. The heading is used as the dialog's label. The `aria-labelledby` attribute points to its `id`
```

{{< code numbered="true" >}}
<div [[[role="dialog"]]] [[[aria-labelledby="dialog-heading"]]]>
  <button [[[aria-label="close"]]]>x</button>
  <h2 [[[id="dialog-heading"]]]>Confirmation</h2>
  <p>Press Okay to confirm or Cancel</p>
  <button>Okay</button>
  <button>Cancel</button>
</div>
{{< /code >}}

1. The dialog is only announced as a dialog if it takes the `dialog` ARIA role
2. The `aria-labelledby` relationship attribute makes the element carrying the `id` it points to its label
3. The close button uses `aria-label` to provide the text label "close", overriding the text content
4. The heading is used as the dialog's label. The `aria-labelledby` attribute points to its `id`

## syntax highlighting

To get syntax highlighting for your code, use markdown code fences, then specify the language:

````
```html
<div role="dialog" aria-labelledby="dialog-heading">
  <button aria-label="close">x</button>
  <h2 id="dialog-heading">Confirmation</h2>
  <p>Press Okay to confirm or Cancel</p>
  <button>Okay</button>
  <button>Cancel</button>
</div>
```
````

```html
<div role="dialog" aria-labelledby="dialog-heading">
  <button aria-label="close">x</button>
  <h2 id="dialog-heading">Confirmation</h2>
  <p>Press Okay to confirm or Cancel</p>
  <button>Okay</button>
  <button>Cancel</button>
</div>
```

## colors

```
{{</* colors "#111111, #cccccc, #ffffff" */>}}
```

{{< colors "#111111, #cccccc, #ffffff" >}}

## expandable

```
{{</* expandable label="A section of dummy text" level="2" */>}}
Here is some markdown including [a link](https://twitter.com/heydonworks). Donec erat est, feugiat a est sed, aliquet pharetra ipsum. Vivamus in arcu leo. Praesent feugiat, purus a molestie ultrices, libero massa iaculis ante, sit amet accumsan leo eros vel ligula.
{{</* /expandable */>}}
```

{{< expandable label="A section of dummy text" level="2" >}}
Here is some markdown including [a link](https://twitter.com/heydonworks). Donec erat est, feugiat a est sed, aliquet pharetra ipsum. Vivamus in arcu leo. Praesent feugiat, purus a molestie ultrices, libero massa iaculis ante, sit amet accumsan leo eros vel ligula.
{{< /expandable >}}

## fileTree

```
{{</* fileTree */>}}
* Level 1 folder
    * Level 2 file
    * Level 2 folder
        * Level 3 file
        * Level 3 folder
            * Level 4 file
        * Level 3 folder
            * Level 4 file
            * Level 4 file
        * Level 3 file
    * Level 2 folder
        * Level 3 file
        * Level 3 file
        * Level 3 file
    * Level 2 file
* Level 1 file
{{</* /fileTree */>}}
```

{{< fileTree >}}
* Level 1 folder
    * Level 2 file
    * Level 2 folder
        * Level 3 file
        * Level 3 folder
            * Level 4 file
        * Level 3 folder
            * Level 4 file
            * Level 4 file
        * Level 3 file
    * Level 2 folder
        * Level 3 file
        * Level 3 file
        * Level 3 file
    * Level 2 file
* Level 1 file
{{< /fileTree >}}

## ticks

```
{{</* ticks */>}}
* Selling point one
* Selling point two
* Selling point three
{{</* /ticks */>}}
```

{{< ticks >}}
* Selling point one
* Selling point two
* Selling point three
{{< /ticks >}}

## wcag

See the [full wcag list](https://github.com/zwbetz-gh/cupper-hugo-theme/blob/master/data/wcag.json). 

```
{{</* wcag include="1.2.1, 1.3.1, 4.1.2" */>}}
```

{{< wcag include="1.2.1, 1.3.1, 4.1.2" >}}

## tested

See the [full browser list](https://github.com/zwbetz-gh/cupper-hugo-theme/tree/master/static/images).

```
{{</* tested using="Firefox + JAWS, Chrome, Safari iOS + Voiceover, Edge" */>}}
```

{{< tested using="Firefox + JAWS, Chrome, Safari iOS + Voiceover, Edge" >}}

## Math

Some math:

```
$$ \varphi = \dfrac{1+\sqrt5}{2}= 1.6180339887… $$
```

$$ \varphi = \dfrac{1+\sqrt5}{2}= 1.6180339887… $$

More math: 

```
$$
\varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } } 
$$
```

$$
\varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } } 
$$
