1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram. <br>
Ans -> <br>
  The product and product_category have a relationship on the "category_id" field of product table and "id" field of the product_category table. The attribute "category_id" of product table refers to the attribute "id" of product_category table. This indicates foreign key relation. Foreign key ensures referential integrity in which a field of one (refering) table refers to a primary field of another (refered) table.


2. How could you ensure that each product in the "Product" table has a valid category assigned to it?<br>
Ans -><br>
  While inserting a new product into product table, we make sure that the category details of the current product like category_name, category_desc already exist in the product_category table.<br>
  If the category details already exist, we fetch the "id" of the corresponding category_name for the current product, and then inserting the new product with the "category_id" equal to fetched "id" in the product table.<br>
  If the category does not exist, we first insert the category details of the product into product_category table and fetching the id of newly inserted category, then then inserting the new product with the "category_id" equal to fetched "id" in the product table.<br>
  Without the product_category details not present in the product_category table, no new product can be added to the product table.
