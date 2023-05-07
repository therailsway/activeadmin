---
redirect_from: /docs/documentation.html
---

Active Admin 是一款用于生成 Ruby on Rails 管理界面的插件。它通过高度概括总结常见商业应用程序的逻辑模式，化繁为简，使开发者只需使用很少的代码就能生成漂亮优雅的界面。

# 开始

Active Admin 以 Ruby Gem 形式发布。该 Gem 在 Ruby on Rails 应用内安装。安装的最简单方式就是在您的 Gemfile 内添加下面代码：

```ruby
# Gemfile
gem 'activeadmin'
```

如果使用 Devise 做为您的用户认证系统，需要在 Gemfile 中添加 `devise` Gem

```ruby
# Gemfile
gem 'devise'
```

更新 bundle 后，运行生成器

```bash
rails generate active_admin:install
```

生成器会创建一个用于配置默认设置的初始化文件和用于放置管理配置的 `app/admin` 文件夹。

运行数据库维护迁移，启动服务器：

```bash
$> rails db:migrate
# 如果您使用 Devise，添加默认用户
$> rails db:seed
$> rails server
```

访问 `http://localhost:3000/admin`，登录：

* __User__: admin@example.com
* __Password__: password

哇！您已经登录到您的新 Active Admin 管理系统的首页了。

注册您的第一个模型，运行：

```bash
$> rails generate active_admin:resource
        [MyModelName]
```

这将创建用于配置资源的文件 `app/admin/my_model_names.rb`，刷新您的浏览器查看新变化。

# 接下来

现在您已经拥有一个可以正常运行的 Active Admin 了，学习更多定制知识：

* [定制索引页](3-index-pages.md)
* [定制新建和编辑表单](5-forms.md)
* [定制展示页](6-show-pages.md)
* [定制资源常用方式](2-resource-customization.md)
