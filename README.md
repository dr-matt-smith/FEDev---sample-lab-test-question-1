[back to assessments](https://github.com/dr-matt-smith/FEDev---assessment-samples-and-walkthroughs?tab=readme-ov-file) <<<

Question 1 
| [Question 1](https://github.com/dr-matt-smith/FEDev-practical-sample-question-1)
| [Question 2](https://github.com/dr-matt-smith/FEDev-practical-sample-question-2)
| [Question 3](https://github.com/dr-matt-smith/FEDev-practical-sample-question-3)
| [Question 4](https://github.com/dr-matt-smith/FEDev-practical-sample-question-4)
| [Question 5](https://github.com/dr-matt-smith/FEDev-practical-sample-question-5)
| [Question 6](https://github.com/dr-matt-smith/FEDev-practical-sample-question-6)

# FEDEv - SAMPLE lab test question 1

The "brief" for the test is a PDF file in directory "brief"

NOTE:
**no use of AI is permitted in the lab test**

There are videos for each of the 6 questions:


The files in this repo are the solution I created to this sample test
- you may use any editor available on the university PCs
  - I used Celbridge, which you may install on the lab PCs if you wish

## Question 1 - video

- question 1
  - https://go.screenpal.com/watch/cOehqAnZFeO
  - 7mins 52secs


## Question 1a - nav bar links

To make every page have a nav bar, we can add links into the site `/routes/+layout.svelte`:

Add these links above `{@render children()}`:

```html
<nav>
  <a href="/">home</a>
  |
  <a href="/privacy">privacy</a>
  |
  <a href="/food">food</a>
  |
  <a href="/evenform">form to input number and test its even'ness</a>

</nav>
<hr>
```

So the full listing for the site layout is:

`/routes/+layout.svelte`

```html
<script>
  import favicon from '$lib/assets/favicon.svg';

  let { children } = $props();
</script>

<svelte:head>
  <link rel="icon" href={favicon} />
</svelte:head>

<nav>
  <a href="/">home</a>
  |
  <a href="/privacy">privacy</a>
  |`
  <a href="/food">food</a>
  |
  <a href="/evenform">form to input number and test its even'ness</a>

</nav>
<hr>

{@render children()}
```

## Question 1a - HTML titles

HTML `<head>` titles can be set by each page individually with `<svelte:head>` elements, e.g. for the privacy page we can add:

`/routes/privacy/+page.svelte`

```html
<svelte:head>
  <title>-- privacy --</title>
</svelte:head>
```


## Question 2 route `/`

Our home page needs a title in the head, a level 1 heading and a level 2 heading.

`/routes/+page.svelte`

```html
<svelte:head>
  <title>-- home --</title>
</svelte:head>

<h1>Welcome to our website</h1>
<h2>level 2 heading “have a nice day”</h2>
```


## Question 2 route `/privacy`

Our privacy page needs a title in the head, a level 1 heading and a paragraph.

`/routes/privacy/+page.svelte`
```html

<svelte:head>
  <title>-- privacy --</title>
</svelte:head>

<h1>Privacy Policy</h1>

<p>
  we collect as much data as we can to improve our
  marketing emails
</p>
```

