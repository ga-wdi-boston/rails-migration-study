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
Migrations allow us to alter database schema conveniently, keeping them
independent from the database.
https://scotch.io/tutorials/understanding-migrations-in-rails
http://guides.rubyonrails.org/active_record_migrations.html
```

## Reference Documentation for Migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
create_table

http://guides.rubyonrails.org/active_record_migrations.html
```

What is the name of the method that creates a new column?

```md
t.string creates a column called name.

create_table :products do |t|
  t.string :name
end

http://guides.rubyonrails.org/active_record_migrations.html
```

Suppose that an application needs a table called `pets` with the columns `name`
and `breed`, both of which are strings. `name` cannot be blank and must be
unique. Write the migration would be used to create a table satisfying these
requirements.

```ruby

class CreatePets < ActiveRecord::Migration[5.0]
  def change
    create_table :pets do |t|
      t.string :name, :default => "something"
      t.string :breed
    end
  end
end
```

http://stackoverflow.com/questions/7098602/add-a-default-value-to-a-column-through-a-migration

http://guides.rubyonrails.org/active_record_migrations.html

## Explain the Role of Seed Data

In your own words, explain the role of application seed data.

```md
To quickly add data to database after it has been created. You store the
instructions for inserting that data in db/seeds.rb
http://guides.rubyonrails.org/active_record_migrations.html
```

Should seed data be used for experimentation during development?

```md
Yes!
```
