<!-- loioa6c978f734de4574a2291a971f447179 -->

# Example 2: Display Customers with Related Contracts

> ### Sample Code:  
> ```
> I want to create an SAP Fiori application that shows my customers with their contracts. 
> Each customer has the following attributes:
> 
> 1. Name
> 2. Identification Number
> 3. Address
> 4. Contract Information
> A contract is referencing a customer. One customer can have multiple contracts. Attributes of a contract include:
> 5. Contract ID: A unique identifier for the contract
> 6. Customer: Information about the customer involved
> 7. Contract Type: The type of contract (sales, service, employment)
> 8. Start Date: The date on which the contract becomes valid
> 9. End Date: The date on which the contract expires (if applicable)
> 10. Status: The current status of the contract (draft, active, expired, terminated, etc.)
> 
> When starting the CAP application I first want to see a list of customers.
> 
> When selecting a specific row in that list, I want to see to a page with details of that customer.
> 
> It should show the following sections:
> - section "Customer Info" displaying the attributes of the selected customer
> - section "Contracts" showing a list of all contracts for this customer
> 
> When selecting a specific row in the contracts list, I want to see a page with details of that contract. This page should show two sections:
> - section "Contract Info" containing:
>   - contract ID
>   - Customer Name
>   - Contract Type
>   - Status
> - section "Validity" containing
>   - Start Date
>   - End Date
> ```

