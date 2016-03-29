## ページの編集

基本的に develop branch で code を書いていきます。例えば、Footer を追加させたい場合は、以下のように `source/layouts/_footer.html.haml` を編集します。
また、 helpermethod を追加させたい場合は、以下の `config.rb` で method を定義します。

* https://middlemanapp.com/jp/basics/directory-structure/

* cf. https://github.com/jtf-2016/jtf-2016.github.io/pull/24

* footer page に copyright を追加させたい場合


source/layouts/_footer.html.haml

```haml
+%footer{role: "contentinfo"}
 +  .copy
 +    &copy;
 +    = copyright_years(2016)
 +    July Tech Fest Member
 +  = partial 'layouts/sns' # 追加でpage の追加も出来る
```

* helpermethod を追加させたい場合

config.rb

```ruby
+helpers do
 +  # Calculate the years for a copyright
 +  def copyright_years(start_year)
 +    end_year =  Date.today.year
 +    if start_year == end_year
 +      start_year.to_s
 +    else
 +      start_year.to_s + '-' + end_year.to_s
 +    end
 +  end
 +end
 ```

* script/server で確認出来ます
