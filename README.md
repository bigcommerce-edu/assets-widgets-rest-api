# Widgets - REST API Code Assets

The assets in this repository support the BigCommerce Widgets - REST API training course.

## Contents

* `Widgets API Labs.postman_collection.json`: The Postman collection used in the course's REST API labs. It has folders for Regions, Widget Templates, Lab Widget Templates (the four example templates from the course), Widgets, and Placements.

## Setup

### Postman

1. Download `Widgets API Labs.postman_collection.json` from this repository.
2. In Postman, click **Import** and drop in the downloaded file.
3. Create a Postman environment for your store with the variables `store_hash` and `v3_token`, then select it before sending requests. The course's Getting Started lab walks through creating the API account and environment.

Your store's API account needs the **Content: Modify** scope.

### Widget Builder

Later labs use [Widget Builder](https://github.com/bigcommerce/widget-builder) rather than Postman. Setup instructions and the code for each widget template are in the [lab-widget-templates](https://github.com/bigcommerce-edu/lab-widget-templates) repository.

## Labs

### Regions

* **Lab - Regions**: Add a region to a theme template file in the control panel. Then try the **Get Regions in Template File** request in the **Regions** folder of the collection.

### Widget Templates

* **Lab - Widget Template**: Try the **Create Widget Template** request in the **Widget Templates** folder of the collection, then explore the other requests in that folder.

### Schema

* **Lab - Template with Static Content**: Try the **Create Static Image + Content Template** request in the **Lab Widget Templates** folder of the collection.
* **Lab - Widget Builder Setup** and **Lab - Schema Array**: Use the [hello-world](https://github.com/bigcommerce-edu/lab-widget-templates/tree/main/hello-world) and [product-grid](https://github.com/bigcommerce-edu/lab-widget-templates/tree/main/product-grid) templates in the lab repository.

### GraphQL

* **Lab - Template with Dynamic Data**: Use the [product-variant-list](https://github.com/bigcommerce-edu/lab-widget-templates/tree/main/product-variant-list) template in the lab repository. Your store needs at least one product with variants. The **Create Product Variant List Template** request in the **Lab Widget Templates** folder of the collection creates the same template.

### Widgets and Placements

Your store needs a widget template from an earlier lab to create widgets from.

* **Lab - Widgets**: Try the **Create Widget** request in the **Widgets** folder of the collection.
* **Lab - Placements**: Try the **Create Placement** request in the **Placements** folder of the collection. Placements require the region you added in the Regions lab.

## Resource Links

### Overview

* [Widgets API Overview](https://docs.bigcommerce.com/developer/docs/admin/widgets-and-scripts/guide)
* [API Accounts](https://docs.bigcommerce.com/developer/docs/overview/api-fundamentals/api-accounts)
* [Store API Accounts (Support Article)](https://support.bigcommerce.com/s/article/Store-API-Accounts)
* [Postman](https://www.postman.com/)
* [Page Builder (Support Article)](https://support.bigcommerce.com/s/article/Page-Builder)
* [Makeswift on Stencil](https://docs.makeswift.com/product/docs/guides/makeswift-on-stencil)

### Regions

* [Widgets API Overview](https://docs.bigcommerce.com/developer/docs/admin/widgets-and-scripts/guide)
* [Regions API Reference](https://docs.bigcommerce.com/developer/api-reference/rest/admin/content/regions)

### Widget Templates

* [Create a Widget Template](https://docs.bigcommerce.com/developer/api-reference/rest/admin/content/widgets)
* [Handlebars Helpers Reference](https://docs.bigcommerce.com/developer/docs/storefront/stencil/themes/context/handlebars-reference)
* [JSON Escape Tool](https://codebeautify.org/json-escape-unescape)

### Schema

* [Widget UI Input Types](https://docs.bigcommerce.com/developer/docs/storefront/stencil/themes/context/object-reference/elements)
* [Widget Builder](https://github.com/bigcommerce/widget-builder)
* [Lab Widget Templates](https://github.com/bigcommerce-edu/lab-widget-templates)

### GraphQL

* [GraphQL Storefront API Overview](https://docs.bigcommerce.com/developer/docs/storefront/guides/graphql-storefront-api)
* [Create Widgets Powered by GraphQL](https://docs.bigcommerce.com/developer/docs/admin/widgets-and-scripts/guide)

### Widgets and Placements

* [Widgets API Reference](https://docs.bigcommerce.com/developer/api-reference/rest/admin/content/widgets)
* [Page Builder (Support Article)](https://support.bigcommerce.com/s/article/Page-Builder)

### Conclusion

* [Developer Community](https://support.bigcommerce.com/s/group/0F913000000HLjECAW/bigcommerce-developers)
* [API Best Practices](https://docs.bigcommerce.com/developer/docs/overview/api-fundamentals/rate-limits)
* [Tools and Resources](https://docs.bigcommerce.com/developer/docs/overview/tools-and-sdks)
