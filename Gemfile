source "https://rubygems.org"

# Jekyll本体
gem "jekyll", "~> 4.3.0"

# テーマ（minimaはシンプルで使いやすい）
gem "minima", "~> 2.5"

# プラグイン
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
  gem "jekyll-seo-tag", "~> 2.8"
  gem "jekyll-paginate", "~> 1.1"
end

# Windows and JRuby does not include zoneinfo files
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1", :platforms => [:mingw, :x64_mingw, :mswin]

# Lock `http_parser.rb` gem to `v0.6.x` on JRuby builds
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]

# GitHub Pages互換性（デプロイ時に使用）
gem "github-pages", group: :jekyll_plugins
