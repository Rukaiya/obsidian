* Class requires a constructor
* Constructor uses super to call the base class
* `componentDidMount()` is a lifestycle event or hook. It runs after the component has been rendered to the DOM
* `setInterval` will keep working even after routing is changed. So we have to close it.
We can use `componentWillUnmoun()` to clear it.
* Never change props within components. Only use it