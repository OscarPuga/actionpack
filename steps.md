# Requisite 02:

```shell
$ rails g scaffold TodoItem due_date:date title:string description:text completed:boolean
```

will produce a migration: db/migrate/XXXXYYYZZ_create_todo_items.rb

```ruby
class CreateTodoItems < ActiveRecord::Migration
  def change
    create_table :todo_items do |t|
      t.date :due_date
      t.string :title
      t.text :description
      t.boolean :completed

      t.timestamps null: false
    end
  end
end
```

edit line for boolean to add default value:

> t.boolean :completed, default: false

$ rake db:migrate

$ rspec -e rq02

# Requisite 03:


$ rake db:seed
$ rspec -e rq03


# Requisite 04:

run server:

```shell
$ rails s
```

or in c9: 

$ rails s -p $PORT -b $IP 

navigate to [todo_lists home page](http://localhost:3000/todo_items) or [in c9](https://saas-proyects-oscarpuga.c9.io/todo_items)

$ rspec -e rq04


# Requisite 05:

with the server running, use the new link to crete a TodoItem

$ rspec -e rq05


# Requisite 06:
