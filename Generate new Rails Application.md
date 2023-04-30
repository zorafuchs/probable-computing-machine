---
aliases: 
tags: 
- public
- knowledge
title: Generate New Rails Application
date created: "2022-10-10T08:42:35"
date modified: "2022-11-02T01:10:42"
---

# Generate New Rails Application

I used the [Setup Guide from Renuo](https://github.com/renuo/applications-setup-guide/tree/feature/update-rails-7-initialization/ruby_on_rails) but only applied the very most important things for me personallly

```rb
rails new [project-name] --database=postgresql --skip-test
```

`--database=postgresql` Using postgresql as a database
`--skip-test` because I want to use rspec instead of the default tests

Show all the options with `rails new --help`

When you run `bin/setup` now, you will see if [[Postgresql]] is installed correctly

You don't really have to do anything below "Adjustments" of the Guide, but it may be worth a look, because of locales settings and forcing ssl

Now you can set up [[Rspec]] if you want:

You can follow the instructions. Don't forget to add `gem 'capybara'` and `gem 'selenium-webdriver'` to the Gemfile in the test group.

## Quick Go Through

- Update ruby, ruby gems, rails
- Create new rails app
- run `bin/setup`
- if rspec setup: install rspec, capybara and selenium webdriver
- add needed test

## Simplified Rspec Installation Including a System Check

Gemfile
```rb
group :development, :test do
  gem "capybara"
  gem "rspec-rails"
  gem "selenium-webdriver"
end
```

`rails generate rspec:install`

spec/rails_helper.rb
```rb
 require 'rspec/rails'
 require 'capybara/rspec'
 require 'capybara/rails'
 require 'selenium/webdriver'
 ```

```rb
   config.before(:each, type: :system) do
     driven_by :rack_test
   end

   config.before(:each, type: :system, js: true) do
     driven_by :selenium_chrome_headless
   end
```

- Write the test [`spec/system/health_spec.rb`](https://github.com/renuo/applications-setup-guide/blob/feature/update-rails-7-initialization/templates/spec/system/health_spec.rb)

- Write the controller [`app/controllers/home_controller.rb`](https://github.com/renuo/applications-setup-guide/blob/feature/update-rails-7-initialization/templates/app/controllers/home_controller.rb)

- Add `get 'home/check'` to `config/routes.rb`

- `bundle exec rspec`
