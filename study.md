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
Migrations allow the developer to evolve a database schema over time using Ruby instead of making modifications in SQL. Each migration, in essence, creates a new version of the database with updated features including the addition or removal of columns, entries, and tables. Each migration also updates your schema.rb file to reflect the changes of the latest migration. Developers use migration because it is an easy and convenient way to keep your database and associated files flexible and adaptable over time.
```

## Reference Documentation for Migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
create_table
```

What is the name of the method that creates a new column?

```md
change_table can do it
or
add_column
```

Suppose that an application needs a table called `pets` with the columns `name`
and `breed`, both of which are strings. `name` cannot be blank and must be
unique. Write the migration would be used to create a table satisfying these
requirements.

```ruby
class CreatePets < ActiveRecord::Migration[5.0]
  validates :name,
            presence: true,
            uniqueness: true
  def change
    create_table :pets do |t|
      t.string :breed
      t.string :name
    end
  end
end
```

## Explain the Role of Seed Data

In your own words, explain the role of application seed data.

```md
The role of application seed data is to allow the ability to add initial data after the database is created.
```

Should seed data be used for experimentation during development?

```md
Yes because it makes the development process much easier as during testing the developer will not have to manually enter initial data to a database before he/she runs tests on the application.
```
