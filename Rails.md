Rails Memos
===========

####Some ActiveRecord queries

	# Get the 
	@item = Item.where('index < ?', @next_item.index)
		.order('index DESC')
		.limit(1)
		.first
