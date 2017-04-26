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
Migrations are a safe and easy way to change your database schema.  A migration creates a new "version" of the database.  You add tables, columns or entries, or remove them.
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

you can also add them in a class, too, when creating a table:

create_table :products do |t|
  t.string :name
  end

  creates a table called products with a column called name
```

Suppose that an application needs a table called `pets` with the columns `name`
and `breed`, both of which are strings. `name` cannot be blank and must be
unique. Write the migration would be used to create a table satisfying these
requirements.

```ruby
create_table :pets do |t|
  t.string :name
  t.string :breed
end

```

## Explain the Role of Seed Data

In your own words, explain the role of application seed data.

```md
seed data is a quick way to add data after a database schema is created.
You have a file (db/seed.rb) filled with whatever code you need, and
after you run rails db.seed, the data you want will quickly populate your new
database.
Useful for test/dev environments.
```

Should seed data be used for experimentation during development?

```md
Yes, since, according to the documentation, the primary use-case for seed data
is when you're constantly reloading a database in test/dev
```
