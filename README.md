# dynamic-form-bs
### NPM Package Description: **DynamicFormsManager**

#### Overview:
**DynamicFormsManager** is a lightweight and flexible library for building and managing dynamic, metadata-driven forms in React applications. It simplifies the creation of complex forms by allowing developers to define forms declaratively through JSON or model-based metadata. The library supports a wide range of field types, validation rules, and API integrations to create highly interactive and customizable forms.

#### Features:
- **Metadata-Driven Forms**: Define forms dynamically using configuration objects or JSON schema.
- **Rich Field Support**: Includes text, number, select, date, checkbox, radio, and file upload field types out of the box.
- **Dynamic Field Updates**: Change field visibility, options, and properties based on user interaction.
- **Validation Made Easy**: Built-in validation for common scenarios (required, regex, length) and custom validation functions.
- **API Integration**: Fetch initial values and options dynamically or submit the form data to REST or GraphQL APIs.
- **Theming and Layout**: Fully customizable styles and layouts with CSS class integration.
- **Event Hooks**: Handle events like field changes, form submission, and error handling easily.
- **Localization Support**: Adapt labels, placeholders, and validation messages for multi-language applications.

#### Installation:
```bash
npm install dynamicformsmanager
```

#### Usage:
```javascript

class User extends CrudClass{
 name:string;
...

getFields(): FieldMetadata[] {
    return [
      {
        fieldName:"name",
        operations:["read", "update"],
        header:"Name",
        group:"Personal Infos",
        field_options:{
          size:4,
          className:"form-control",
          label:"Name",
          placeholder:"Name ex John",
        }
      }
    ] as FieldMetadata[];
  }
}
import User from ".../your/model/path"
import { DynamicFormCreate } from "dynamic-form-bs";

const onSubmit = (data) => {
  console.log("Form Data:", data);
};

const App = () => (
  <DynamicFormCreate model={User} onSubmit={onSubmit} />
);

export default App;
```

#### Documentation:
Visit the [GitHub repository](https://github.com/serge24/dynamic-form-bs) for detailed usage examples, API documentation, and advanced configuration options.

#### License:
This package is open-sourced under the MIT license.
