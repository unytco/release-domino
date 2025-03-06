ase 1 Testing Details

#### links to other documents

Test Plan
Intro to RAVEs
[Piecework Setup](https://hackmd.io/sTH9kh57Qwu32ceYkkH-YQ)
[Phase 1 Testing Details](https://hackmd.io/-SoiQbJ-SqGOGm_U0tzQSw)
Issues


  * How to test:

  * Intro Document
    * Set up new user / accounts  (3?)
    * See guide of code template with code examples for different sections
    * Create Code Template
      * Who: created by your project’s engineering team with support from Unyt.
      * Components of Code Template 
        * Template Title 
        * Input Signature (JSON Schema)
        * Parked Invoice Signature (JSON Schema)
        * Output Signature (JSON Schema)
    * Create Executable Agreement
      * Who: created by your project’s engineering team. 
        * Infrastructure_Account_Pub_Key
          * Select one
            * FromParkedInvoice
            * RAVEFixed
            * ExecutorProvided
            * Fixed (if you use this, assign pubkey now)
            * Query
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
    * Send direct transactions via Promise
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



    * Receive direct transaction via Promise
      * Who: any member of your community in good standing.
        * In Agent UI for Receiver, go to Transactions > Actionable Transactions
        * Find Promise, check details and click the accept button (on the right)
          * As soon as you click, the software will check that the spender was not attempting to spend beyond their credit limit. 
          * If that is fine, it immediately credits the amount to your account.





    * Request direct transaction via Invoice
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



    * Pay an Invoice
      * Who: any member of your community in good standing with adequate credit available.
        * After an invoice has been sent to you, go to the Actionable Transactions section of your agent’s UI. 
        * Find the invoice
        * Check the details of the invoice
        * Click button to pay the invoice (Spend?)
          * As soon as you click, the software will check that you are not attempting to spend beyond your credit limit. 
          * If that is fine, it immediately deducts the amount from your balance and makes it available to the receiver
          * It also deducts any associated transaction fees from your account.



    * Receive Payment of an Invoice
      * Who: Any member of your community in good standing
        * After reloading, the Receiving Agent will find the transaction in the Actionable Transactions section of their Agent UI
        * Check the details and click accept
          * As soon as you click, the software will check that the spender was not attempting to spend beyond their credit limit. 
          * If that is fine, it immediately credits the amount to your account.





      * Send Transaction using a RAVE
        * Create Code Template
        * Create Executable Agreement
        * Create Execution Instance
          * Select Executable Agreement
          * take steps to set up
          * trigger execution
      * Sender
      * Executor
      * Receiver

