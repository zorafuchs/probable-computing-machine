---
aliases: 
tags: 
- public
- knowledge
title: Build in Rails Authentication
date created: "2022-10-17T08:20:42"
date modified: "2022-10-31T07:42:35"
---

# Build in Rails Authentication

If you want to implement simple authentication with [[Ruby on Rails]], these methods may be helpful. Rails uses the [[bcrypt]] gem in these methods

`has_secure_password`

Documentation: https://api.rubyonrails.org/classes/ActiveModel/SecurePassword/ClassMethods.html

Usage example
```rb
require 'securerandom'

class User < ApplicationRecord
	has_secure_password
	
	validates :email, uniqueness: true, confirmation: true
	validates :username, uniqueness: true
	
	attr_accessor :email_confirmation

	def start_email_confirmation
		return unless update(email_confirmation_token: SecureRandom.alphanumeric(20))
		UserMailer.with(user: self).email_confirmation_email.deliver_later
	end

	def start_password_reset
		return unless update(password_reset_token: SecureRandom.alphanumeric(20))
		UserMailer.with(user: self).password_reset_email.deliver_later
	end
	
	def email_confirmed?
		email_confirmation_token.blank?
	end
end
```

## Needed DB Attributes

```ruby
t.string "password_digest"
t.string "email", null: false
t.string "email_confirmation_token"
t.string "password_reset_token"
t.index ["email"], name: "index_users_on_email", unique: true
```
