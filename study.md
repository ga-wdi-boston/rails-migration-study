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
Migrations allow you to take older versions of a database and update/add things to it
without destroying the original one. So it seems to be a diferent style of version control
for databases.
```

## Reference Documentation for Migrations

In ActiveRecord Migrations, what is the name of the method the creates a new
table?

```md
create_table :name do |t|
```

What is the name of the method that creates a new column?

```md
<!-- t.<type of input> :<title of column > thats if you're doing it while declaring a new table
If doing it as a stand alone it would add_column :name of column, :type of input-->
```

Suppose that an application needs a table called `pets` with the columns `name`
and `breed`, both of which are strings. `name` cannot be blank and must be
unique. Write the migration would be used to create a table satisfying these
requirements.

```ruby
class CreatePets
  def change
    create_table :pets do |t|
      t.string :name, null: false,
      t.string :breed
```
I am not sure about keeping to colum unique. This also only seems right following the reading
and the diagrams in the reading, but I am convinced I am probably wrong.

## Explain the Role of Seed Data

In your own words, explain the role of application seed data.

```md
Seed data is the data that is migrated to the version being worked on. That way that
data remains untouched and can be called upon again without being editted.
```

Should seed data be used for experimentation during development?

```md
Nope, if its data that shouldn't be touched then seeding it allows for basically copies
of the data to go out. It can be updated but obviously not until it needs to be. 
```
