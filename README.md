React Image Annotation
=========================

An  image annotation library built on React

## Installation

```
npm install --save react-image-annotation
```

## Usage

```js
export default class Simple extends Component {
  state = {
    annotations: [],
    annotation: {}
  }

  onChange = (annotation) => {
    this.setState({ annotation })
  }

  onSubmit = (annotation) => {
    const { geometry, data } = annotation

    this.setState({
      annotation: {},
      annotations: this.state.annotations.concat({
        geometry,
        data: {
          ...data,
          id: Math.random()
        }
      })
    })
  }

  render () {
    return (
      <Root>
        <Annotation
          src={img}
          alt='goomba'

          annotations={this.state.annotations}

          type={this.state.type}
          value={this.state.annotation}
          onChange={this.onChange}
          onSubmit={this.onSubmit}
        />
      </Root>
    )
  }
}
```

## License

MIT
"# react_annotation_dashboard" 
