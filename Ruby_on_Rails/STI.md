# Single Table Inheritance

While working on final project and deciding on how to set up my User/Admin/Customer relationships, I touched on STI.

Why not Single Table Inheritance? Because we don’t have multiple types of users, like VIP, Premium, Free, Student etc. to unite them in single table and need to retrieve data like reports.
Instead,  we have only one  customer and one user, so that we have separate classes/models for those. Admin model would not have is_admin:true/false.
