## stylesheetの変更

stylesheet を変更したい場合 develop branch で code を書いていきます。


* stylesheet を追加

```bash
+++ b/source/stylesheets/global/_footer.css.scss
@@ -0,0 +1,10 @@
+footer {
+  padding: 2em 1em;
+  border-top: 1px solid #eeeeee;
+  .copy {
+    float: left;
+    margin-bottom: 5px;
+    font-size: 85%;
+    color: #ccc;
+  }
+}
```

* stylesheet を外出しした場合は、 site.css.scss で import すれば反映されます

```bash
diff --git a/source/stylesheets/site.css.scss b/source/stylesheets/site.css.scss
index ff3718c..b684c19 100644
--- a/source/stylesheets/site.css.scss
+++ b/source/stylesheets/site.css.scss
@@ -65,3 +65,5 @@ h1 {
     -webkit-transform: scale(1);
   }
 }
+
+@import "global/footer"
```

* script/server で確認出来ます
