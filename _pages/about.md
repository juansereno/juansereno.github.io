---
layout: default
title: about
permalink: /

# ---------------------------------------------------------------------------
# Welcome photo at the top of the home page.
# "typed" lines are written one after another in a loop.
# ---------------------------------------------------------------------------
hero:
  image: dubrovnik-hero.jpg
  title: Juan E. Sereno, Ph.D.
  subtitle: Incoming Postdoctoral Researcher at the University of Dubrovnik
  typed:
    - We can only see a short distance ahead,
    - but we can see plenty there that needs to be done. — A. Turing
    - Welcome to my homepage!
  credit: 'Photo: <a href="https://commons.wikimedia.org/wiki/File:Dubrovnik_as_seen_from_Sr%C4%91_-_September_2017.jpg">Martin Falbisoner</a>, <a href="https://creativecommons.org/licenses/by-sa/4.0/">CC BY-SA 4.0</a>'

# ---------------------------------------------------------------------------
# Left sidebar: edit the photo, name, short bio and the list of links here.
# Icons: "fa-..." are Font Awesome (fontawesome.com/icons),
#        "ai ai-..." are Academicons (jpswalsh.github.io/academicons).
# Remove "url" for an item that should not be a link.
# ---------------------------------------------------------------------------
sidebar:
  image: prof_pic.jpg
  name: Juan E. Sereno
  bio: Control theory • mathematical modelling • biomedical systems.
  items:
    - icon: fa-solid fa-location-dot
      text: Dubrovnik, Croatia
      url: https://maps.app.goo.gl/geJ6Bbeaj82wCTnZ6
    - icon: fa-solid fa-building-columns
      text: University of Dubrovnik
      url: https://www.unidu.hr/eng/
    - icon: fa-solid fa-envelope
      text: Email
      url: mailto:jeserenom@gmail.com
    - icon: ai ai-google-scholar
      text: Google Scholar
      url: https://scholar.google.com/citations?user=KMzVSbMAAAAJ&hl=en
      color: "#4285f4"
    - icon: ai ai-orcid
      text: ORCID
      url: https://orcid.org/0000-0002-8498-1277
      color: "#a6ce39"
    - icon: ai ai-researchgate
      text: ResearchGate
      url: https://www.researchgate.net/profile/Juan-Sereno
      color: "#00ccbb"
    - icon: fa-brands fa-linkedin
      text: LinkedIn
      url: https://www.linkedin.com/in/juan-sereno-3252b3232
      color: "#0a66c2"
    - icon: fa-brands fa-github
      text: GitHub
      url: https://github.com/juansereno
    - icon: fa-brands fa-bluesky
      text: Bluesky
      url: https://bsky.app/profile/jeserenom.bsky.social
      color: "#1185fe"
    - icon: ai ai-cv
      text: CV (PDF)
      url: /assets/pdf/CV_Sereno.pdf

announcements:
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: # leave blank to include all the news in the `_news` folder

latest_posts:
  scrollable: true
  limit: 3
---

{% comment %} ------------------------- Edit your bio here ------------------------- {% endcomment %}
{% capture bio %}

