# Rails6 * Tailwind CSS

## 1 gem

```
gem 'tailwindcss-rails'

$ bundle install

$ bundle exec rails taildwindcss:install
```

## 2 app/javascript/css/tailwindcss.css

`app/javascript/css/tailwindcss.css`ファイルを新規作成し、以下のようにする

```
@import "tailwindcss/base";
@import "tailwindcss/components";
@import "tailwindcss/utilities";
```

## 3 app/javascript/packs/application.js

`app/javascript/packs/application.js`ファイルに以下の記述を追記する

```
import "../css/tailwindcss.css";
mport "stylesheets/application"
```

## 4 app/views/layouts/application

`app/views/layouts/application`ファイル内のstylesheetをlinkから`pack`に変更する

```
<%= stylesheet_pack_tag 'application', media: 'all', 'data-turbolinks-track': 'reload' %>
```
