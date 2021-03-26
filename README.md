# cloud9-website

This is the website for team Cloud 9 to display our robot Clyde.

## Running the website locally

This website is built using Hugo. To run it locally you need to:

- [Install Hugo](https://gohugo.io/getting-started/installing/)
- Clone the repo
- `cd` into the folder
- Run `hugo server` in a terminal

If you have any trouble then ask Ryan.

## Editing the site

I'm going to break this down into 3 parts:

#### Editing the landing page

To edit the landing page you need to look at **/data/homepage.yml** where you can work out how each section relates to the content of the landing page. Since this data is injected into a pre-determined layout please don't write too much unless you think the layout itself needs edited to accommodate it.

#### Editing the other pages

To edit the other pages of the site you need to look at **/content/pages/<page-you-want-to-edit>**. These pages are written in markdown. If you have not used markdown before you can find out how it works [here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

#### Editing the styling

To edit the styling you either want to look at **/layouts/<part-you-want-to-edit>** to edit the html or **/assets/scss/<part-you-want-to-edit>** to edit the css. Note that both of these are broken down into components so it may not be obvious which part to edit at first.

## Support

If you have any questions then ask Ryan.
