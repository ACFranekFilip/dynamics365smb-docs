---
    title: How to Reconcile Bank Accounts by Using Bank Statements | Microsoft Docs
    description: [!INCLUDE[d365fin](includes/d365fin_md.md)] provides a **Bank Rec.Worksheet** that you can use to reconcile bank account ledger entries with bank statements.
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
# How to: Reconcile Bank Accounts by Using Bank Statements
[!INCLUDE[d365fin](includes/d365fin_md.md)] provides a **Bank Rec.Worksheet** that you can use to reconcile bank account ledger entries with bank statements.  
  
### To reconcile bank accounts with bank statements  
  
1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Account Reconciliations**, and then choose the related link.  
  
2.  On the **Home** tab, in the **New** group, choose **New**.  
  
3.  On the **General** FastTab, fill in the required fields as described in the following table.  
  
    |Field|Description|  
    |---------------------------------|---------------------------------------|  
    |**Bank Account No.**|The bank account number to reconcile.|  
    |**Statement No.**|The bank statement number to reconcile.|  
    |**Statement Date**|The bank statement date.|  
    |**Statement Balance**|The bank statement balance.|  
  
4.  On the **Actions** tab, in the **Functions** group, choose **Mark Lines**.  
  
    > [!NOTE]  
    >  In the **Functions** group, you can also select the following bank reconciliation functions: suggest lines, clear lines, record adjustments, and recalculate the general ledger balance.  
  
5.  In the **Bank Rec. Process Lines** batch job, on the **ADD INCLUDE<!--[!INCLUDE[bp_optionsheading](../../includes/bp_optionsheading_md.md)]-->** FastTab, fill in the fields as described in the following table.  
  
    |Field|Description|  
    |---------------------------------|---------------------------------------|  
    |**Record type to process**|Specify the type as **Checks**, **Deposits**, or **Both**.|  
    |**Mark lines as cleared**|Select to process the option selected in the **Record type to process** field.|  
  
6.  On the **Bank Rec. Line** FastTab, select the appropriate filters.  
  
7.  Choose the **OK** button.  
  
8.  In the **Bank Rec.Worksheet** window, on the **Adjustments** FastTab, on the **Bank Rec. Adj. Lines Subform** FastTab, enter information into the remaining fields to make adjustments.  
  
    > [!NOTE]  
    >  If needed, you can also use the Bank Rec.Worksheet window to view the **Bank Reconciliation Comments** card or the **Bank Reconciliation** card. This feature is available on the **Navigate** tab.  
  
9. On the **Actions** tab, in the **Posting** group, choose **Post**.  
  
## See Also  
 [How to: Fill In Bank Reconciliations](how-to-fill-in-bank-reconciliations.md)   
 [How to: Post Bank Reconciliations](how-to-post-bank-reconciliations.md)   
 [How to: Post a Bank Reconciliation](how-to-post-a-bank-reconciliation.md)   
 [How to: Print Bank Reconciliation Reports](how-to-print-bank-reconciliation-reports.md)   
 Bank Account Ledger Entries