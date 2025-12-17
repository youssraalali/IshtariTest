Task 1.1 – Product Cost Field, Filtering & Sorting

* Added a new cost column to the products database table using SQL (via phpMyAdmin) and populated it with generated test values.
* Displayed the cost field in the Admin Product List view by:

  * Adding a new column to the product table
  * Rendering cost values for each product
  * Adding a filter input to allow filtering products by cost
* Implemented JavaScript logic for the cost filter input to:

  * Trim and store user input
  * Persist the filter value across requests
  * Append the filter parameter correctly to the URL
* Retrieved and stored the filter value in the product controller and ensured it was preserved in pagination and sorting URLs.
* Implemented server-side parsing of the filter input using preg_match, supporting comparison operators (>, <, >=, <=, =, !=).
* Added sorting support for the cost column by:

  * Defining a sortable column header in the product list view
  * Passing the sort and order parameters through the controller
  * Applying the sorting logic in the product model query
* Passed the parsed filter and sorting parameters through the $data and filter arrays to ensure consistent behavior across filtering, sorting, and pagination.

Files modified: Product list view, Product controller, Product model, Language files

---

Task 1.2 – Product Profit

* Added a calculated profit field (price − cost) to the product model query.
* Displayed the profit column in the Admin product list.
* Implemented filtering and sorting for the profit column same as for cost.

Files modified: Product list view, Product controller, Product model

---

Task 1.3

* Implement addCategoryWithParents() in the model.
* Integrate it within the addProduct() function.

Files modified: Product model

---

Task 1.4

* Implement two functions in the model: getCategoryId() and getCategoryFullPath().
* Use and pass them in the controller.

Files modified: Product model, Product controller, Product list view

---

Task 2.1

* Implement getProductCountByCategory() in the model.
* Use and pass it in the controller.
* Apply filtering (pre_match) and sorting in the controller.

Files modified: Category model, Category controller, Category list view

---

Task 2.2

* Implement getParentCategory() in the model.
* Use and pass it in the controller.

Files modified: Category model, Category controller, Category list view

---

Task 3

* Added “View Products” button in Orders page.

  * Controller fetches order products by ID and returns JSON.
  * Modal loads products dynamically via jQuery (researched to implement)

Challenges faced: I didn't know jQuery before, so I researched the AJAX part
