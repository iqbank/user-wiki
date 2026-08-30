# IQBank User Wiki

This repository contains the IQBank user documentation site for students and instructors. 

It is published as a Github Page static site and built with Jekyll using the [Just the Docs](https://just-the-docs.com/) theme.

## Repository Structure

- [index.md](index.md): Documentation home page
- **Content folders**: Markdown pages for the website’s content sections. This includes:
    - [getting-started](getting-started)
    - [account-management](account-management)
    - [using-iqbank](using-iqbank)
    - [instructor-guide](instructor-guide)
    - [contact](contact)
    - [faq](faq)
- [assets](assets): Folder containing static images. Paths are named based on which website section the image would belong to 
- [_sass]( _sass ): Contains several `.scss` file defining custom theme styling overrides.
- [_config.yml](_config.yml): Jekyll configuration and theme settings
- [Gemfile.txt](Gemfile.txt): Txt file containing content used to create a Gemfile (used to run website locally)

## How to compile site locally

Here are the instructions to run the site locally, to test any changes before deployment:

**Mac-OS**

1. Install Ruby (version needs to be `>= 3.0`). Normally, the Ruby that comes with the OS is not sufficient.
```
brew install ruby
```

2. Put the Homebrew installed Ruby in your PATH. Run this command in a terminal session (or add it to shell configuration file like `.zshrc`)

```
export PATH="/opt/homebrew/opt/ruby/bin:$PATH"
```

3. Clone this repository. Locate the `Gemfile.txt` file. Make a file called `Gemfile` with the contents located in the template. 

4. In the repository root directory, with Ruby configured in your PATH, run:

```
bundle install
bundle exec jekyll serve
```

The website should now be running locally at `http://127.0.0.1:4000`

Note: Sometimes when you change files in `_sass` or need to clear stale website cache, try running `bundle exec jekyll clean` before the serve command.

## Additional Development Notes

**Inserting new pictures into repo**

- If you need to insert a new picture into the `assets` folder, it is recommended to try and compress/optimize the image (to avoid the repository size from bloating). 

    - On MacOS, ImageOptim is a good tool to use. For Windows, perhaps FileOptimizer could be a good fit. 