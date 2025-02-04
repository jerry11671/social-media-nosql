# Analysis of Social Media NoSQL Schema

## 1. Understanding SQL vs NoSQL Databases

### **SQL (Relational) Databases**
SQL databases are structured and use predefined schemas with tables, rows, and columns. They follow ACID (Atomicity, Consistency, Isolation, Durability) principles, ensuring data integrity and consistency.

#### **Advantages:**
- Strong data consistency and integrity.
- Uses structured query language (SQL) for powerful querying.
- Suitable for applications that require complex transactions.

#### **Disadvantages:**
- Not easily scalable for large-scale, high-traffic applications.
- Requires predefined schema, making modifications more difficult.
- Performance bottlenecks when handling large volumes of unstructured data.

---

### **NoSQL (Non-Relational) Databases**
NoSQL databases are designed for scalability and flexibility. They do not use fixed schemas and can store data in various formats (document, key-value, column-family, or graph).

#### **Advantages:**
- Highly scalable (horizontal scaling for distributed data processing).
- Schema flexibility allows dynamic data structures.
- Optimized for high-speed transactions and large-scale applications.

#### **Disadvantages:**
- Does not strictly enforce ACID properties (eventual consistency model).
- Querying capabilities are not as powerful as SQL.
- Data duplication can occur due to denormalization.

---

## 2. Identifying Key Entities and Relationships

### **Key Entities Identified:**
Based on the requirements, the main entities in the social media app are:
- **Users** (Profiles, Followers, Following)
- **Posts** (Text, Images, Videos, Likes, Comments, Shares)
- **Feed** (Personalized user feed)

### **Entity Relationships:**
- **Users can create multiple posts.**
- **Users can follow other users to see their posts in their feed.**
- **Users can like, comment on, and share posts.**
- **A post belongs to one user but can have multiple likes and comments.**
- **A user’s feed is dynamically updated with posts from followed users.**

---

