#### Code Review

- spinner should be added while searching for books for better user experience.
- better to use async pipe to display the data from store selectors instead of using subscribe for every selector, as we need not to explicitly unsubscribe them.
- naming convenction of test cases should be in proper format.
- wherever we are using subscription, that needs to be unsubscribed in ngDestroy to prevent the memory leak issue.

#### Accessibility Issues - Manually found (Fixed all the below issues)

- Image elements do not have explicit width and height and 'alt' attributes.
  Set an explicit width and height on image elements to reduce layout shifts and improve CLS.
- Large network payloads cost users real money and are highly correlated with long load times.
- Background and foreground colors do not have a sufficient contrast ratio.
  Low-contrast text is difficult or impossible for many users to read.
- Insecure URL Request Resolution /books/content?id= found.
- Javascript text is not being highlighted.
- Added aria disabled for the want to read button.
- Modified the label for want to read button (Added book title to the label).

#### Issues from automated scan (Fixed)

- Background and foreground colours do not have a sufficient contrast ratio.

#### Fixed issues from code review section

- Error handling for the book search api and null/undefined/empty check is added for the response object
- Reducers were added
- Added test cases for reading list component, book search component, book reducer, book effects, reading list effects and reducer