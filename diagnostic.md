# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components. Explain why each piece might be it's own component.

    ```md
    One example would be a hierarchy represented by a top level component called 'Recipe Title' and, below that visually, a
    nested component called 'Ingredients'.  A change to one would not conceptually affect the other (unless that was the
    desired outcome).  To see the 'Ingredient' component I might want to click on the 'Recipe Title'.  I could add different
    ingredients without affectng the 'parent' component.
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember generate component my-map
    ```

1.  What files are created and/or edited to produce a component, and what are their responsibilities?

    ```md
    There are two files generated.  component.js and template.hbs.  The component.js is responsible
    for the actions and the template.hbs is responsible for the html and the page that is presented
    to the User.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` route. What is
    the syntax (code that is written) to render this component inside that template?

    ```html
    {{#link-to 'my-contact' my-contact}} {{/link-to}}
    ```

1.  Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{#each my-contact.my-phone as |my-phone|}}
    {{my-contact/my-phone=my-phone
  {{/each}}
    ```
