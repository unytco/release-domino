# Phase 1 Testing Details

#### links to related docs

- [Test Plan](./1_0_testing_plan.md)
- [HFvZ Setup](../README.md)
- [Phase 1 Testing Details](./1_1_phase_testing_details.md)
- [Intro to RAVEs (Three Layers)](./1_2_three_layers_of_raves.md)
- [Sample Code for Creating RAVEs](./rave_templates)
- [Feedback](https://github.com/orgs/unytco/projects/5/views/1)



### Transactions
We have two main categories of transactions:
1) Direct Mutual Credit Transactions
2) RAVE Transactions

#### Direct Mutual Credit Transactions
A Process Overview

Direct transactions involve a sender and a receiver and can be initiated in two different ways:

1) A Promise
2) An Invoice

You can find each of these as Transaction Type options when Creating a Transaction under Transactions > MC Tx

##### 1) Promise
A sending of payment by the spender to a receiver.
    
The workflow is as follows:
**1) The Promise**
Spender promises a specific amount to a specific receiver. As soon as the Spender clicks "Create a Promise" the funds are immediately debited from their account balance along with any associated transaction fees.

**2) The Between Times (Before Acceptance)**
Spender will see the transaction as a "Completed Transaction" of the type "promise". At this point, Receiver will see the transaction as an "Actionable Transaction" of the type "Promise" and will be shown the details and an option to Accept the payment.

**3) Acceptance**
Receiver clicks accept. The funds are immediately credited to their account.

**Summary**
This form of payment is a multi-step process with validation happening behind the scenes for both the making of the promise and the acceptance of the promise. 

Reminder: In Holochain, individual agents each have their own activity history (source chain) and they alone authorize state changes to their own source chain. Each agent is responsible for checking the validity of the action they are taking, and each action is also independently validated by other devices on the the network. Agents are able to validly spend amounts (including fees), going into the negative up to their credit limit (if they have a credit limit).
    
##### 2) Invoice
A request for payment, made by the receiver. 

A receiver can request a payment by sending an invoice. They will indicate the Spender and the Amount Requested.

The workflow is as follows:

1) Invoice Request

2) The Between Times (Before Invoice is Paid)
After an invoice is sent, the receiver will see it in their Pending Transactions as an Invoice and the spender will see it in their Actionable Transactions as an Invoice and will have a button to Pay the invoice on the right hand side. (Spender may need to refresh first). At this point, only a request has been made and no funds have been debited or credited to either account. 
    
3) Paying an Invoice
The process that follows from this point forward is identical to the Promise workflow, as the Spender is now making a Promise (though the details had initially be proposed by the receiver).
As soon as the Spender clicks "Pay" the funds are immediately debited from their account balance along with any associated transaction fees. 

4) The Between Times (Before Acceptance)
Spender will see the transaction as a "Completed Transaction" of the type "promise". At this point, Receiver will see the transaction as an "Actionable Transaction" of the type "Promise" and will be shown the details and an option to Accept the payment.


5) Acceptance
Receiver clicks accept. The funds are immediately credited to their account. Receiver will now see the transaction as a Completed Transaction of the type "Accepts".

Summary
An invoice transaction involves the same underlying payment workflow as a promise transaction, but enables the Receiver to initialize the request.


### Making a Direct Transaction 
A step-by-step walk through.

The below Direct Transactions will only work if the sender has available credit in their account.


### Send direct transactions via Promise
  * Who: Any member of your community in good standing with available credit in their account.
    * Transaction Type
      * select Promise
    * Amount
      * (pick an amount that is less than that agents remaining credit limit)
    * Receiver
      * Copy receivers public key (ask that agent for it, or if in dev mode, click on the receiver’s icon in that agents window to copy it to clipboard)
      * Paste receivers public key into Receiver field
    * Note
      * Add a note if you want (optional)
    * Click create Promise
      * As soon as you click, the software will check that you are not attempting to spend beyond your credit limit. 
      * If that is fine, it immediately deducts the amount from your balance and makes it available to the receiver
      * It also deducts any associated transaction fees from your account.



### Receive direct transaction via Promise
  * Who: any member of your community in good standing.
    * In Agent UI for Receiver, go to Transactions > Actionable Transactions
    * Find Promise, check details and click the accept button (on the right)
      * As soon as you click, the software will check that the spender was not attempting to spend beyond their credit limit. 
      * If that is fine, it immediately credits the amount to your account.





### Request direct transaction via Invoice
  * Any member of your community in good standing
    * Transaction Type
      * select Invoice
    * Amount
      * (pick an amount that is less than that agents remaining credit limit)
    * Spender
      * Copy Spender’s public key (ask that agent for it, or if in dev mode, click on the receiver’s icon in that agents window to copy it to clipboard)
      * Paste Spenders public key into Spender field
    * Note
      * Add a note if you want (optional)
    * Click create Invoice
      * As soon as you click, the software will send an Actionable Transaction to the party being invoiced (the spender).



### Pay an Invoice
  * Who: any member of your community in good standing with adequate credit available.
    * After an invoice has been sent to you, go to the Actionable Transactions section of your agent’s UI. 
    * Find the invoice
    * Check the details of the invoice
    * Click button to pay the invoice (Spend?)
      * As soon as you click, the software will check that you are not attempting to spend beyond your credit limit. 
      * If that is fine, it immediately deducts the amount from your balance and makes it available to the receiver
      * It also deducts any associated transaction fees from your account.



### Receive Payment of an Invoice
  * Who: Any member of your community in good standing
    * After reloading, the Receiving Agent will find the transaction in the Actionable Transactions section of their Agent UI
    * Check the details and click accept
      * As soon as you click, the software will check that the spender was not attempting to spend beyond their credit limit. 
      * If that is fine, it immediately credits the amount to your account.





### Send Transaction using a RAVE
* Create Code Template
* Create Executable Agreement
* Create Execution Instance (Recorded Execution)
  * Select Executable Agreement
  * take steps to set up
  * trigger execution

* Parties
  * Sender
  * Executor
  * Receiver



See guide of code template with code examples for different sections


### Create Code Template

* Who: created by your project’s engineering team with support from Unyt.
      * Components of Code Template 
        * Template Title
        * Execution Code 
        * Input Signature (JSON Schema)
        ~~* Parked Invoice Signature (JSON Schema)~~
        * Output Signature (JSON Schema)

### Create Executable Agreement
  * Who: created by your project’s engineering team. 
    * Infrastructure_Account_Pub_Key
      * Select one
        * FromParkedInvoice
        * RAVEFixed
        * ExecutorProvided
        * Fixed 
            * (if you use Fixed, assign pubkey now)
        * Query 
            * (Query allows you to add a query to the [HDK](https://docs.rs/hdk/latest/hdk/), 80% of the time this will be a get-links call. See this [example code template].(https://github.com/unytco/hfvz/blob/develop/docs/rave_templates/test_query_rave_template.md))
    * Claiming_Agent_Pub_Key
      * Select one
        * FromParkedInvoice
        * RAVEFixed
        * ExecutorProvided
        * Fixed (if you use this, assign pubkey now)
        * Query
    * Infrastructure_Account_Credit_Limit
          * Select One
            * FromParkedInvoice
            * RAVEFixed
            * ExecutorProvided
            * Fixed (if you use this, assign credit limit)
            * Query