# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components.

    ```md
    A blog-formatted web app, with a user profile 'page', a feed of posts and
    their associated comments, as well as maybe another feed of related topics
    or tags.
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember g component my-map
    ```

1.  What files are edited to produce a component, and what are their
    responsibilities?

    ```md
    A component.js file, which is responsible for describing action methods, defining an enclosing element type, and setting component object properties, and a template.hbs file which allows HTMLBars to render the ui content of the component through references to the enclosing object.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` path. What is
    the syntax for loading this component inside that template?

    ```html
    {{#each model as |contact|}}
      {{my-contact contact=contact}}
    {{/each}}
    ```

    Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{#each contact.phone as |phone|}}
      {{my-contact.my-phone phone=phone}}
    {{/each}}
    ```
