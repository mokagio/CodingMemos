Rails Memos
===========

####Some ActiveRecord queries

```ruby
@item = Item.where('index < ?', @next_item.index)
	.order('index DESC')
	.limit(1)
	.first
```

####Generate model with ActiveRecord CLI

```bash
$ rails generate model Product name:string description:text
```
