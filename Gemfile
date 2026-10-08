source "https://rubygems.org"

# GitHub Pages builds this site with its own pinned toolchain ("legacy" build
# type = Jekyll 3.9.x). Keeping the gem here means a local preview matches what
# actually gets published, rather than a newer Jekyll that tolerates more.
gem "github-pages", group: :jekyll_plugins
gem "webrick"

# Jekyll 3.9 still expects these in the standard library. They were unbundled
# in Ruby 3.4/4.0, so a local build needs them named explicitly. GitHub Pages
# runs its own Ruby and ignores this file.
gem "csv"
gem "base64"
gem "bigdecimal"
gem "logger"
gem "ostruct"
