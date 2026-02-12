---
layout: home
title: ホーム
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css' | relative_url }}">

<!-- ヒーローセクション -->
<div class="hero">
  <h1>サブスリーへのラン日記</h1>
  <p>陸上未経験アラフォー市民ランナーのラン日記へようこそ！</p>
</div>

<!-- 注目記事 -->
<div class="featured-post">
  <img src="https://via.placeholder.com/600x400/667eea/ffffff?text=Featured+Post" alt="Featured" class="featured-post-image">
  <div class="featured-post-content">
    <div>
      <span class="post-category">注目</span>
    </div>
    <h2 class="featured-post-title">フルマラソンでサブスリー達成への道</h2>
    <p class="featured-post-excerpt">このブログでは、フルマラソンでサブスリー（3時間切り）を目指す日々のトレーニング、シューズレビュー、ランニングに関する研究や知見を共有しています。</p>
    <a href="{{ '/about.md' | relative_url }}" style="color: #667eea; font-weight: 600;">もっと読む →</a>
  </div>
</div>

<!-- 主なコンテンツ -->
<h2 class="section-title">📝 主なコンテンツ</h2>

<div class="post-grid">
  <a href="#" class="post-card">
    <div class="post-card-image"></div>
    <div class="post-card-content">
      <span class="post-category">デイ日記</span>
      <h3 class="post-card-title">日々のトレーニング記録</h3>
      <p class="post-card-excerpt">毎日のトレーニング内容、走行距離、ペース、心拍数などを詳細に記録しています。</p>
    </div>
  </a>
  
  <a href="#" class="post-card">
    <div class="post-card-image"></div>
    <div class="post-card-content">
      <span class="post-category">シューズレビュー</span>
      <h3 class="post-card-title">ランニングシューズのレビュー</h3>
      <p class="post-card-excerpt">実際に使用したランニングシューズの詳細なレビューと評価を紹介します。</p>
    </div>
  </a>
  
  <a href="#" class="post-card">
    <div class="post-card-image"></div>
    <div class="post-card-content">
      <span class="post-category">ランニング関連研究</span>
      <h3 class="post-card-title">科学的な視点からのランニング分析</h3>
      <p class="post-card-excerpt">科学的な研究や知見を基にしたランニングの効果的なトレーニング方法を解説します。</p>
    </div>
  </a>
  
  <a href="#" class="post-card">
    <div class="post-card-image"></div>
    <div class="post-card-content">
      <span class="post-category">トレーニング方法</span>
      <h3 class="post-card-title">効果的なトレーニングテクニック</h3>
      <p class="post-card-excerpt">インターバル、ペース走、ロング走など、様々なトレーニング方法を紹介します。</p>
    </div>
  </a>
  
  <a href="#" class="post-card">
    <div class="post-card-image"></div>
    <div class="post-card-content">
      <span class="post-category">障害予防</span>
      <h3 class="post-card-title">ランニング障害の予防と対処法</h3>
      <p class="post-card-excerpt">ランニングによる怪我を予防し、長く走り続けるための知識を共有します。</p>
    </div>
  </a>
</div>

<!-- 最新記事 -->
<h2 class="section-title">🆕 最新記事</h2>

<div class="post-grid">
  {% for post in site.posts limit:6 %}
  <a href="{{ post.url | relative_url }}" class="post-card">
    <div class="post-card-image"></div>
    <div class="post-card-content">
      {% if post.categories %}
        {% for category in post.categories %}
        <span class="post-category">{{ category }}</span>
        {% endfor %}
      {% endif %}
      <h3 class="post-card-title">{{ post.title }}</h3>
      <p class="post-card-meta">{{ post.date | date: "%Y年%m月%d日" }}</p>
      {% if post.excerpt %}
      <p class="post-card-excerpt">{{ post.excerpt | strip_html | truncate: 100 }}</p>
      {% endif %}
    </div>
  </a>
  {% endfor %}
</div>
