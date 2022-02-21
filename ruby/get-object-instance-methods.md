# Get Object Instance Methods

You can quickly get the direct instance methods of an object by calling [`instance_methods`](https://ruby-doc.org/core-2.6.3/Module.html#method-i-instance_methods) on that object's class.

```rb
user.instance_of?(Person)
# => true

user.class.instance_methods(false)
# => [:speak, :walk, :sit]
```

Passing provided flag of `false` filters out methods from ancestors.
