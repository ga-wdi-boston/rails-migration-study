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
<!-- migrations are useful to update databases structure as we write our program.  -->
```

## Reference Documentation for Migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
<!-- According to the reading a table can be created using generate migration CreateXxx (attributes and their types) but I found that I can also use the command rails generate model (name of table in singular) (attributes and their type). Which one is the preferred one and in what situations? -->
```

What is the name of the method that creates a new column?

```md
<!-- Add  -->
```

Suppose that an application needs a table called `pets` with the columns `name`
and `breed`, both of which are strings. `name` cannot be blank and must be
unique. Write the migration would be used to create a table satisfying these
requirements.

```ruby
generate model pet name:string  breed:string

# then update migration file with

change_column_null :pets, :name, default: true
```

## Explain the Role of Seed Data

In your own words, explain the role of application seed data.

```md
<!-- This is an included method in rails which adds initial data to the database created-->
```

Should seed data be used for experimentation during development?

```md
<!-- I think it is helpful to get the app functional and to test its functionality but once itnis, I will use a different file to store the app data.  -->
```
