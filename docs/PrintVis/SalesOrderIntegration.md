# Sales and Purchase Order Integration

PrintVis includes standard integrations with sales quotes, sales orders, purchase quotes, and purchase orders that can be enabled.

## Sales Order Integration

Sales Order Integration connects sales quotes and sales orders with PrintVis cases.

### Setup

On the **PrintVis General Setup** page, enable **Sales Order Integration**.

![Sales Order Integration setup](./assets/SOI1.png)

Once enabled, additional PrintVis fields appear on the sales lines, and a **PrintVis Jobs** section appears below the sales lines section.

The Jobs section displays the jobs belonging to the case connected to the selected sales line.

### Item Setup

On the **Item Card**, the **PrintVis Finished Goods** section contains a checkbox called **Sales Order Auto Create Case**.

![Sales Order Auto Create Case on the Item Card](./assets/SOI2.png)

Select this checkbox to create a PrintVis case automatically whenever the item is added to a sales quote or sales order.

This option can be used for items that are always produced rather than taken from inventory.

### Usage

![PrintVis fields on a sales order](./assets/SOI3.png)

Select **PrintVis Case** on the sales line to create a PrintVis case using the line’s item number and quantity.

The PrintVis quote or order number appears on the line, and the Jobs section displays the corresponding case jobs.

To open the complete PrintVis case, use the action on the **PrintVis** tab in the sales line menu.

## Purchase Order Integration

Purchase Order Integration is typically used for stock items that are planned through purchasing processes but produced internally.

For example, when an item reaches its minimum stock level, the requisition worksheet may suggest creating a purchase order. Instead of sending that order to an external supplier, you can use the purchase line to create a PrintVis case for internal production.

The produced items can then be received into stock and used to fulfill future sales or inventory requirements.

### Setup

1. Open **PrintVis Feature Management**.
2. Enable the purchase order creation feature.
3. If the feature is missing, run **Initialize Features** on the page.

### Usage

Follow these steps to create a PrintVis case from a purchase order line:

1. Create a new purchase order.
2. Add a purchase line for an item with a valid PrintVis template assigned.
3. Review the customer number. If a customer is preset on the Item Card, that customer appears by default on the purchase line. Keep or change it as needed.
4. Enable **PrintVis Case** on the purchase line. A new PrintVis case is created for the selected customer.
5. Review the additional PrintVis fields, including the **PrintVis order number** and **PrintVis status code**. These fields update to show that the purchase line is linked to a PrintVis case.

### Important Notes

- When Purchase Order Integration is disabled, purchase orders follow standard purchasing behaviour.
- When the integration is enabled, purchase orders still follow standard purchasing behaviour unless you select **PrintVis Case** on a purchase line.
- For the internal production workflow described here, the purchase order is not received or invoiced. It can be deleted after production has been released into inventory from the case.
- The integration provides an additional way to create internal production from purchase demand or a manually created purchase order.
- The quality of the created PrintVis case depends on the item setup and its assigned template.