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
Migrations alter the database schema over time. Migrations use RUBY which allows changes to be made independent of the database. A migration is a like a new version of the database, each migration modifies a schema by adding or removing tables etc.
```

## Reference Documentation for Migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
create_table
rails db:migrate
```

What is the name of the method that creates a new column?

```md
symbols
t.text :column
add_column
```

Suppose that an application needs a table called `pets` with the columns `name`
and `breed`, both of which are strings. `name` cannot be blank and must be
unique. Write the migration would be used to create a table satisfying these
requirements.

```ruby

# rails generate model Pet name:string breed:string

class PetsTable < ActiveRecord::Migrations[5.0]
  def change
    create_table :pets do |t|
      t.string :name :breed

      t.timestamps
    end
  end
end

```

## Explain the Role of Seed Data

In your own words, explain the role of application seed data.

```md
seeds are used to add data after the database has been created
```

Should seed data be used for experimentation during development?

```md
seed data should be used to add data AFTER a database has been created. you can add/modify existing data and using seed data can be usefule when reloading the database during development and testing.
```
