---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<style>
  .pub-intro {
    margin: 0 0 1.2rem;
    color: #555;
    font-size: 0.92em;
  }

  .pub-section {
    margin-top: 1.6rem;
  }

  .pub-section-title {
    margin: 0 0 0.75rem;
    padding-bottom: 0.35rem;
    border-bottom: 1px solid #e6e6e6;
    color: #222;
    font-size: 1.05em;
    font-weight: 700;
  }

  .pub-list {
    display: grid;
    gap: 0.85rem;
    margin: 0;
    padding: 0;
    list-style: none;
  }

  .pub-item {
    padding: 0.95rem 1rem;
    border: 1px solid #e8e8e8;
    border-left: 4px solid #2f6f73;
    border-radius: 8px;
    background: #fff;
  }

  .pub-title {
    margin: 0;
    color: #1f2933;
    font-size: 1em;
    font-weight: 700;
    line-height: 1.35;
  }

  .pub-authors,
  .pub-meta {
    margin: 0.28rem 0 0;
    color: #4b5563;
    font-size: 0.9em;
    line-height: 1.45;
  }

  .pub-authors strong {
    color: #111;
    font-weight: 700;
    text-decoration: underline;
    text-decoration-thickness: 1px;
    text-underline-offset: 2px;
  }

  .pub-venue {
    color: #1f2933;
    font-style: italic;
    font-weight: 600;
  }

  .pub-tags {
    display: inline-flex;
    flex-wrap: wrap;
    gap: 0.32rem;
    margin-left: 0.35rem;
    vertical-align: 0.05rem;
  }

  .pub-tag {
    display: inline-block;
    padding: 0.1rem 0.38rem;
    border: 1px solid #d7e6e6;
    border-radius: 6px;
    color: #2f6f73;
    background: #f6fbfb;
    font-size: 0.78em;
    font-style: normal;
    font-weight: 700;
    line-height: 1.2;
  }

  .pub-links {
    display: flex;
    flex-wrap: wrap;
    gap: 0.45rem;
    margin-top: 0.55rem;
  }

  .archive .pub-link {
    display: inline-block;
    padding: 0.18rem 0.55rem;
    border: 1px solid #cfd8dc;
    border-radius: 6px;
    color: #254a52;
    background: #fafafa;
    font-size: 0.82em;
    font-weight: 700;
    line-height: 1.35;
    text-decoration: none;
  }

  .archive .pub-link:hover {
    border-color: #2f6f73;
    color: #183b3f;
    background: #f1f8f8;
    text-decoration: none;
  }

  @media (max-width: 640px) {
    .pub-item {
      padding: 0.85rem;
    }

    .pub-tags {
      display: flex;
      margin: 0.35rem 0 0;
    }
  }
</style>

<p class="pub-intro">
  {{ site.data.publications.intro }}
</p>

{% for section in site.data.publications.sections %}
<section class="pub-section" aria-labelledby="section-{{ forloop.index }}">
  <h2 id="section-{{ forloop.index }}" class="pub-section-title">{{ section.title }}</h2>

  <ul class="pub-list">
    {% for paper in section.items %}
    <li class="pub-item">
      <p class="pub-title">{{ paper.title }}</p>
      <p class="pub-authors">{{ paper.authors_html }}</p>
      <p class="pub-meta">
        <span class="pub-venue">{{ paper.venue }}</span>
        {% if paper.tags and paper.tags.size > 0 %}
        <span class="pub-tags">
          {% for tag in paper.tags %}
          <span class="pub-tag">{{ tag }}</span>
          {% endfor %}
        </span>
        {% endif %}
      </p>

      {% if paper.paper or paper.code or paper.project or paper.bibtex %}
      <div class="pub-links">
        {% if paper.paper %}<a class="pub-link" href="{{ paper.paper }}">Paper</a>{% endif %}
        {% if paper.code %}<a class="pub-link" href="{{ paper.code }}">Code</a>{% endif %}
        {% if paper.project %}<a class="pub-link" href="{{ paper.project }}">Project</a>{% endif %}
        {% if paper.bibtex %}<a class="pub-link" href="{{ paper.bibtex }}">BibTeX</a>{% endif %}
      </div>
      {% endif %}
    </li>
    {% endfor %}
  </ul>
</section>
{% endfor %}
