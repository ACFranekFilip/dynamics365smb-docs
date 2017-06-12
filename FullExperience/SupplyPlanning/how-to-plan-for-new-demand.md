---
title: "How to: Plan for New Demand"
ms.custom: na
ms.date: "03-03-2017"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "planning, demand"
  - "demand, setting up new"
  - "planning, orders"
ms.assetid: 722cd165-c926-4ed6-8233-58fe12e2c6a4
caps.latest.revision: 11
ms.author: "sgroespe"
manager: "terryaus"
translation.priority.ht: 
  - "da-dk"
  - "de-at"
  - "de-ch"
  - "de-de"
  - "en-au"
  - "en-ca"
  - "en-gb"
  - "en-in"
  - "en-nz"
  - "es-es"
  - "es-mx"
  - "fi-fi"
  - "fr-be"
  - "fr-ca"
  - "fr-ch"
  - "fr-fr"
  - "is-is"
  - "it-ch"
  - "it-it"
  - "nb-no"
  - "nl-be"
  - "nl-nl"
  - "ru-ru"
  - "sv-se"
---
# How to: Plan for New Demand
This planning task can be performed in the **Order Planning** window, which displays all new demand along with availability information and suggestions for supply. It provides the visibility and tools needed to effectively plan demand from sales lines and component lines and then create different types of supply orders directly.  
  
 You can enter the **Order Planning** window in two ways depending on your focus.  
  
### To plan for new production order demand  
  
1.  In the **Search** box, enter **Production Orders**, and then choose the related link. You can perform these steps for a planned, firm planned, or released production order.  
  
2.  Open the production order you want to plan.  On the **Navigate** tab, in the **Order** group, choose **Planning**.  
  
3.  In the **Order Planning** window, on the **Action** tab, in the **Functions** group, choose **Calculate Plan**.  
  
 The window displays planning lines according to the view filter **Production Demand**, meaning unfulfilled component lines of all existing production orders. Demand for only the one production order is not shown because t is necessary to plan for one production order with an overview of demand for potentially earlier components lines. Planning lines for the production order in context are expanded.  
  
### To plan for any new demand  
  
