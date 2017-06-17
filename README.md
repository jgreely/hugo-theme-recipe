# Recipe Archive Theme

This is pretty minimal Hugo theme for an online cookbook, primarily
designed around converting MasterCook export format (MX2) to
TOML+Markdown. It shows off two new features added in 0.22: nested
sections and `$.Site.GetPage "page"` support.

## How-To

1. Copy `example/*` to your `content` directory and customize the
   contents.

2. Use my [MasterCook scripts] to convert MX2 recipe files to Hugo
   content files, and store them in one or more content sections. Or
   use your own Markdown formatting.

3. Add an `_index.md` file to the section to add a custom title to the
   Collections menu and a description to the section index page. Nested
   sections will not be detected without this.

4. (optional) To add download links in `_index.md`, use the `mx2`
   shortcode (see example in `content/mcarchive/cheesecakes`), and
   name the file `static/mx2/sectionname.mx2`.

5. (optional) To add emoji-based star ratings, add lines to the
   `[stars]` section of `data/meta.toml`, in the form 
   `"/rel/perma/link/" = N`. The default is 0, and there's
   no maximum. A negative rating prints a single red "X".

6. (optional) To add featured recipes on the home page, add lines
   to the `featured` array in `data/meta.toml`.

## Notes

* The `xml2md` script isn't in the repo yet; still cleaning up the
  output. Any format will work, but the sidebar formatting assumes
  the use of MC-compatible parameter names in the front matter. See
  the provided examples.

[MasterCook scripts]: https://github.com/jgreely/mastercook-tools
