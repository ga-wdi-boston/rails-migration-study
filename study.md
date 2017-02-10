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
Migrations are a way for Rails developers to update a database. This allows developers to track changes over time and easily implement or rollback changes.
```

## Reference Documentation for Migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
`create_table`
```

http://guides.rubyonrails.org/active_record_migrations.html#creating-a-table

What is the name of the method that creates a new column?

```md
`add_column`
```

http://guides.rubyonrails.org/active_record_migrations.html#creating-a-standalone-migration

Suppose that an application needs a table called `pets` with the columns `name`
and `breed`, both of which are strings. `name` cannot be blank and must be
unique. Write the migration would be used to create a table satisfying these
requirements.

```ruby
class CreatePets < ActiveRecord::Migration[5.0]
  def change
    create_table :pets do |t|
      t.string :name, :null => false, uniqueness: true
      t.string :breed

      t.timestamps
    end
  end
end
```

- http://stackoverflow.com/questions/19972913/validates-presense-vs-null-false-in-rails-models-tables
- http://guides.rubyonrails.org/active_record_migrations.html#creating-a-standalone-migration

## Explain the Role of Seed Data

In your own words, explain the role of application seed data.

```md
Seed data provides a way to quickly add data after a database has already been created.
```

http://guides.rubyonrails.org/active_record_migrations.html#migrations-and-seed-data

Should seed data be used for experimentation during development?

```md
Yes. Seed data is helpful in the development or testing process when some initial data must be present to work with the application.
```

http://guides.rubyonrails.org/active_record_migrations.html#migrations-and-seed-data