1.  In the **Order Planning** window, on the **Action** tab, in the **Functions** group, choose **Calculate Plan**.  
  
     The window displays planning lines according to the view filter **All Demand**, meaning sales order lines as well as production component lines with insufficient availability. You can change this filter as you like.  
  
     When the plan is being calculated, any new demand that has arisen since a plan was last calculated is analyzed. The quantity needed is calculated based on total availability of each demand line found. This calculation is done order\-by\-order, meaning that the order that includes the demand line with the earliest due date or shipment date is considered first, and all other demand lines in that production order, irrespective of their individual due dates or shipment dates, are also calculated for that order. Therefore, all planning lines under one order header line have the same demand date. When the calculation is completed, all unfulfilled demand is displayed as planning lines, sorted by the earliest demand date, with the various quantity fields filled in.  
  
     The **Order Planning** window is filled with order header lines representing orders with unfulfilled demand.  
  
    1.  The **Demand Date** field contains the earliest shipment or due date of a demand line in the order.  
  
    2.  The **Demand Type** field shows whether the demand is from sales lines or component lines.  
  
    3.  The **Description field** contains the following depending on the demand type.  
  
        |Demand type|[!INCLUDE[bp_tabledescription](../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
        |-----------------|---------------------------------------|  
        |**Production**|The description of the produced item.<br /><br /> For production demand for a project production order, the customer name is displayed. For more information, see [How to: Plan Project Orders](../OperationsPlanning/how-to-plan-project-orders.md).|  
        |**Sales**|The customer name.|  
  
     The first planning line has the earliest demand date, and therefore you should plan this line first. To see the actual demand lines, either sales order lines or component lines, of each order header line, you must expand the line.  
  
2.  Choose the **Expand \(\+\)** button in front of the date in the **Demand Date** field to see the underlying planning lines that represent demand lines with insufficient availability.  
  
3.  For each expanded planning line, that is, demand line, you can see values in information fields at the bottom of the window.  
  
    |[!INCLUDE[bp_tableoption](../ApplicationDesign/includes/bp_tableoption_md.md)]|[!INCLUDE[bp_tabledescription](../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |----------------------------------|---------------------------------------|  
    |**Qty. on Other Locations**|Shows if the item exists on another location. You can then look up and select it.|  
    |**Substitutes Exist**|Shows if a substitute item is created for the item. You can then look up and select it. Note that this feature only applies to components, that is, from demand lines of type **Production**.|  
    |**Quantity Available**|Shows the total availability of the item, that is, the Projected Available Balance.|  
    |**Earliest Date Available**|Shows the arrival date of an inbound supply order that can cover the needed quantity on a date later than the demand date.|  
  
4.  In the **Replenishment System** field, select which type of supply order to create.  
  
     The default value is that of the item card, or SKU card, but you can change it to one of three options:  
  
    |[!INCLUDE[bp_tableoption](../ApplicationDesign/includes/bp_tableoption_md.md)]|[!INCLUDE[bp_tabledescription](../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |----------------------------------|---------------------------------------|  
    |**Purchase**|Creates a purchase order.|  
    |**Transfer**|Creates a transfer order.|  
    |**Prod. Order**|Creates a production order.|  
  
     In the **Supply From** field you must select a value according to the selected replenishment system.  
  
    > [!NOTE]  
    >  If the field is not filled in, the system will display an error message when you use the **Make Supply Order** function, and no supply order will be created for the planning line in question. This, however, is not the case if the replenishment system is **Prod. Order**.  
  
5.  From the **Supply From** field, you can look up in the relevant list and select where the supply should come from:  
  
    -   If replenishment system is **Purchase**, the look\-up button in this field looks up in the **Item Vendor Catalog** window.  
  
    -   If replenishment system is **Transfer**, the look\-up button in this field looks up in the **Location List** window.  
  
     In case the item exists in another location, the **Qty. on Other Location** field at the bottom shows a value and you can then look up and select the location from which the item should be supplied when you make the transfer order.  
  
     If a substitute exists for the demanded item, the **Substitute Exists** field is set to **Yes**, and you can then look up to the **Item Substitution Entries** window and select the substitute.  
  
6.  Select the **Reserve** check box if you want to make a reservation between the supply order you are creating and the demand line that it is created for. It is empty by default.  
  
    > [!NOTE]  
    >  You can only select this check box if the item has **Optional** or **Always** in the **Reserve** field on its item card.  
  
7.  In the **Qty. to Order** field, you can enter the quantity that will go on the supply order you are creating.   
    The default value is the same quantity as that in the **Needed Quantity** field. But you may decide to order more or less than this quantity based on your knowledge of the demand situation. If, for example, you see in the **Order Planning** window that several unrelated demand lines are for the same purchased item, and they are due around the same date, you can consolidate these by entering the total needed quantity in the **Qty. to Order** field of one line, and then delete the other, obsolete planning lines for that item.  
  
8.  In the **Due Date** and **Order Date** fields, you can enter the dates that should apply to the created supply orders.  
  
     These two fields are interrelated according to the **Default Safety Lead Time** field, which can be found in the **Manufacturing Setup** window. By default, the due date is the same as the demand date, but you can change this as you like.  
  
> [!NOTE]  
>  If you enter a date later than the demand date, you will receive a warning message.  
  
### To make supply orders  
  
1.  In the **Search** box, enter **Production Orders**, and then choose the related link. You can perform these steps for a planned, firm planned, or released production order.  
  
2.  Open the production order you want to plan.  On the **Navigate** tab, in the **Order** group, choose **Planning**.  
  
3.  Place the cursor on a relevant planning line. In the **Order Planning** window, on the **Action** tab, in the **General** group, choose **Make Orders**.  
  
4.  In the **Make Supply Orders** window, on the **Order Planning** FastTab, in the **Make Orders for** field, select one of the following options.  
  
    |[!INCLUDE[bp_tableoption](../ApplicationDesign/includes/bp_tableoption_md.md)]|[!INCLUDE[bp_tabledescription](../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |----------------------------------|---------------------------------------|  
    |**The Active Line**|Make a supply order only for the line where the cursor is placed.|  
    |**The Active Order**|Make supply orders for all lines in the order where the cursor is placed.|  
    |**All Lines**|Make supply orders for all lines in the **Order Planning** window.|  
  
5.  On the **Options** FastTab, define what kind of supply orders, or requisition worksheet lines, should be made.  
  
    > [!NOTE]  
    >  The settings you last made in the **Make Supply Orders** window will be saved under your user ID so that they are the same the next time you use the window.  
  
6.  Choose the **OK** button to make the suggested supply orders or requisition worksheet lines.  
  
 You have now planned for the unfulfilled demand by making respective supply orders. Details about specific work flows when using the **Order Planning** window would depend on a company’s internal policies.  
  
 When you have finished your planning work in the **Order Planning** window, for example defined an alternative way to supply the quantity, you can proceed to create supply orders for one or more of the planning lines.  
  
> [!NOTE]  
>  The supply orders you create may introduce new dependent demand, for example for underlying production orders, and you should therefore choose **Calculate Plan** again to find and resolve this before moving down the list.  
  
## See Also  
 [Reserve](../Topic/\($%20T_27_100%20Reserve%20$\).md)   
 [About Planning Functionality](../OperationsPlanning/about-planning-functionality.md)   
 [How to: Refresh Production Orders](../OperationsPlanning/how-to-refresh-production-orders.md)   
 [How to: Replan Production Orders](../OperationsPlanning/how-to-replan-production-orders.md)   
 [How to: Run MPS and MRP](../OperationsPlanning/how-to-run-mps-and-mrp.md)   
 [Design Details: Supply Planning](../ApplicationDesign/design-details-supply-planning.md)   
 [Setup Best Practices: Supply Planning](../SetupAndAdministration/setup-best-practices-supply-planning.md)