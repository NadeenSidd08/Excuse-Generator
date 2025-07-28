# Excuse-Generator

Build a Next.js application called "Excuse Generator 3000".

1. Core Functionality:

Create a main page with the title "Excuse Generator 3000".
The page should feature a card with a text area where a user can describe their situation. The text area should have a placeholder like "e.g., I double-booked myself for a meeting and my cousin's birthday dinner...".
Below the text area, there should be a "Generate Excuse" button.
When the "Generate Excuse" button is clicked:
Show a loading state.
Send the situation text in a POST request to [ENTER YOUR API KEY].
The request body should be a JSON object: { "situation": "The user's input" }.
The API will respond with JSON formatted as { "excuse": "A generated excuse string" }.
Parse this response and display only the excuse string value in a new card titled "Your Generated Excuse:".
Handle potential errors from the API call and display a user-friendly error message in an alert component.
Include a subtle fade-in animation for the card that displays the generated excuse.

2. Email Functionality:

After an excuse has been successfully generated and displayed, reveal a new section within the excuse card's footer.
This section must contain:
An input field for the user to enter a recipient's email address.
A "Send Email" button.
When the "Send Email" button is clicked:
Show a loading state on the button.
Send a POST request to [ENTER YOUR API KEY].
The payload for this request must be a JSON object containing the recipient's email, the original situation, and the generated excuse: { "email": "...", "situation": "...", "excuse": "..." }.
Upon successful submission, show a success toast notification (e.g., "Excuse sent to recipient@example.com.").
If the email sending fails, show an error toast notification with the reason for the failure.
Implement basic validation: the "Send Email" button should be disabled if the email input is empty.

3. Styling and Component Usage:

Use ShadCN UI components for all UI elements: Card, Button, Textarea, Input, Label, Alert, Toast, and Skeleton for loading states.
The page layout should be clean, centered, and modern.
Apply the following color scheme in globals.css:
Background: Light Gray (#F5F5F5)
Card/Input Background: White (#FFFFFF)
Primary (for buttons/headers): Teal (#008080)
Use the Wand2 icon for the "Generate Excuse" button and the Mail icon for the "Send Email" button from lucide-react.
