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

A migration is a method used to update and create schemas for a databse. Developers use migrations as opposed to manually changing and creating each schema to take advantage of version control and automate redundant tasks.
```

## Reference Documentation for Migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
<!-- your response here -->
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

bin/rails generate migration CreatePets name:string null: false,  breed:string

```

## Explain the Role of Seed Data

In your own words, explain the role of application seed data.

```md
Seed data populates newly created databases with pseudo data so that developers can begin programming and/or testing without the need of having real data.

```

Should seed data be used for experimentation during development?

```md

Seeds are meant for testing. Its good to test with seeds to make sure the entity relations are acting as they should.
```
