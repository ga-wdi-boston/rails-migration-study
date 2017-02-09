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
A migration is a way to modify one's database. I believe they are useful in the same way github can do a pull request, on can do a migration of their new data to the master database. Also, one can go back to how it was before a certain data was migrated.
```

## Reference Documentation for Migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
create_table :name_of_table
```

What is the name of the method that creates a new column?

```md
add_column :name_of_table, :name_of_column, :type_of_data
```

Suppose that an application needs a table called `pets` with the columns `name`
and `breed`, both of which are strings. `name` cannot be blank and must be
unique. Write the migration would be used to create a table satisfying these
requirements.

```ruby
class CreatePets < ActiveRecord::Migration[5.0]
    def change
      create_table :pets do |t|
        t.string :name, null: false, unique: true
        t.string :breed
      end
    end
 end
 ```

## Explain the Role of Seed Data

In your own words, explain the role of application seed data.

```md
It's the data that gets added to a database at first. It just non important data used as a filling to take out later.
```

Should seed data be used for experimentation during development?

```md
Yes, because it will allow someone to see if their code works. Kind of like entering 'lorem' into a div to see the effects of the css.```
