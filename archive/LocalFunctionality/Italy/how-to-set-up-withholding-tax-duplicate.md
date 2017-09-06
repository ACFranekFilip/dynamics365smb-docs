---
    title: How to Set Up Withholding Tax | Microsoft Docs
    description: Companies must pay withholding tax to the government for third-party services and vendor purchases. Withholding tax is calculated during invoice payment rather than during invoice posting.
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
# How to: Set Up Withholding Tax
Companies must pay withholding tax to the government for third-party services and vendor purchases. Withholding tax is calculated during invoice payment rather than during invoice posting.  
  
### To set up withholding tax codes  
  
1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Withhold Tax**, and then choose the link for the **Setup** area for payables.  
  
2.  Under **Lists**, choose **Code**.  
  
3.  To open a new withholding code, on the **Home** tab, choose **New**.  
  
4.  Enter information into the relevant fields.  
  
5.  To open add lines to the withhold code, on the **Navigate** tab, choose **Withhold Code Lines**.  
  
6.  Enter information into the relevant fields.  
  
7.  Choose the **OK** button.  
  
8.  To close the **Withhold Codes** window, choose the **OK** button.  
  
### To set up withholding tax for vendors  
  
1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.  
  
2.  Select the relevant vendor, and then, on the **Home** tab, in the **Manage** group, choose **Edit**.  
  
3.  Fill in the FastTabs as described in the following table.  
  
    |FastTab|ADD INCLUDE<!--[!INCLUDE[bp_tabledescription](../../includes/bp_tabledescription_md.md)]-->|  
    |-------------|---------------------------------------|  
    |**General**|The vendor personal data.|  
    |**Communication**|The contact details for the vendor.|  
    |**Invoicing**|The invoicing details for the vendor.|  
    |**Payments**|The payment information for the vendor.|  
    |**Receiving**|The subcontracting information for the vendor.|  
    |**Foreign Trade**|The foreign trade information for the vendor.|  
    |**Free Lance Fee**|Select the relevant withholding tax code in the **Withholding Tax Code** field to include the withholding tax information.|  
  
4.  To close the **Vendor Card** window, choose the **OK** button.  
  
### To calculate withholding tax for purchase invoices  
  
1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Invoices**, and then choose the related link.  
  
2.  Select the relevant purchase invoice, and then on the **Home** tab, in the **Manage** group, choose **Edit**.  
  
3.  On the **Navigate** tab, in the **Invoice** group, Choose **Withhold Taxes-Soc. Sec.**.  
  
4.  In the **Withh. Taxes-Contribution Card** window, on the **Withhold Taxes** FastTab, in the **Withholding Tax Code** field, select the code for the withholding tax.  
  
5.  To calculate the withholding tax amount before posting, on the **Home** tab, in the **Process** group, choose **Calculate**.  
  
6.  Choose the **OK** button.  
  
### To make a vendor payment  
  
1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.  
  
2.  In the **Batch Name** field, specify the relevant journal batch.  
  
3.  To create a new payment journal line, enter the relevant information in the fields.  
  
4.  To make a vendor payment, on the **Home** tab, in the **Process** group, choose **Post**.  
  
    > [!NOTE]  
    >  The amount in the new line in the **Payment Journal** window is the withholding tax payment amount.  
  
5.  To close the **Payment Journal** window, choose the **OK** button.  
  
## See Also  
 Vendor Card   
 Purchase Invoice   
 Payment Journal   
 [How to: Print Withholding Tax Reports](how-to-print-withholding-tax-reports.md)