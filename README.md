# refactoring-the-atm
An exercise in refactoring an existing ATM project.

This is a simple example of an ATM (or it could be a banking app for an institution with no engineering resources). The app is built as an HTML page with css and React on the backend.

The app presents a default blank menu and instructs the user to choose an action, either Deposit or Withdraw from their account.

If the user selects either Deposit or Withdraw, then a field appears for the submission of some amount for either transaction.

The only constraint on the user is that they cannot withdraw more funds than they have deposited. The ATM does not loan money.

### Changes to the code

- Changed ‘’status’ to ‘balance’ because ‘status’ is deprecated in React
- Changed ‘Cash Back’ to ‘Withdraw’ because that’s more accurate
- Changed the title from “onClick’ to ‘Simple ATM’ reflect the application’s purpose
- Removed ‘Refresh here…’ from the page to make the interface cleaner
- Centered the text 

### Planned improvements

- Attempted to add an alert when insufficient funds are available to support a withdrawal, but could not find a way yet to preempt the selection of the submit button by the alert when the alert is trigged
```js
 alert (`Insufficient funds available. Please deposit $${ Number(event.target.value - totalState)} to continue.`);
 ```

- On submit, the amount input for deposit or withdrawal should be removed automatically. Currently the amount remains even when a different action is selected from the menu.
