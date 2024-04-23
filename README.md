# Pipenile Coding Test
## Description
Implement a dynamic filter function for a mock order management system using JavaScript. The function should allow filtering of order data based on multiple criteria such as status, quantity, amount, and creation date ranges. The solution should be easily extensible, allowing additional filters to be added or modified with minimal changes to existing code.

---
## Requirements


**1. Data Structure:** Use the following mock data for the orders:
```javascript

const orders = [
  { id: 1, status: 'shipped', quantity: 10, amount: 150, createdDate: '2022-04-01' },
  { id: 2, status: 'pending', quantity: 5, amount: 90, createdDate: '2022-04-02' },
  { id: 3, status: 'delivered', quantity: 20, amount: 300, createdDate: '2022-03-30' },
  // Add more mock data as needed
];
```

**2. Filter Functionality:**
- Filter by status (e.g., 'shipped', 'pending', 'delivered').
- Filter by quantity (exact match).
- Filter by amount (range: minimum and maximum).
- Filter by creation date (range: from and to dates).
  
**3. Coding Standards:**
- Write clean and readable code.
- Use functional programming techniques where applicable.
- Avoid using multiple if-else conditions; strive for a scalable and maintainable solution.
  
**1. Output:**
- The function should return an array of orders that match all provided filters.

---
## Instructions for Candidates:

**1. Create a New Public Repository:** Go to your GitHub account and create a new public repository. Name the repository: `pipenile-order-filter`.

**2. Set Up Your Repository:**
- Initialize your repository by creating a new file named `main.js`.
  
**3. Copy the Starter Code:**
- Copy the provided [starter code](#starter-code) into the main.js file in your repository.
  
**4. Implement the Filter Functionality:**
- Open the `main.js` file and implement the `filterOrders` function to add the required filtering functionality.
- Ensure your implementation matches the requirements described, such as filtering orders by status, quantity, amount range, and creation date range.
  
**5. Test Your Code:**
- Ensure that your code runs correctly against the sample data provided. Test various scenarios to validate the filtering logic.
  
**6. Document Your Work:**
- Write comments within the `main.js` file to explain your implementation approach. This helps reviewers understand your thought process and design choices.
  
**7. Create a New Branch and Pull Request:**
- Create a new branch named `feature/order-filter` from your `main` branch.
- Commit your changes to this new branch.
- Push the `feature/order-filter` branch to your GitHub repository.
- Create a pull request from your `feature/order-filter` branch to the `main` branch in your repository for review.
  
**8. Submit Your Work:**
- Once your pull request is ready, email the link to the pull request to pipenile.com@gmail.com.
  - Email Subject: PN CODING TEST B7 [YOUR NAME]. (make sure you replace the placeholder with your name)
  - Include a brief message in the email body stating that you are submitting the pull request link for the coding test.
   
#### Starter Code

```javascript

/**
 * test-b07
 * Filters orders based on provided criteria.
 * @param {Array} orders - Array of order objects.
 * @param {Object} criteria - Filtering criteria.
 * @returns {Array}
 */
function filterOrders(orders, criteria) {
  // Your code here
  return []; // Return filtered orders
}

// Example usage (this part will be used by reviewers to test your implementation)

const orders = [
  { id: 1, status: 'shipped', quantity: 10, amount: 150, createdDate: '2022-04-01' },
  { id: 2, status: 'pending', quantity: 5, amount: 90, createdDate: '2022-04-02' },
  { id: 3, status: 'delivered', quantity: 20, amount: 300, createdDate: '2022-03-30' },
  { id: 4, status: 'processing', quantity: 8, amount: 120, createdDate: '2022-04-04' },
  { id: 5, status: 'cancelled', quantity: 12, amount: 180, createdDate: '2022-05-01' },
  { id: 6, status: 'returned', quantity: 6, amount: 110, createdDate: '2022-04-25' },
  { id: 7, status: 'shipped', quantity: 15, amount: 200, createdDate: '2022-04-15' },
  { id: 8, status: 'pending', quantity: 30, amount: 450, createdDate: '2022-03-21' },
  { id: 9, status: 'delivered', quantity: 25, amount: 375, createdDate: '2022-05-05' },
  { id: 10, status: 'processing', quantity: 9, amount: 95, createdDate: '2022-06-01' },
  { id: 11, status: 'cancelled', quantity: 5, amount: 75, createdDate: '2022-05-20' },
  { id: 12, status: 'returned', quantity: 16, amount: 240, createdDate: '2022-05-15' },
  { id: 13, status: 'shipped', quantity: 10, amount: 150, createdDate: '2022-04-10' },
  { id: 14, status: 'pending', quantity: 7, amount: 105, createdDate: '2022-04-20' },
  { id: 15, status: 'delivered', quantity: 22, amount: 330, createdDate: '2022-06-02' }
];

const filteredOrders = filterOrders(orders, {
  status: 'delivered',
  quantity: 20,
  amount: { min: 250, max: 350 },
  dateRange: { from: '2022-03-01', to: '2022-04-01' }
});
console.log(filteredOrders);
```