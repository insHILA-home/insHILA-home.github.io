# Repository of CFT HILA project's home page
This repository hosts [Jekyll](https://jekyllrb.com/docs/)-based 
home page of CFT framework HILA. 
The home page will be rendered as [Github page](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages) 
by utilizing the automation provided by Github [branch deployment](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

The template [Start Bootstrap - Clean Blog Jekyll](https://github.com/StartBootstrap/startbootstrap-clean-blog-jekyll) is chosen as basis of working. This template is built upon 
[Bootstrap](https://getbootstrap.com/), which offer convenient [CSS/Sass](https://en.wikipedia.org/wiki/CSS) style sheet design.

A pre-rendered test site can be found at [here](https://inshila-home.github.io/). 

## Structure of site source tree and User guide

1. Create the following pages if they do not exist already (or change the extension of existing markdown files from `.md` to `.html`):

   * `index.html` - set to `layout: home`
   * `about.html` - set to `layout: page`
   * `contact.html` - set to `layout: page`
   * `posts/index.html` - set to `layout: page` (you will also need to create a `posts` directory)

2. Configure the `index.html` front matter. Example:

    ```markdown
    ---
    layout: home
    background: '/PATH_TO_IMAGE'
    ---
    ```

3. Configure the `about.html`, `contact.html`, and `posts/index.html` front matter. Example:

    ```markdown
    ---
    layout: page
    title: Page Title
    description: This is the page description.
    background: '/PATH_TO_IMAGE'
    ---
    ```

4. For each post in the `_posts` directory, update the front matter. Example:

    ```markdown
    ---
    layout: post
    title: "Post Title"
    subtitle: "This is the post subtitle."
    date: YYYY-MM-DD HH:MM:SS
    background: '/PATH_TO_IMAGE'
    ---
    ```

    For reference, look at the [demo repository](https://github.com/StartBootstrap/startbootstrap-clean-blog-jekyll) to see how the files are set up.

5. Add the form to the `contact.html` page. Add the following code to your `contact.html` page:

    ```html
    <form name="sentMessage" id="contactForm" novalidate>
      <div class="control-group">
        <div class="form-group floating-label-form-group controls">
          <label>Name</label>
          <input type="text" class="form-control" placeholder="Name" id="name" required data-validation-required-message="Please enter your name.">
          <p class="help-block text-danger"></p>
        </div>
      </div>
      <div class="control-group">
        <div class="form-group floating-label-form-group controls">
          <label>Email Address</label>
          <input type="email" class="form-control" placeholder="Email Address" id="email" required data-validation-required-message="Please enter your email address.">
          <p class="help-block text-danger"></p>
        </div>
      </div>
      <div class="control-group">
        <div class="form-group col-xs-12 floating-label-form-group controls">
          <label>Phone Number</label>
          <input type="tel" class="form-control" placeholder="Phone Number" id="phone" required data-validation-required-message="Please enter your phone number.">
          <p class="help-block text-danger"></p>
        </div>
      </div>
      <div class="control-group">
        <div class="form-group floating-label-form-group controls">
          <label>Message</label>
          <textarea rows="5" class="form-control" placeholder="Message" id="message" required data-validation-required-message="Please enter a message."></textarea>
          <p class="help-block text-danger"></p>
        </div>
      </div>
      <br>
      <div id="success"></div>
      <div class="form-group">
        <button type="submit" class="btn btn-primary" id="sendMessageButton">Send</button>
      </div>
    </form>
    ```

    Make sure you have the `email` setting in your `_config.yml` file set to a working email address! Once this is set, fill out the form and then check your email, verify the email address using the link sent to you by Formspree, and then the form will be working!

### Default _config.yml keywords

Update the following configuration settings in `_config.yml` file to control the information flow:

    * `baseurl`
    * `url`
    * `title`
    * `email` (after setting this setting to a working email address, fill out the form on the contact page and send it - then check your email and verify the address and the form will send you messages when used)
    * `description`
    * `author`
    * `twitter_username` (Optional)
    * `facebook_username` (Optional)
    * `github_username` (Optional)
    * `linkedin_username` (Optional)
    * `instagram_username` (Optional)

## Copyright and License

Copyright 2013-2021 Start Bootstrap LLC. Code released under the [MIT](https://github.com/StartBootstrap/startbootstrap-clean-blog-jekyll/blob/master/LICENSE) license.
