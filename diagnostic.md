# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components. Explain why each piece might be it's own component.

    ```md
    Twitter dashboard
    - List of tweets on the right
      - Individual tweets
    - User on the left
      - User details

    User info and the list of tweets could each be their own component to separate
    out the two different halve of the view. From their components could be rendered
    from inside each of these parent components.

    Individual tweets would need to be it's own component since the UI of all tweets
    are identical - retweet button, like button, etc. These actions can be compartmentalized
    into this component.

    User details could also be it's own component since the user's info sometimes
    changes depending on which view state you're on in the app. 


    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember g component my-map
    ```

1.  What files are created and/or edited to produce a component, and what are their responsibilities?

    ```md
    component.js and template.js

    The component.js houses the actions, properties and class names of a specific component.
    The template is used to render the view of the component which includes the html structure and data received
    back from the API.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` route. What is
    the syntax (code that is written) to render this component inside that template?

    ```html
    {{my-contact contact=model}}
    ```

1.  Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{my-contact/my-phone }}
    ```