From **1 November 2026** I will join the [University of Dubrovnik](https://www.unidu.hr/eng/) as a postdoctoral researcher on the [Conduction / InterCoML](https://conduction.unidu.hr/) project, working on infinite-dimensional optimal control under the supervision of Prof. dr. [Martin Lazar](https://www.martin-lazar.from.hr/). Until September 2026 I was a postdoctoral research fellow at the [University of Idaho](https://www.uidaho.edu/), in the Department of Mathematics and Statistical Science, where I worked in the [SMID Lab](https://www.systemsmedicine.de/) under the supervision of Prof. [Esteban A. Hernandez-Vargas](https://scholar.google.com/citations?user=mbo1boUAAAAJ&hl=en).

I obtained my Ph.D. in Mathematical Engineering from the [Universidad Nacional del Litoral](https://www.unl.edu.ar/), Argentina, under the supervision of Prof. [Alejandro H. González](https://scholar.google.com/citations?user=1urE4oMAAAAJ&hl=en), with a thesis on predictive controllers for hybrid systems applied to socio-biomedical processes. Before that I completed an M.Sc. in Industrial Automation and a B.E. in Control Engineering at the [Universidad Nacional de Colombia](https://unal.edu.co/).

My work sits between control theory and mathematical biology: **model predictive control**, **adaptive observers**, **reduced-order modelling** and **nonlinear mixed-integer optimization**, applied to infectious diseases, diabetes and medical digital twins.

I am always glad to discuss research and new collaborations — feel free to [get in touch](mailto:jeserenom@gmail.com).

{% endcapture %}
{% comment %} ------------------------------------------------------------------- {% endcomment %}

<section class="jes-hero" style="background-image: url('{{ page.hero.image | prepend: '/assets/img/' | relative_url }}');">
<style>
  body { overflow-x: clip; }
  .jes-hero { position: relative; left: 50%; width: 100vw; margin-left: -50vw; margin-top: -3rem; margin-bottom: 3rem;
    height: 45vh; min-height: 300px; max-height: 480px; background-size: cover; background-position: center 55%; display: flex; align-items: center; }
  .jes-hero::before { content: ""; position: absolute; inset: 0; background: linear-gradient(90deg, rgba(5, 13, 24, 0.75) 0%, rgba(5, 13, 24, 0.5) 55%, rgba(5, 13, 24, 0.25) 100%); }
  .jes-hero-inner { position: relative; z-index: 1; width: 100%; max-width: 930px; margin: 0 auto; padding: 0 15px; color: #fff; }
  .jes-hero h1 { color: #fff; font-size: clamp(2rem, 4.5vw, 3.4rem); font-weight: 700; margin: 0 0 0.75rem; text-shadow: 0 2px 12px rgba(0, 0, 0, 0.45); }
  .jes-hero p { color: #fff; font-size: clamp(1.05rem, 2.2vw, 1.6rem); margin: 0; text-shadow: 0 1px 8px rgba(0, 0, 0, 0.5); }
  .jes-typed { color: #fff; display: inline-block; min-height: 1.4em; border-bottom: 3px solid var(--global-theme-color); padding-bottom: 2px; margin-top: 0.4rem; }
  .jes-typed::after { content: "|"; margin-left: 2px; animation: jes-blink 0.8s step-end infinite; }
  @keyframes jes-blink { 50% { opacity: 0; } }
  .jes-hero-credit { position: absolute; z-index: 1; right: 0.75rem; bottom: 0.5rem; font-size: 0.7rem; color: rgba(255, 255, 255, 0.75); }
  .jes-hero-credit a { color: rgba(255, 255, 255, 0.9); text-decoration: underline; }
  @media (prefers-reduced-motion: reduce) { .jes-typed::after { animation: none; } }
</style>
  <div class="jes-hero-inner">
    <h1>{{ page.hero.title }}</h1>
    <p>{{ page.hero.subtitle }}</p>
    <p><span class="jes-typed" data-items="{{ page.hero.typed | join: '|' | escape }}">{{ page.hero.typed | first }}</span></p>
  </div>
  <div class="jes-hero-credit">{{ page.hero.credit }}</div>
<script>
  (function () {
    var el = document.querySelector(".jes-typed");
    if (!el || window.matchMedia("(prefers-reduced-motion: reduce)").matches) return;
    var items = el.getAttribute("data-items").split("|"), i = 0, j = 0, deleting = false;
    function tick() {
      var word = items[i];
      j += deleting ? -1 : 1;
      el.textContent = word.slice(0, j);
      var wait = deleting ? 40 : 90;
      if (!deleting && j === word.length) { deleting = true; wait = Math.max(1600, word.length * 45); }
      else if (deleting && j === 0) { deleting = false; i = (i + 1) % items.length; wait = 400; }
      setTimeout(tick, wait);
    }
    el.textContent = "";
    setTimeout(tick, 600);
  })();
</script>
</section>

<div class="jes-layout">
<style>
  .jes-layout { display: flex; gap: 2.5rem; align-items: flex-start; }
  .jes-sidebar { flex: 0 0 220px; position: sticky; top: 90px; }
  .jes-main { flex: 1 1 auto; min-width: 0; }
  .jes-photo { width: 180px; height: 180px; border-radius: 50%; object-fit: cover; display: block; margin-bottom: 1rem; border: 4px solid var(--global-divider-color); }
  .jes-name { font-size: 1.35rem; font-weight: 600; margin: 0 0 0.35rem; color: var(--global-text-color); }
  .jes-bio { font-size: 0.9rem; color: var(--global-text-color-light); margin: 0 0 1rem; line-height: 1.4; }
  .jes-links { list-style: none; padding: 0; margin: 0; }
  .jes-links li { display: flex; align-items: center; gap: 0.6rem; margin: 0.45rem 0; font-size: 0.9rem; color: var(--global-text-color); }
  .jes-links i { width: 1.1rem; text-align: center; font-size: 1rem; color: var(--global-text-color-light); }
  .jes-links a { color: var(--global-text-color); text-decoration: none; }
  .jes-links a:hover { color: var(--global-theme-color); }
  .jes-main h2 { margin-top: 2rem; }
  .jes-main > .jes-bio-text p:first-child { margin-top: 0; }
  @media (max-width: 767px) {
    .jes-layout { flex-direction: column; align-items: stretch; gap: 1.5rem; }
    .jes-main { width: 100%; }
    .jes-sidebar { position: static; flex: none; width: 100%; text-align: center; }
    .jes-photo { margin: 0 auto 1rem; }
    .jes-links { display: flex; flex-wrap: wrap; justify-content: center; gap: 0.25rem 1rem; }
    .jes-links li { margin: 0.2rem 0; }
  }
</style>

<aside class="jes-sidebar">
  <img class="jes-photo" src="{{ page.sidebar.image | prepend: '/assets/img/' | relative_url }}" alt="{{ page.sidebar.name }}">
  <p class="jes-name">{{ page.sidebar.name }}</p>
  <p class="jes-bio">{{ page.sidebar.bio }}</p>
  <ul class="jes-links">
    {% for item in page.sidebar.items %}
    <li>
      <i class="{{ item.icon }}"{% if item.color %} style="color: {{ item.color }}"{% endif %} aria-hidden="true"></i>
      {% if item.url %}{% if item.url contains '://' or item.url contains 'mailto:' %}{% assign href = item.url %}{% else %}{% assign href = item.url | relative_url %}{% endif %}<a href="{{ href }}"{% unless item.url contains 'mailto:' %} target="_blank" rel="noopener"{% endunless %}>{{ item.text }}</a>{% else %}<span>{{ item.text }}</span>{% endif %}
    </li>
    {% endfor %}
  </ul>
</aside>

<div class="jes-main">
  <div class="jes-bio-text">{{ bio | markdownify }}</div>

  <h2><a href="{{ '/news/' | relative_url }}" style="color: inherit">news</a></h2>
  {% include news.liquid limit=true %}

  <h2><a href="{{ '/blog/' | relative_url }}" style="color: inherit">latest posts</a></h2>
  {% include latest_posts.liquid %}

  <h2><a href="{{ '/publications/' | relative_url }}" style="color: inherit">selected publications</a></h2>
  {% include selected_papers.liquid %}
</div>
</div>
