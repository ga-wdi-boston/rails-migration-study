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
Migrations allow us to change a database in accordance with pre-existing information form another database. We can take the rows/columns/info that make up one database and migrate them into another to have more versatility with how we use our data.
```

## Reference Documentation for Migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
bin/rails generate migration createtable
```

What is the name of the method that creates a new column?

```md
bin/rails generate migration AddColumnToTable
```

Suppose that an application needs a table called `pets` with the columns `name`
and `breed`, both of which are strings. `name` cannot be blank and must be
unique. Write the migration would be used to create a table satisfying these
requirements.

```ruby
create_table :pets do | |
  t.string :name, null, false
  t.string :breed
```

## Explain the Role of Seed Data

In your own words, explain the role of application seed data.

```md
Seed data is the initial data  found in the database upon its creation
```

Should seed data be used for experimentation during development?

```md
Yes, seed data is like example data.
```
