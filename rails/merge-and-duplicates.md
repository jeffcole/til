Merging a `has_many` association in a scope can cause duplicates to be returned.
```ruby
class Album
  def self.with_favorited_photos
    joins(:photos).
      merge(Photo.favorited)
  end
end
```

 `Album.with_favorited_photos` will return an album for every favorited photo, rather than one album in each case where a photo has been favorited.

 The solution is to use `.distinct`.

```ruby
joins(:photos).
  merge(Photo.favorited).
  distinct
```

[2015-10-14]
