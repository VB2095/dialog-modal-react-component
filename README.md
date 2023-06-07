# dialog-modal-react-component

> A React component for a modal made with dialog html element

[![NPM](https://img.shields.io/npm/v/dialog-modal-react-component.svg)](https://www.npmjs.com/package/dialog-modal-react-component) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Install

```bash
npm install --save dialog-modal-react-component
```

## Usage

Where you want to use the modal, import the component and use it like this:

```jsx
import { useEffect } from "react";

import Modal from "dialog-modal-react-component";
import "modal-dialog-react-component/dist/index.css";

class Example extends Component {
  render() {
    const [isModalOpen, setIsModalOpen] = useState(false); // state to control the modal
    return (
      <Modal isOpen={isModalOpen} setIsOpen={setIsModalOpen}>
        {Children}
      </Modal>
    );
  }
}
```

Then use `setIsModalOpen(true)` to open the modal. It can be used in a button onClick event for example, or when your form is submited.

## Example

```jsx
import React from "react";
import Modal from "dialog-modal-react-component";
import { useState } from "react";
const App = () => {
  const [isModalOpen, setIsModalOpen] = useState(false);
  const handleClick = () => {
    setIsModalOpen(true);
  };
  return (
    <>
      <p>App</p>
      <button onClick={handleClick}>Ouvrir la modal</button>
      <Modal isOpen={isModalOpen} setIsOpen={setIsModalOpen}>
        <p>Modal</p>
      </Modal>
    </>
  );
};

export default App;
```

## Customize

This component comes with a basic default style and is imported as `import "./modal.css";` but you can customize it by adding your own css.
Check the repository to get the default style and its classes and override it in your own css file.

Example:

```css
.modal {
  background-color: #fff;
  border-radius: 5px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.25);
  padding: 1rem;
  width: 100%;
  max-width: 40rem;
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 100;
}
```

## License

MIT © [VB2095](https://github.com/VB2095)
