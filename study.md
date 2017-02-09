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
Migrations are a way to manage changes to a database... they basically tell the schema to change/update or undo a change. They're useful mostly because it gives developers flexibility when needing to make a change and letting them adapt to change when need be... and it saves developers from having to remove an entire database to create a new one... it sounds kind of like GitHub, to be honest, because there are changes you make, but you can undo them, and you manage every little step of the process and can go back to a better version of a database.
```

## Reference Documentation for Migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
create_table
```

What is the name of the method that creates a new column?

```md
add_column
```

Suppose that an application needs a table called `pets` with the columns `name`
and `breed`, both of which are strings. `name` cannot be blank and must be
unique. Write the migration would be used to create a table satisfying these
requirements.

```ruby
class CreatePets < ActiveRecord::Migration[5.0]
  def change
    create_table :pets do |p|
      p.string :name, null: false, uniqueness: true
      p.string :breed

      p.timestamps null: false
    end
  end
end
```

## Explain the Role of Seed Data

In your own words, explain the role of application seed data.

```md
Seed data is just some default data to throw into a new database so it's not empty when you're visualizing your database/making sure your migrations work.
```

Should seed data be used for experimentation during development?

```md
I think so, because you probably don't want to test with actual factual data in case something goes wrong when you're constantly reloading your database.
```

## Other sources I used

In the seed section I also looked at [this post by David Morales] (https://davidmles.com/blog/seeding-database-rails/) and [xyzpub](http://www.xyzpub.com/en/ruby-on-rails/3.2/seed_rb.html)
