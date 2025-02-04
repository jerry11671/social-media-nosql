 # Social Media NoSQL Schema

## Project Overview
This project presents a NoSQL database schema for a social media application using MongoDB. The schema is designed to handle user profiles, posts (text, images, and videos), follow relationships, likes, comments, and feeds efficiently.

## Features
- User registration and profile management
- Creating and managing posts (text, images, videos)
- Following and unfollowing users
- Viewing a personalized feed
- Liking, commenting, and sharing posts

## Database Design (MongoDB)

### **Users Collection**
Stores user information and follow relationships.

```json
{
  "_id": "user_id",
  "username": "johndoe",
  "email": "johndoe@example.com",
  "profile_picture": "profile.jpg",
  "bio": "I love coding!",
  "followers": ["user_id_2", "user_id_3"],
  "following": ["user_id_4", "user_id_5"],
  "created_at": "2025-02-03T12:00:00Z"
}
```

### **Posts Collection**
Stores posts made by users.

```json
{
  "_id": "post_id",
  "user_id": "user_id",
  "content": "Hello, world!",
  "media": ["image1.jpg", "video1.mp4"],
  "likes": ["user_id_2", "user_id_3"],
  "comments": [
    {
      "user_id": "user_id_2",
      "comment": "Nice post!",
      "timestamp": "2025-02-03T12:05:00Z"
    }
  ],
  "shares": ["user_id_5"],
  "created_at": "2025-02-03T12:00:00Z"
}
```

### **Feed Collection**
Stores posts from followed users for quick access.

```json
{
  "_id": "user_id",
  "feed": [
    {
      "post_id": "post_id_1",
      "user_id": "user_id_2",
      "content": "New post!",
      "media": ["image2.jpg"],
      "timestamp": "2025-02-03T13:00:00Z"
    }
  ]
}
```

---

## API Endpoints

### **User Endpoints**
- `POST /users/register` → Register a new user
- `POST /users/login` → Authenticate user
- `GET /users/:id` → Get user profile
- `PUT /users/:id` → Update profile
- `POST /users/:id/follow` → Follow another user
- `POST /users/:id/unfollow` → Unfollow a user

### **Post Endpoints**
- `POST /posts` → Create a new post
- `GET /posts/:id` → Get a post by ID
- `DELETE /posts/:id` → Delete a post
- `POST /posts/:id/like` → Like a post
- `POST /posts/:id/unlike` → Unlike a post
- `POST /posts/:id/comment` → Comment on a post
- `POST /posts/:id/share` → Share a post

### **Feed Endpoint**
- `GET /users/:id/feed` → Get user feed

---

## Getting Started
### **Installation**
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/social-media-nosql.git
   ```
2. Navigate to the project directory:
   ```sh
   cd social-media-nosql
   ```

```

---

## Author
Developed by **Godson Jerry**

---

## License
This project is licensed under the MIT License.

