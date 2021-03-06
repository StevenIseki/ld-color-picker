# ld-color-picker
color-picker plugin for [last-draft](http://lastdraft.vace.nz)

[![npm version](https://badge.fury.io/js/ld-color-picker.svg)](https://badge.fury.io/js/ld-color-picker)

# Install
```jsx
npm install ld-color-picker --save
```

# Use
```jsx
import {Editor} from 'last-draft'
import color from 'ld-color-picker'
let plugins = [color]

export default class ExampleEditor extends Component {
  constructor(props) {
    super(props)
    const INITIAL_STATE = editorStateFromHtml('<div></div>')
    this.state = { value: INITIAL_STATE }
  }

  onChange(editorState) {
    this.setState({ value: editorState })
  }

  render() {
    return (
      <Editor
        inline={['bold', 'italic', 'code', 'dropcap']}
        blocks={['h2', 'quote']}
        plugins={plugins}
        editorState={this.state.value}
        onChange={::this.onChange} />
    )
  }
}
```

## Styles

Last Draft plugins use styled-components 💅 for the base styling.

## Custom Styles with CSS

You can also add custom css to override the base styling with the following class names specified below:

```css
.ld-button-color-picker {}
.ld-color-picker-modal-wrapper {}
.ld-color-picker-wrapper {}
.ld-color-picker-close-wrapper {}
.ld-color-picker-close {}
.ld-color-picker {}
.ld-color-picker-item {}
```
