---
    title: How to Export Electronic Payments | Microsoft Docs
    description: You can use the Export Electronic Payments report to export payment journal entries to a file that is based on the Automated Clearing House (ACH) standard file format or the International ACH Transaction (IAT) file format.  The file can then be used to transmit electronic payments to a bank. For more information, see [How to: Transmit Electronic Payments](how-to-transmit-electronic-payments.md).
    services: project-madeira
    documentationcenter: ''
    author: SorenGP

    ms.service: dynamics365-financials
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 07/01/2017
    ms.author: sgroespe

---
# How to: Export Electronic Payments
You can use the Export Electronic Payments report to export payment journal entries to a file that is based on the Automated Clearing House (ACH) standard file format or the International ACH Transaction (IAT) file format.  The file can then be used to transmit electronic payments to a bank. For more information, see [How to: Transmit Electronic Payments](how-to-transmit-electronic-payments.md).  
  
> [!IMPORTANT]  
>  If you have set up the **Payment Export Format** field in the **Bank Account Card** window, for example to export using the SEPA standard, then the following procedure is not valid. To export these payments, refer to [How to: Export Payments to a Bank File](how-to-export-payments-to-a-bank-file.md).  
  
### To export electronic payments  
  
1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.  
  
2.  On the **Navigate** FastTab, choose **Electronic Payments**, and then choose **Export**.  
  
3.  In the **Export Electronic Payments** window, on the **Options** FastTab, fill in the fields as described in the following table.  
  
    |Field|Description|  
    |---------------------------------|---------------------------------------|  
    |**Bank Account No.**|Enter the bank account from which these payments will be taken.|  
    |**Settle Date**|Enter the settle date that will be transmitted to the bank. This date will become the posting date for the exported payment journal entries. Transmission should occur two or three banking days before the settle date. Ask your bank for the exact number of days.|  
    |**If Posting Date does not match Settle Date**|Select what will occur if the posting date does not match the settle date. The options are to change the posting date to match the entered settle date, or to skip any payment journal lines where the entered posting date does not match the settle date.|  
    |**Number of Copies**|Enter the number of additional copies of the remittance advice that will be printed by this process. One document is always printed to mail to the payee, but additional copies can be printed if they are needed.|  
    |**Print Company Address**|Select if you want the company address printed on the remittance advice. If not selected, the remittance advice already has the company address preprinted on it.|  
  
4.  On the **Gen. Journal Line** FastTab, select the appropriate filters.  
  
## See Also  
 [Electronic Payments for United States, Canada, and Mexico](electronic-payments-for-united-states-canada-and-mexico.md)   
 [How to: Set Up Electronic Payments for Bank Accounts](how-to-set-up-electronic-payments-for-bank-accounts.md)   
 [How to: Transmit Electronic Payments](how-to-transmit-electronic-payments.md)   
 [How to: Generate Electronic Payments](how-to-generate-electronic-payments.md)   
 Payment Journal   
 Export Electronic Payments