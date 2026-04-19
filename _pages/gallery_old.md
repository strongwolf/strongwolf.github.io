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
    height: fit-content;
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
  <p style="font-family: 'Ma Shan Zheng', cursive; font-size: 1.5rem;">当时只道是寻常.</p>
</div>

<div class="gallery-categories">
  <section class="gallery-category">
    <h2 class="gallery-category-title">食物</h2>
    <div class="gallery-grid">
      <figure class="gallery-item">
        <a href="/images/gallery/3.jpeg">
          <img src="/images/gallery/3.jpeg" alt="围桌盛宴" loading="lazy">
        </a>
        <figcaption>围桌盛宴</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/4.jpeg">
          <img src="/images/gallery/4.jpeg" alt="晚餐时刻" loading="lazy">
        </a>
        <figcaption>晚餐时刻</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/8.jpeg">
          <img src="/images/gallery/8.jpeg" alt="烤肉局" loading="lazy">
        </a>
        <figcaption>烤肉局</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/17.jpeg">
          <img src="/images/gallery/17.jpeg" alt="寿司拼盘" loading="lazy">
        </a>
        <figcaption>寿司拼盘</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/30.jpeg">
          <img src="/images/gallery/30.jpeg" alt="街边小店" loading="lazy">
        </a>
        <figcaption>街边小店</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/33.jpeg">
          <img src="/images/gallery/33.jpeg" alt="夜宵时间" loading="lazy">
        </a>
        <figcaption>夜宵时间</figcaption>
      </figure>
    </div>
  </section>

  <section class="gallery-category">
    <h2 class="gallery-category-title">自然风光</h2>
    <div class="gallery-grid">
      <figure class="gallery-item">
        <a href="/images/gallery/1.jpeg">
          <img src="/images/gallery/1.jpeg" alt="云雾山峰" loading="lazy">
        </a>
        <figcaption>云雾山峰</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/6.jpeg">
          <img src="/images/gallery/6.jpeg" alt="海边云层" loading="lazy">
        </a>
        <figcaption>海边云层</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/7.jpeg">
          <img src="/images/gallery/7.jpeg" alt="海上航迹" loading="lazy">
        </a>
        <figcaption>海上航迹</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/16.jpeg">
          <img src="/images/gallery/16.jpeg" alt="峡湾之间" loading="lazy">
        </a>
        <figcaption>峡湾之间</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/23.jpeg">
          <img src="/images/gallery/23.jpeg" alt="山间远眺" loading="lazy">
        </a>
        <figcaption>山间远眺</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/32.jpeg">
          <img src="/images/gallery/32.jpeg" alt="山谷瀑流" loading="lazy">
        </a>
        <figcaption>山谷瀑流</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/35.jpeg">
          <img src="/images/gallery/35.jpeg" alt="逆光海岸" loading="lazy">
        </a>
        <figcaption>逆光海岸</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/37.jpeg">
          <img src="/images/gallery/37.jpeg" alt="雪山公路" loading="lazy">
        </a>
        <figcaption>雪山公路</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/41.jpeg">
          <img src="/images/gallery/41.jpeg" alt="海湾晨色" loading="lazy">
        </a>
        <figcaption>海湾晨色</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/44.jpeg">
          <img src="/images/gallery/44.jpeg" alt="海岸假日" loading="lazy">
        </a>
        <figcaption>海岸假日</figcaption>
      </figure>
    </div>
  </section>

  <section class="gallery-category">
    <h2 class="gallery-category-title">城市景观</h2>
    <div class="gallery-grid">
      <figure class="gallery-item">
        <a href="/images/gallery/5.jpeg">
          <img src="/images/gallery/5.jpeg" alt="城市雕像" loading="lazy">
        </a>
        <figcaption>城市雕像</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/9.jpeg">
          <img src="/images/gallery/9.jpeg" alt="旅途纪念" loading="lazy">
        </a>
        <figcaption>旅途纪念</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/10.jpeg">
          <img src="/images/gallery/10.jpeg" alt="飞行甲板" loading="lazy">
        </a>
        <figcaption>飞行甲板</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/11.jpeg">
          <img src="/images/gallery/11.jpeg" alt="晴空楼群" loading="lazy">
        </a>
        <figcaption>晴空楼群</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/12.jpeg">
          <img src="/images/gallery/12.jpeg" alt="校园一角" loading="lazy">
        </a>
        <figcaption>校园一角</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/13.jpeg">
          <img src="/images/gallery/13.jpeg" alt="赛场夜色" loading="lazy">
        </a>
        <figcaption>赛场夜色</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/14.jpeg">
          <img src="/images/gallery/14.jpeg" alt="灯影时刻" loading="lazy">
        </a>
        <figcaption>灯影时刻</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/15.jpeg">
          <img src="/images/gallery/15.jpeg" alt="夜游码头" loading="lazy">
        </a>
        <figcaption>夜游码头</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/18.jpeg">
          <img src="/images/gallery/18.jpeg" alt="港湾天际线" loading="lazy">
        </a>
        <figcaption>港湾天际线</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/19.jpeg">
          <img src="/images/gallery/19.jpeg" alt="古城夜景" loading="lazy">
        </a>
        <figcaption>古城夜景</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/20.jpeg">
          <img src="/images/gallery/20.jpeg" alt="塔影流光" loading="lazy">
        </a>
        <figcaption>塔影流光</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/21.jpeg">
          <img src="/images/gallery/21.jpeg" alt="城市地标" loading="lazy">
        </a>
        <figcaption>城市地标</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/22.jpeg">
          <img src="/images/gallery/22.jpeg" alt="烟花之夜" loading="lazy">
        </a>
        <figcaption>烟花之夜</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/24.jpeg">
          <img src="/images/gallery/24.jpeg" alt="仰望高楼" loading="lazy">
        </a>
        <figcaption>仰望高楼</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/25.jpeg">
          <img src="/images/gallery/25.jpeg" alt="维港夜色" loading="lazy">
        </a>
        <figcaption>维港夜色</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/26.jpeg">
          <img src="/images/gallery/26.jpeg" alt="建筑线条" loading="lazy">
        </a>
        <figcaption>建筑线条</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/27.jpeg">
          <img src="/images/gallery/27.jpeg" alt="城中远景" loading="lazy">
        </a>
        <figcaption>城中远景</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/28.jpeg">
          <img src="/images/gallery/28.jpeg" alt="雾中地标" loading="lazy">
        </a>
        <figcaption>雾中地标</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/29.jpeg">
          <img src="/images/gallery/29.jpeg" alt="旧楼立面" loading="lazy">
        </a>
        <figcaption>旧楼立面</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/31.jpeg">
          <img src="/images/gallery/31.jpeg" alt="尖顶教堂" loading="lazy">
        </a>
        <figcaption>尖顶教堂</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/34.jpeg">
          <img src="/images/gallery/34.jpeg" alt="夜色长廊" loading="lazy">
        </a>
        <figcaption>夜色长廊</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/36.jpeg">
          <img src="/images/gallery/36.jpeg" alt="城市天际线" loading="lazy">
        </a>
        <figcaption>城市天际线</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/38.jpeg">
          <img src="/images/gallery/38.jpeg" alt="山城夜幕" loading="lazy">
        </a>
        <figcaption>山城夜幕</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/39.jpeg">
          <img src="/images/gallery/39.jpeg" alt="节庆现场" loading="lazy">
        </a>
        <figcaption>节庆现场</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/40.jpeg">
          <img src="/images/gallery/40.jpeg" alt="梦幻城堡" loading="lazy">
        </a>
        <figcaption>梦幻城堡</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/42.jpeg">
          <img src="/images/gallery/42.jpeg" alt="雾夜高楼" loading="lazy">
        </a>
        <figcaption>雾夜高楼</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/43.jpeg">
          <img src="/images/gallery/43.jpeg" alt="江边霓虹" loading="lazy">
        </a>
        <figcaption>江边霓虹</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/45.jpeg">
          <img src="/images/gallery/45.jpeg" alt="书墙空间" loading="lazy">
        </a>
        <figcaption>书墙空间</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/46.jpeg">
          <img src="/images/gallery/46.jpeg" alt="摩天轮夜色" loading="lazy">
        </a>
        <figcaption>摩天轮夜色</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/47.jpeg">
          <img src="/images/gallery/47.jpeg" alt="霓虹乐园" loading="lazy">
        </a>
        <figcaption>霓虹乐园</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/48.jpeg">
          <img src="/images/gallery/48.jpeg" alt="黄昏楼宇" loading="lazy">
        </a>
        <figcaption>黄昏楼宇</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/49.jpeg">
          <img src="/images/gallery/49.jpeg" alt="老屋门前" loading="lazy">
        </a>
        <figcaption>老屋门前</figcaption>
      </figure>

      <figure class="gallery-item">
        <a href="/images/gallery/50.jpeg">
          <img src="/images/gallery/50.jpeg" alt="现代园区" loading="lazy">
        </a>
        <figcaption>现代园区</figcaption>
      </figure>
    </div>
  </section>
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
