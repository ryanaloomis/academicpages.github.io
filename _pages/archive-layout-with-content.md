---
title: "Archive Layout with Content"
layout: archive
permalink: /archive-layout-with-content/
---

A variety of common markup showing how the theme styles them.

# Header one

## Header two

### Header three

#### Header four

##### Header five

###### Header six

## Blockquotes

Single line blockquote:

> Quotes are cool.

## Tables

| --------         | ------ | ------------------------------------------------------------ |
| [John Doe](#)    | 2016   | Description of the item in the list                          |
| [Jane Doe](#)    | 2019   | Description of the item in the list                          |
| [Doe Doe](#)     | 2022   | Description of the item in the list                          |



<div class="container">
    <h2>Scientific Interests</h2>
    Star and planet formation, protoplanetary disks, exoplanets, statistics, radio astronomy, transients, instrumentation.
</div>

<div class="container">
    <h2>Education</h2>
  <table class="table table-striped">
      <tr>
      <td>2012 - 2016</td>
      <td>Ph.D. <em>Astronomy and Astrophysics</em>, Harvard University</td>
      </tr>
      <tr>
      <td>2010 - 2012</td>
      <td>Masters of Arts in <em>Astronomy and Astrophysics</em>, Harvard University</td>
      </tr>
      <tr>
      <td>2006 - 2010</td>
      <td>Bachelors of Science in <em>Aerospace Engineering; Astronomy</em>, University of Virginia <br>
      Graduated with High Distinction, Tau Beta Pi, Jefferson Scholar (full scholarship)</td>
      </tr>
  </table>
</div>


<div class="container">
    <h2>Scientific Research</h2>
  <table class="table table-striped">
      <tr>
          <td>2013 - 2016</td>
          <td><strong>Ph.D. Thesis</strong>: <em>The Fundamental Properties of Young Stars</em>, CfA, advised by Dr. Sean Andrews</td>
      </tr>
      <tr>
          <td> 2012 </td>
          <td><em>MMTCam Commissioning</em>, CfA, advised by Dr. Warren Brown</td>
      </tr>
      <tr>
          <td>2010 - 2012 </td>
          <td><strong>Masters project</strong>: <em>Intermediate Luminosity Transients</em>, CfA, advised by Dr. Edo Berger</td>
      </tr>
      <tr>
          <td>2009 - 2010 </td>
          <td><em>PAPER Instrumentation Study</em>, University of Virginia, advised by Dr. Richard Bradley</td>
      </tr>
      <tr>
          <td>2009 - 2010</td>
          <td><em>ALMA Collaborative Engineering Study</em>, Santiago, Chile, advised by Drs. Kelsey Johnson and Alison Peck</td>
      </tr>
      <tr>
          <td>2009</td>
          <td><em>Circumstellar Disks</em>, Smithsonian Astrophysical Observatory REU Intern, advised by Dr. Sean Andrews</td>
      </tr>
  </table>
</div>



## Definition Lists

Definition List Title
:   Definition list division.

Startup
:   A startup company or startup is a company or temporary organization designed to search for a repeatable and scalable business model.

#dowork
:   Coined by Rob Dyrdek and his personal body guard Christopher "Big Black" Boykins, "Do Work" works as a self motivator, to motivating your friends.

Do It Live
:   I'll let Bill O'Reilly [explain](https://www.youtube.com/watch?v=O_HyZ5aW76c "We'll Do It Live") this one.

## Unordered Lists (Nested)

  * List item one 
      * List item one 
          * List item one
          * List item two
          * List item three
          * List item four
      * List item two
      * List item three
      * List item four
  * List item two
  * List item three
  * List item four

## Ordered List (Nested)

  1. List item one 
      1. List item one 
          1. List item one
          2. List item two
          3. List item three
          4. List item four
      2. List item two
      3. List item three
      4. List item four
  2. List item two
  3. List item three
  4. List item four

## Buttons

Make any link standout more when applying the `.btn` class.

## Notices

**Watch out!** You can also add notices by appending `{: .notice}` to a paragraph.
{: .notice}

## HTML Tags

### Address Tag

<address>
  1 Infinite Loop<br /> Cupertino, CA 95014<br /> United States
</address>

### Anchor Tag (aka. Link)

This is an example of a [link](http://github.com "Github").

### Abbreviation Tag

The abbreviation CSS stands for "Cascading Style Sheets".

*[CSS]: Cascading Style Sheets

### Cite Tag

"Code is poetry." ---<cite>Automattic</cite>

### Code Tag

You will learn later on in these tests that `word-wrap: break-word;` will be your best friend.

### Strike Tag

This tag will let you <strike>strikeout text</strike>.

### Emphasize Tag

The emphasize tag should _italicize_ text.

### Insert Tag

This tag should denote <ins>inserted</ins> text.

### Keyboard Tag

This scarcely known tag emulates <kbd>keyboard text</kbd>, which is usually styled like the `<code>` tag.

### Preformatted Tag

This tag styles large blocks of code.

<pre>
.post-title {
  margin: 0 0 5px;
  font-weight: bold;
  font-size: 38px;
  line-height: 1.2;
  and here's a line of some really, really, really, really long text, just to see how the PRE tag handles it and to find out how it overflows;
}
</pre>

### Quote Tag

<q>Developers, developers, developers&#8230;</q> &#8211;Steve Ballmer

### Strong Tag

This tag shows **bold text**.

### Subscript Tag

Getting our science styling on with H<sub>2</sub>O, which should push the "2" down.

### Superscript Tag

Still sticking with science and Isaac Newton's E = MC<sup>2</sup>, which should lift the 2 up.

### Variable Tag

This allows you to denote <var>variables</var>.

{% include base_path %}
{% for post in site.pages %}
{% include archive-single.html %}
{% endfor %}