# simple-react-mathjax

`simple-react-mathjax` provides React component to render MathML, TeX or ASCIImath formulas.

## Installation
Install `simple-react-mathjax` as a dependency:

```
npm install simple-react-mathjax
```

## Usage
Add your MathJax configuration in index.html

```
<script type="text/x-mathjax-config">
        MathJax.Hub.Config({
          tex2jax: {
            inlineMath: [["$", "$"], ["\\(", "\\)"]],
            displayMath: [["$$", "$$"], ["\\[", "\\]"]]
          },
          showMathMenu: false,
          messageStyle: "none"
        });      
</script>
<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML"></script>


```

Import the package and Wrap your components with Mathjax.

```js
import React, {Component} from 'react'
import {render} from 'react-dom'
import MathJax from 'react-mathjax-preview'

class Demo extends Component {
  constructor(props) {
    super(props);
    this.state = {
      math: tex
    }
  render() {
    return <Mathjax><div>$sec \\theta / cosec \\theta$</div></Mathjax> />
  }
}
```


