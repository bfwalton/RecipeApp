source "https://rubygems.org"

# The versions GitHub Pages' "legacy" build actually renders with, pinned
# directly instead of through the github-pages wrapper gem. The wrapper can't
# be used locally: it pins liquid = 4.0.3, whose Liquid::Variable#taint_check
# calls String#tainted?, removed from Ruby in 3.2. Nothing newer helps either
# -- github-pages 232 pulls commonmarker, which caps Ruby < 4.0.
#
# Trade-off: version bumps on GitHub's side no longer arrive automatically.
# Check them against https://pages.github.com/versions/ when it matters.
gem "jekyll", "3.9.5"
gem "jekyll-sass-converter", "1.5.2"  # libsass, as the legacy build uses
gem "kramdown", "2.3.2"
gem "kramdown-parser-gfm", "1.1.0"
gem "jekyll-sitemap", "1.4.0"
gem "webrick"                         # unbundled from Ruby in 3.0

# Jekyll 3.9 still expects these in the standard library. They were unbundled
# in Ruby 3.4/4.0, so a local build needs them named explicitly. GitHub Pages
# runs its own Ruby and ignores this file.
gem "csv"
gem "base64"
gem "bigdecimal"
gem "logger"
gem "ostruct"
