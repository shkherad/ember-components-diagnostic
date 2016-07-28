# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components.

    ```md
    home page (application) -> team -> Engineering Team -> Web Dev -> Shireen
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember g component my-map
    ```

1.  What files are edited to produce a component, and what are their
    responsibilities?

    ```md
    Component File:
      -can be edited to add css or JS actions to the component
    Template File
      -Display what you want in that component
    Parent Template Files
      -if you need to push data down


    application/route.js file.
      -only if this component is appearing in a different view state
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` path. What is
    the syntax for loading this component inside that template?

    ```html

    {{#link-to 'my-contact'}}My Contact{{/link-to}}

    ```

    Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    <ul>
      {{#each my-contact.my-phone as |phone|}}
        {{my-contact/my-phone phone=phone}}
      {{/each}}
    </ul>
    ```
