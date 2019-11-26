# ReactJS Facebook messenger

The goal of this exercise is to learn how to style a React app using styled-components.

## To get started

### Step 1

If you haven't already set up your project, head here and follow the instructions https://github.com/leanjscom/fb-messenger/blob/master/README.md

### Step 2

```sh
 git checkout styling-in-react
```

## Exercise

### Part 1, Storybook

#### P component

Task 1. Use styled-components to move the style from the `p` tag from `src/components/Login/index` into `src/components/Form/P`.

Task 2. There should be two stories in P.stories.js:

1. The default P style
2. The "quote" style when P receives the prop `quote={true}`. The quote style is the following:

```
{
    padding-top: 10px;
    padding-left: 10px;
    border-left: 4px solid grey;
}
```

#### Button component

Task 1. Using styled-components, implement the `src/components/Form/Button` using the styles defined in that file. Then create the following stories in `src/components/Form/Button.stories.js`:

1. Default, no props required.
2. Button large when prop `large={true}`
3. Button primary when prop `primary={true}`
4. Button block when prop `block={true}`

Task 2. Replace the button tag in `src/components/Login/index` with the `Button` component from `src/components/Form/Button`

### Part 2, sharing variables

You can share variables(like colours in this case) between CSS and JavaScript by using :export from CSS Modules.

Copy the Sass variables from `src/styles/variables.scss` into `src/styles/export/colours.scss`. You have an example on how we export `$white` in `colours.scss`. This way you can share your SASS variables with JavaScript to incrementally migrate the CSS in styled-components.

`src/components/App.js` shows you how we use the Sass `$white` variable as a JavaScript variable.

### Part 3, refactoring

Now that you have your Sass variables in JS, you can start refactoring your application.

Current styles, which are being mapped to our components via classes, can be found in the index.css file (Sass is being compiled to CSS) which is being imported to the `src/index.js` file. The goal of the refactoring is to migrate those `src/index.js` styles into styled-components. Let's start by migrating the styles from two components into styled-components.

- The first component, uncomment the `AppWrapper` component in `src/components/App.js`. Follow the comments in that file to get more tips.
- The second component is more interesting since you can use some conditional rendering in the CSS (meaning using props in your styles). Refactor the styles from the `src/components/Layout/Avatar.js` component into styled-components.

## Bonus exercise

Let's migrate the rest of the FB-Messenger Sass styles into styled-components 💪 🎉

- Take appropriate styles from the stylesheet for each of the component and create styled components within each of the components or as a separate component should you need it (if the styled-component is being used on multiple places).
- You can work your way through your application, starting with smaller components in the Layout folder to the bigger ones in Messenger.

## Articles and links

- [ReactJS article on Styling in React](https://reactjs.academy/blog/styling-in-react/)
- [https://www.styled-components.com/](https://www.styled-components.com/)
- [https://github.com/css-modules/webpack-demo](https://github.com/css-modules/webpack-demo)
- [https://github.com/css-modules/css-modules/](https://github.com/css-modules/css-modules/)

## License

This material is available for private, non-commercial use under the [GPL version 3](http://www.gnu.org/licenses/gpl-3.0-standalone.html).
