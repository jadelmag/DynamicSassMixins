# Dynamic theming through SCSS mixin

Sass themes is a tool to add multiple themes in your project using mixins.

Sass themes includes:

- Themify is a tool to create responsive and mobile friendly sites.
- Dynamic breakpoints to your sass files.
- Multiple colors, tokens, etc..

# Theme usage

Inside a scss file

1 - Import main.scss path

2 - Apply breakpoint

    .container {
       padding: 20px;
       font-family: $font-primary;

       @include themify($themes) {
        // iconColor is declared in custom-theme (in both themes)
        background-color: themed("iconColor");
       }

       @include breakpoint-min($breakpoint-md) {
            padding: 10px
            font-family: $font-secondary;
       }
    }

# Breakpoints usage

Inside a scss file

1 - Import main.scss path

2 - Apply breakpoint

    import './main.scss';

    .container {
       padding: 20px;
       @include breakpoint-min() {
            padding: 10px
       }
    }
