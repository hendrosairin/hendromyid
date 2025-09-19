---
layout: default
title: Home
---

<section class="hero">
    <div class="hero-content">
        <h1>Selamat Datang di Perjalanan Hidup Hendro</h1>
        <p>Berbagi cerita, tips, petualangan travel, dan kuliner nusantara</p>
        <a href="{{ '/about/' | relative_url }}" class="cta-button">Tentang Saya</a>
    </div>
</section>

<section class="featured-posts">
    <h2>Artikel Terbaru</h2>
    <div class="posts-grid">
        {% for post in site.posts limit:6 %}
        <article class="post-card">
            {% if post.featured_image %}
            <div class="post-image">
                <img src="{{ post.featured_image | relative_url }}" alt="{{ post.title }}">
            </div>
            {% endif %}
            <div class="post-content">
                <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
                <p>{{ post.excerpt | strip_html | truncate: 120 }}</p>
                <div class="post-meta">
                    <time>{{ post.date | date: "%d %B %Y" }}</time>
                    <span class="category">{{ post.categories.first }}</span>
                </div>
            </div>
        </article>
        {% endfor %}
    </div>
</section>

<section class="categories">
    <h2>Kategori</h2>
    <div class="category-grid">
        <a href="/category/travel/" class="category-card">
            <h3>🌍 Travel</h3>
            <p>Petualangan dan destinasi menarik</p>
        </a>
        <a href="/category/kuliner/" class="category-card">
            <h3>🍜 Kuliner</h3>
            <p>Cita rasa nusantara dan dunia</p>
        </a>
        <a href="/category/tips/" class="category-card">
            <h3>💡 Tips & Trik</h3>
            <p>Panduan praktis kehidupan</p>
        </a>
        <a href="/category/personal/" class="category-card">
            <h3>📖 Personal</h3>
            <p>Cerita dan refleksi hidup</p>
        </a>
    </div>
</section>
