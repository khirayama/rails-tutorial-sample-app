# Ruby on Rails チュートリアル：サンプルアプリケーション

これは、以下のためのサンプルアプリケーションです。
[*Ruby on Rails Tutorial*](http://railstutorial.jp/)
by [Michael Hartl](http://www.michaelhartl.com/).

## メモ

[Rubyのテンプレートエンジンをerbからslimに変更する際に変えた事](http://qiita.com/moriyaman/items/c0d60406422677bcb398)

```
gem 'slim-rails'
```

```config/application.rb
class Application < Rails::Application
  config.generators.template_engine = :slim  
end
```

```
$ gem install html2slim
$ for file in app/views/**/*.erb; do erb2slim $file ${file%erb}slim && rm $file; done
```
