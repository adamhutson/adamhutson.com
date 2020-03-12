adamhutson.com blog

brew install hugo
brew upgrade hugo
hugo version

cd ~/github.com/adamhutson
hugo new site adamhutson.com
cd adamhutson.com
git init

>> browse https://themes.gohugo.io for potential themes
decide on https://themes.gohugo.io/loveit/

https://hugoloveit.com/theme-documentation-basics/

update config.toml with selected settings

cd static
mkdir images
add AdamHutson-Headshot-512x512.jpg
update config.toml with 
    [params.home.profile]
        avatarURL = "/images/AdamHutson-Headshot-512x512.jpg"

Default theme includes menu items for [Posts,Tags,Categories]
Update to [Posts,Talks,Resume]

Need way to show slideshare widget
Copy code from https://www.thepolyglotdeveloper.com/2019/01/create-custom-shortcodes-embed-content-hugo-posts-pages/
cd layouts
mkdir shortcodes
add slideshare.html
use {{< slideshare id="" >}} to reference new shortcode

Need way to have download widget
cd layouts/shortcodes
add download.html
use {{< download file="" >}} to href a downloadable file

add adamhutson.github.io as submodule to be destination of builds and ultimately hosted from (for free!)