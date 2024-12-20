# Job API Application 🛠️
A robust API for managing job listings, with a focus on security, scalability, and user authentication.

## Setup ⚙️

1. **Install Dependencies**  
   ```bash
   npm install
   ```

2. **Start the Application**  
   ```bash
   npm start
   ```

3. **Database Connection**     
   - Create a `.env` file in the root directory and add the `MONGO_URI` variable with your MongoDB connection string.

---

## Routers 🛣️

- **auth.js**: Handles user authentication, including registration and login.  
- **jobs.js**: Handles job-related operations such as creating, updating, and deleting job listings.

---

## User Model 👤

### Register User
- Validate `name`, `email`, and `password` using Mongoose.  
- Hash the password using `bcryptjs`.  

### Login User 
- Find the user in the database.  
- Compare passwords using `bcryptjs`.  
- If credentials are correct, generate a token.  

---

## Mongoose Errors ⚠️

- **Validation Errors**: Ensure all required fields meet validation rules.
- **Duplicate (Email)**: Handle unique constraints for email.
- **Cast Error**: Handle invalid IDs or malformed requests.

---

## Security 🔒

- **helmet**: Adds security-related HTTP headers.  
- **cors**: Enables cross-origin resource sharing.  
- **xss-clean**: Prevents cross-site scripting attacks.  
- **express-rate-limit**: Limits the number of requests to prevent abuse.

## Swagger UI 📜

Interactive API documentation available at `/api-docs`.  
