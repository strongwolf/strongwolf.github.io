---
layout: archive
title: "Gallery"
permalink: /gallery/
author_profile: true
---

<style>
:root {
    --gallery-ink: #22302d;
    --gallery-muted: #65716d;
    --gallery-paper: #ffffff;
    --gallery-soft: #f4f8f6;
    --gallery-line: #bfd7cf;
    --gallery-accent: #2f8f74;
    --gallery-warm: #d35b4a;
    --gallery-shadow: 0 18px 42px rgba(31, 52, 47, 0.14);
}

.gallery-intro {
    max-width: 760px;
    margin: 0 auto 1.8rem;
    padding: 1.25rem 0.25rem 0.4rem;
    color: var(--gallery-muted);
    font-size: 1.02em;
    line-height: 1.75;
}

.gallery-intro p {
    margin: 0;
}

.gallery-categories {
    max-width: 1040px;
    margin: 0 auto;
    padding: 0.7rem 0 2.5rem;
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
}

.gallery-category {
    display: grid;
    grid-template-columns: 160px minmax(0, 1fr);
    gap: 1.25rem;
    align-items: start;
}

.gallery-category-title {
    position: sticky;
    top: 1rem;
    z-index: 2;
    width: fit-content;
    min-width: max-content;
    margin: 0;
    padding: 0.35rem 0.9rem;
    color: var(--gallery-ink);
    font-size: 1.15em;
    font-weight: 800;
    line-height: 1;
    white-space: nowrap;
    background: var(--gallery-paper);
    border: 1px solid rgba(47, 143, 116, 0.20);
    border-radius: 999px;
    box-shadow: 0 8px 20px rgba(31, 52, 47, 0.08);
}

.gallery-category-title::before {
    content: '';
    display: inline-block;
    width: 0.55rem;
    height: 0.55rem;
    margin-right: 0.45rem;
    border-radius: 50%;
    background: var(--gallery-warm);
    vertical-align: 0.08rem;
}

.gallery-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1rem;
    align-items: start;
    grid-auto-flow: dense;
    grid-auto-rows: 8px;
}

.gallery-item {
    position: relative;
    margin: 0;
    overflow: hidden;
    background: var(--gallery-paper);
    border: 1px solid rgba(47, 143, 116, 0.16);
    border-radius: 8px;
    box-shadow: 0 10px 28px rgba(31, 52, 47, 0.10);
    transition: transform 180ms ease, box-shadow 180ms ease, border-color 180ms ease;
}

.gallery-item:hover {
    transform: translateY(-4px);
    border-color: rgba(47, 143, 116, 0.34);
    box-shadow: var(--gallery-shadow);
}

.gallery-item a {
    display: block;
    background: var(--gallery-soft);
}

.gallery-item img {
    display: block;
    width: 100%;
    height: auto;
    object-fit: contain;
    transition: transform 300ms ease, filter 300ms ease;
}

.gallery-item:hover img {
    transform: scale(1.02);
    filter: saturate(1.04) contrast(1.02);
}

.gallery-item figcaption {
    position: absolute;
    right: 0;
    bottom: 0;
    left: 0;
    margin: 0;
    padding: 2.7rem 0.85rem 0.75rem;
    color: rgba(255, 255, 255, 0.84);
    font-size: 0.84em;
    line-height: 1.55;
    text-align: left;
    background: linear-gradient(180deg, transparent, rgba(9, 22, 19, 0.76));
    pointer-events: none;
}

.gallery-item figcaption::first-line {
    color: #fff;
    font-weight: 700;
}

@media screen and (max-width: 768px) {
    .gallery-intro {
        margin-bottom: 1rem;
        padding-top: 0.8rem;
        font-size: 0.96em;
    }

    .gallery-categories {
        padding-bottom: 1.5rem;
        gap: 1.75rem;
    }

    .gallery-category {
        grid-template-columns: 1fr;
        gap: 0.85rem;
    }

    .gallery-category-title {
        position: relative;
        top: auto;
        margin-right: auto;
        padding: 0.35rem 0.7rem;
        font-size: 0.95em;
    }

    .gallery-item figcaption {
        padding: 2.2rem 0.75rem 0.65rem;
        font-size: 0.78em;
    }
}

@media screen and (max-width: 560px) {
    .gallery-grid {
        grid-template-columns: 1fr;
        grid-auto-rows: auto;
    }

    .gallery-item {
        grid-row: auto !important;
    }
}

@media (prefers-reduced-motion: reduce) {
    .gallery-item,
    .gallery-item img {
        transition: none;
    }

    .gallery-item:hover {
        transform: none;
    }

    .gallery-item:hover img {
        transform: none;
    }
}
</style>


<link href="https://fonts.font.im/css2?family=Ma+Shan+Zheng&display=swap" rel="stylesheet">

<div class="gallery-intro">
  <p style="font-family: 'Ma Shan Zheng', cursive; font-size: 2.5rem;">当时只道是寻常.</p>
</div>

<div class="gallery-categories">
  {% for section in site.data.gallery.sections %}
  <section class="gallery-category">
    <h2 class="gallery-category-title">{{ section.title }}</h2>
    <div class="gallery-grid">
      {% for item in section.items %}
      <figure class="gallery-item">
        <a href="/images/gallery/{{ item.file }}">
          <img src="/images/gallery/{{ item.file }}" alt="{{ item.alt }}" loading="lazy">
        </a>
        <figcaption>{{ item.caption }}</figcaption>
      </figure>
      {% endfor %}
    </div>
  </section>
  {% endfor %}
</div>

<script>
(function () {
    function resizeGridItem(item) {
        const grid = item.closest('.gallery-grid');
        if (!grid) return;

        const style = window.getComputedStyle(grid);
        const rowHeight = parseFloat(style.getPropertyValue('grid-auto-rows'));
        const rowGap = parseFloat(style.getPropertyValue('gap'));

        if (!rowHeight || window.innerWidth <= 560) {
            item.style.gridRowEnd = 'auto';
            return;
        }

        item.style.gridRowEnd = 'auto';

        requestAnimationFrame(function () {
            const itemHeight = item.getBoundingClientRect().height;
            const rowSpan = Math.ceil((itemHeight + rowGap) / (rowHeight + rowGap));
            item.style.gridRowEnd = 'span ' + rowSpan;
        });
    }

    function resizeAllGridItems() {
        document.querySelectorAll('.gallery-grid .gallery-item').forEach(resizeGridItem);
    }

    function bindImage(img) {
        const item = img.closest('.gallery-item');
        if (!item) return;

        if (img.complete) {
            resizeGridItem(item);
        } else {
            img.addEventListener('load', function () {
                resizeGridItem(item);
            }, { once: true });

            img.addEventListener('error', function () {
                resizeGridItem(item);
            }, { once: true });
        }
    }

    document.querySelectorAll('.gallery-grid .gallery-item img').forEach(bindImage);
    window.addEventListener('load', resizeAllGridItems);

    let resizeTimer;
    window.addEventListener('resize', function () {
        clearTimeout(resizeTimer);
        resizeTimer = setTimeout(resizeAllGridItems, 100);
    });
})();
</script>
