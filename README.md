# React Csv Parse

Parse content of a csv file.
Inspiration: (paypal/downshift)[https://raw.githubusercontent.com/paypal/downshift]
Development structure: (github.com/insin/nwb)[https://github.com/insin/nwb]

## Installation

```
npm install --save react-csv-parse
```

## Usage

```js
import CsvParse from "CsvParse"
```

```jsx
handleData = data => {
  this.setState({ data })
}
```

```jsx
render() {
  const fileHeaders = [
    "header1",
    "header2",
    "header3",
    "header4",
    "header5",
  ]

  return (
    <CsvParse
      fileHeaders={fileHeaders}
      onDataUploaded={this.handleData}
      render={onChange => <input type="file" onChange={onChange} />}
    />
  )
}
```

`CsvParse` is the only component. It doesn't render anything itself, it just
calls the child function and renders that. Wrap everything in
`<CsvParse>{/* your function here! */}</CsvParse>`.

`fileHeaders` are mandatory.
