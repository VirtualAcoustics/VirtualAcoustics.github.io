
{:toc}
# Shock response with SEA - What to expect?
I got a chance to revisit an application of Statistical Energy Analysis (SEA) during some course work at KTH; the application of predicting high frequency shock response of plate-like structures, which I researched in my Masters Thesis one and a half decade ago. The analysed structure is shown below, comprised of five connected metal plates.

![](/images/logo.png "fast.ai's logo")

Shock waves in structures due to sudden release of energy are common in aerospace applications. Explosive bolts to separate rocket stages, latches and deployment of appendices are some examples. The shock load is often short in time and the frequency content of the propagating waves are high. In some cases, the analysis is performed up to 100 kHz. This requires a high element-density when using FE-methods to predict the shock wave propagation. That's where SEA comes in to play.

## Statistical Energy Analysis (SEA)
SEA was developed for analysing mid- to high-frequency acoustics and has been later on become a tool in vibro-acoustics. Instead of a calculating the deterministic responses of structures, a statistical approach is done by considering an average response of similar sub-structures. An "element" can be one of the plates in the presented structure.

A typical two-subsystem arrangement, depicted on the left, is commonly used to demonstrate the power flow in SEA. Eᵢ represents the vibro-acoustic energy of i:th subsystem and the power input to each system is Pᵢ. Each subsystem has a power-loss, ωηᵢEᵢ, where ω is the analysed center-frequency and ηᵢ is **the loss factor**. The energy exchange between the two subsystems are governed by the coupling loss factor η₁₂ and the reciprocal loss factor η₂₁. The power balance for the system may be set up and written

P₁ = ω η₁ E₁ + ω η₁₂ n₁ E₁ ( E₁/n₁ - E₂/n₂ ),

P₂ = ω η₂ E₂ + ω η₂₁ n₂ E₂ ( E₂/n₂ - E₁/n₁ ),

where the modal density nᵢ of the i:th subsystem has been introduced. This system of equations may be solved for the energy and the spatial averaged velocity squared may be calculated by, v² = Eᵢ / mᵢ, where m is the mass of the subsystem. The Shock Response Spectrum (SRS) is commonly used to evaluate the shock severity. Anyhow, let us keep it simple and stick to analysing the velocity and acceleration responses.

## What to expect?

Here's the table of contents:

1. TOC
{:toc}

## Basic setup

Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-filename.md`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `filename` is whatever file name you choose, to remind yourself what this post is about. `.md` is the file extension for markdown files.

The first line of the file should start with a single hash character, then a space, then your title. This is how you create a "*level 1 heading*" in markdown. Then you can create level 2, 3, etc headings as you wish but repeating the hash character, such as you see in the line `## File names` above.

## Basic formatting

You can use *italics*, **bold**, `code font text`, and create [links](https://www.markdownguide.org/cheat-sheet/). Here's a footnote [^1]. Here's a horizontal rule:

---

## Lists

Here's a list:

- item 1
- item 2

And a numbered list:

1. item 1
1. item 2

## Boxes and stuff

> This is a quotation

{% include alert.html text="You can include alert boxes" %}

...and...

{% include info.html text="You can include info boxes" %}

## Images

![](/images/logo.png "fast.ai's logo")

## Code

General preformatted text:

    # Do a thing
    do_thing()

Python code and output:

```python
# Prints '2'
print(1+1)
```

    2

## Tables

| Column 1 | Column 2 |
|-|-|
| A thing | Another thing |

## Footnotes

[^1]: This is the footnote.
