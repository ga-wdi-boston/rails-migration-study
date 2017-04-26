# Rails Migrations Study

Use your favorite search engine and the provided readings to research and
respond to the following questions.

In your responses, be sure to cite any relevant sources you consulted in your
search. We ask you to write responses in your own words in order to see how you
process what you've read. Please do not respond with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

## Required Readings

-   Ruby on Rails Guides
    -   [Active Record Basics Migrations](http://guides.rubyonrails.org/active_record_basics.html#migrations)
        (chapter 8)
    -   [Active Record Migrations](http://guides.rubyonrails.org/active_record_migrations.html)
        (chapters 1, 2.1, 2.2, 3.1, 3.3, 3.4, 3.5, 3.8, 6, 8)

## Additional Resources
-   [Active Record Migrations](http://guides.rubyonrails.org/active_record_migrations.html)
    (the entirety)

## Explain the Role of Migrations

In your own words, define migrations and explain why developers use them.

```md
<!--
A migration contains a specific set of instructions for the database that is used and created for the application it is backing. The migration contains tables that are stored and used. When a migration file is run, rails is able to both make changes to the database and automatically create a table. Without this, the application itself would be somewhat useless.
Developers use migrations to enable them to deploy to production in a more seamless, less error prone manner, rather than updating anything for deployment manually.

additional resource: http://culttt.com/2015/10/07/understanding-ruby-on-rails-migrations/
 -->
```

## Reference Documentation for Migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
<!-- create_table -->
```

What is the name of the method that creates a new column?

```md
<!-- add_column-->
```

Suppose that an application needs a table called `pets` with the columns `name`
and `breed`, both of which are strings. `name` cannot be blank and must be
unique. Write the migration would be used to create a table satisfying these
requirements.

```ruby
class CreatePets < ActiveRecord::Migration[5.0]
   def change
     create_table :pets do |t|
       t.string :name, default:"unique name"
       t.string :breed
       t.timestamps
     end
   end
 end
```

## Explain the Role of Seed Data

In your own words, explain the role of application seed data.

```md
<!-- Seed data is used for filling an empty database with default values.
This gives you more immediate full access to all classes and methods within your application, meaning you wont need to enter everything manually in the rails console in order to make the records

additional resource used: http://www.xyzpub.com/en/ruby-on-rails/3.2/seed_rb.html
-->
```

Should seed data be used for experimentation during development?

```md
<!-- Yes, it should be used. -->
```
