Name: Inventory & Restocking Management System Database

Purpose:
	Manages product inventory, supplier information, restocking logs, and low-stock alerts.
	Tracks user roles (admin/employees) for system operations.

Key Database Tables:

• users: Stores usernames, passwords, and roles (admin/employee).

• suppliers: Holds supplier contact information (e.g., name, phone).

• products: Maintains product details (name, category, supplier link, with restock_threshold to trigger alerts.

• restocking_logs: Logs each restocking event, including the user who restocked and any discrepancies.

• stock_alerts: Records low-stock alerts and their status (pending/resolved).

Features:

• User Management: Enables admin vs. employee roles

• Supplier Linking: Each product can link to a supplier for easy reference

• Automatic Timestamps: last_updated, restocked_at, and generated_at columns track changes.

• Foreign Key Constraints: Maintains data integrity (e.g., cascade deletes on related rows).

• Stock Threshold Alerts: Sends or records an alert when product quantity falls below threshold.

Technologies:

• MySQL database engine using InnoDB.

• UTF8MB4 character set and collation (adjusted to utf8mb4_general_ci for wide compatibility).
