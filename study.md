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
Migrations are a way to change your database schema.  As you develop an application,
you made need to add new columns to tables or add new tables themselves, or add
relations between tables.  Migrations allow you to apply these changes incrementally
as you continue development.  It also allows for rollback if you don't like the change.
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
class CreatePets < ActiveRecord::Migration
  def change
    create_table :pets do |t|
      t.string :name, null: false,  unique: true
    end
end
```

## Explain the Role of Seed Data

In your own words, explain the role of application seed data.

```md
Seed data is data that initializes the database. It's primarily used for development
and testing - to set up a known environment.  But it could be used to load
the database for any reason.
```

Should seed data be used for experimentation during development?

```md
Yes.
```
