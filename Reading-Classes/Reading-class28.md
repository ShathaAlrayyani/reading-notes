## Working with forms

The form is defined in HTML as a collection of elements inside <form>…</form> tags, containing at least one input
element of type="submit".

        <form action="/team_name_url/" method="post">
            <label for="team_name">Enter name: </label>
            <input id="team_name" type="text" name="name_field" value="Default name for team.">
            <input type="submit" value="OK">
        </form>

While here we just have one text field for entering the team name, a form may have any number of other input elements
and their associated labels.

The form attributes define the HTTP method used to send the data and the destination of the data on the server (action):

- action: The resource/URL where data is to be sent for processing when the form is submitted. If this is not set (or
  set to an empty string), then the form will be submitted back to the current page URL.
- method: The HTTP method used to send the data: post or get.
    - The POST method should always be used if the data is going to result in a change to the server's database, because
      it can be made more resistant to cross-site forgery request attacks.
    - The GET method should only be used for forms that don't change user data (for example, a search form). It is
      recommended for when you want to be able to bookmark or share the URL.

## Django form handling process

the view gets a request, performs any actions required including reading data from the models, then generates and
returns an HTML page (from a template, into which we pass a context containing the data to be displayed). What makes
things more complicated is that the server also needs to be able to process data provided by the user, and redisplay the
page if there are any errors.

1. Display the default form the first time it is requested by the user.
  - The form may contain blank fields if you're creating a new record, or it may be pre-populated with initial values (for example, if you are changing a record, or have useful default initial values).
  - The form is referred to as unbound at this point, because it isn't associated with any user-entered data (though it may have initial values).
2. Receive data from a submit request and bind it to the form.
  - Binding data to the form means that the user-entered data and any errors are available when we need to redisplay the form.
3. Clean and validate the data.
  - Cleaning the data performs sanitization of the input fields, such as removing invalid characters that might be used to send malicious content to the server, and converts them into consistent Python types.
  - Validation checks that the values are appropriate for the field (for example, that they are in the right date range, aren't too short or too long, etc.)
4. If any data is invalid, re-display the form, this time with any user populated values and error messages for the problem fields.
5. If all data is valid, perform required actions (such as save the data, send an email, return the result of a search, upload a file, and so on).
6. Once all actions are complete, redirect the user to another page.





