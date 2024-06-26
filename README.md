# Radio Buttons
​

## How to submit

1. You are required to have a Github URL to submit the coding test. Go create one if you haven't already.
2. Then, create a *private* repo to host the assignment and commit all the changes to that repo.
3. Grant access to the following Github users to assess your submission once you're done:
- antoniocarlosortiz
- nadinejamila
- joshuadiezmo


## Technical Challenge

Create an interactive and dynamic form using VueJS. The form should render multiple groups of radio buttons. 
​
Add a submit button at the bottom that is only enabled when a valid option from all groups has been selected.
​
The radio-button groups should be dynamically rendered based on the following data structure:
​
```javascript
[
  // first group of radio-buttons
  [
    { id: '101', value: 'Vegetarian' },
    { id: '102', value: 'Nut allergy' },
    { id: '103', value: 'Halal' }
  ],
  // second group of radio-buttons
  [
    { id: '201', value: 'Cashew chicken' },
    { id: '202', value: 'Sweet and sour pork' },
    { id: '203', value: 'Stir fried Tofu' },
    { id: '204', value: 'Vegetable fried rice' },
    { id: '205', value: 'Pad Thai' },
    { id: '206', value: 'Massaman beef' },
  ],
  // third group of radio-buttons
  [
    { id: '301', value: 'Peanut sauce' },
    { id: '302', value: 'Oyster sauce' },
    { id: '303', value: 'Vegetable spring rolls' },
    { id: '304', value: 'Steamed rice' },
  ],
]
```
​
Initially, only items from the first group are able to be selected. Inputs in second and third groups are to be initially disabled.
​
When an item from the first group is selected, valid items from the second group are enabled. Valid items are specified in a set of rules; which is an object where the key is the ID of an option, and the value is an array containing the IDs of options which are NOT compatible. Items in the third group remain disabled until an item in the second group is selected.
​
```javascript
{
  // 'Vegetarian' is NOT compatible with 'Cashew chicken', 'Sweet and sour pork', 'Massaman beef', 'Oyster sauce'
  101: [201, 202, 206, 302], 
  // 'Nut allergy' is NOT compatible with 'Cashew chicken', 'Peanut sauce',
  102: [201, 301], 
  // 'Halal' is NOT compatible with 'Sweet and sour pork',
  103: [202], 
  // 'Vegetable fried rice' is NOT compatible with 'Steamed rice' (you don't need more rice... carb overload),
  204: [304],
  // 'Pad thai' is NOT compatible with 'Steamed rice' (Pad thai comes with noodles),
  205: [304],
}
```
  
## Evaluation

Feel free to ask any questions you need to ask if need be, or if you need any clarification on the requirements.
​
We will evaluate your response based on the following criteria:
​
* Problem solving and design approach.
* Best practices.
* Code should be easy to read and understand. Self-explanitory variable/function/method names, with little to no comments required.
* Consistency in style, readability, naming conventions.
