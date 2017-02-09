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
Migrations is a way to change the database schema so that a developer does not have to write SQL by hand.
```

## Reference Documentation for Migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
The method is called: create_table
```

What is the name of the method that creates a new column?

```md
The method to create a new column is: add_column
```

Suppose that an application needs a table called `pets` with the columns `name`
and `breed`, both of which are strings. `name` cannot be blank and must be
unique. Write the migration would be used to create a table satisfying these
requirements.

```ruby
class CreatePets < ActiveRecord::Migration
  def up
    create_table :pets do |t|
      t.text :name, :null => false, :uniqueness => true
      t.text :breed

      t.timestamps, :null => false
    end
  end
end
```

## Explain the Role of Seed Data

In your own words, explain the role of application seed data.

```md
Application seed data makes it easy and fast to add initial data once a database has been established.
```

Should seed data be used for experimentation during development?

```md
Yes.  One of the benefits of using seed data is that a person can use it in test environments (where the database usually has to be roloaded frequently).
```
