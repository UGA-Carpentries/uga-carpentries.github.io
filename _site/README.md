# Carpentries@UGA hub page

This is the web page for the Carpentries@UGA, to coordinate all Carpentries-related work at the Universitry of Georgia. The website theme is based on the [Bulme Clean theme](https://github.com/chrisrhymes/bulma-clean-theme/) from [C. S. Rhymes](https://github.com/chrisrhymes/). This site is currently under development.

If you want to be involved in planning/running Carpentries workshops at UGA, please join the Carpentries@UGA conversation on Slack at https://join.slack.com/t/carpentriesuga/signup. (Note: If you use a @uga.edu email address, you should be able to join automatically.)

The compiled version of this page is at [https://uga-carpentries.github.io](https://uga-carpentries.github.io)

# Guide to modifying the web page

The full guide to using the Bulma Clean theme is at [the project repo]("https://github.com/chrisrhymes/bulma-clean-theme"). This is the short version for most accessed stuff

## Navbar
The navbar at the top of the site is controlled by `data/navigation.yml`. It uses the following format, including support for dropdown menus:
```
- name: Page 1
  link: /page-1/
- name: Blog
  link: /blog/
  dropdown: 
    - name: Page 2
      link: /page-2/
```

## Footer menu
The footer is formatted like the navbar and is in `data/footer.yml`. Not sure if it accepts dropdowns or not.

## CSS
Custom CSS values can be done in `assets/css/app.scss`. Global variables need to be included before `@import "main";`, while normal CSS code can be put after. (Note that most normal elements need `.content` in front of them to override the default values):
```
// Change header colors.
.content h1 {
    color: red;
}

// Does not work.
h1 {
    color: blue;
}
```

