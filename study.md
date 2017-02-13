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
A migration is a way for us to change a database.  We can generate new tables or columns, and the history of these changes is stored.  To me it sounds similar to git commits, where you have a history of your changes and you can restore to a previous state if you need to.
```

## Reference Documentation for Migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md

$ bin/rails generate migration CreateX
```

What is the name of the method that creates a new column?

```md
$ bin/rails generate migration AddColumnToTable
```

Suppose that an application needs a table called `pets` with the columns `name`
and `breed`, both of which are strings. `name` cannot be blank and must be
unique. Write the migration would be used to create a table satisfying these
requirements.

```ruby
create_table :pets do |t|
  t.string :name, null: false
  t.string :breed
end
```

## Explain the Role of Seed Data

In your own words, explain the role of application seed data.

```md
Seed data is data that fills the database when it is initally launched
```

Should seed data be used for experimentation during development?

```md
Yes, because seed data can be just filler data that doesn't have any value except to demonstrate how the database works.  
```
