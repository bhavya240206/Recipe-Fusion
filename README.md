
# 🍽️ Recipe Ingredient Web Application
A comprehensive web application for managing and sharing recipes. Built using PHP, HTML, CSS, JavaScript, Bootstrap, Ajax, and MySQL, this application allows users to register, log in, add, edit, delete, and view recipes, with features such as ingredient lists, reviews, and ratings.

## 🌟 Features
- User registration and login 🔐
- Add new recipes 🆕
- Edit existing recipes ✏️
- Delete recipes ❌
- View recipes with detailed ingredients and instructions 👩‍🍳
- Search and filter recipes by category or name 🔍
- Review and rate recipes ⭐
- Responsive design using Bootstrap 📱💻
- AJAX for dynamic content updates ⚡

## 🛠️ Technologies Used
- **Frontend**: HTML, CSS, Bootstrap, JavaScript, jQuery
- **Backend**: PHP, MySQL
- **AJAX**: For seamless updates

## 📝 Setup Instructions
Follow these steps to set up the project locally:

### 1. Clone the Repository
```bash
git clone https://github.com/obadaKraishan/RecipeIngredientApp.git
cd RecipeIngredientApp
```

### 2. Set Up the Database
1. Start your local server using XAMPP, WAMP, or MAMP.
2. Open phpMyAdmin and create a new database named `recipe_ingredient`.
3. Import the SQL file to set up the tables:
   ```sql
   CREATE DATABASE recipe_ingredient;
   USE recipe_ingredient;

   CREATE TABLE users (
       id INT AUTO_INCREMENT PRIMARY KEY,
       username VARCHAR(255) NOT NULL UNIQUE,
       email VARCHAR(255) NOT NULL UNIQUE,
       password VARCHAR(255) NOT NULL,
       created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
   );

   CREATE TABLE recipes (
       id INT AUTO_INCREMENT PRIMARY KEY,
       title VARCHAR(255) NOT NULL,
       description TEXT NOT NULL,
       instructions TEXT NOT NULL,
       image VARCHAR(255) NOT NULL,
       category VARCHAR(255) NOT NULL,
       created_by INT NOT NULL,
       created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
       FOREIGN KEY (created_by) REFERENCES users(id)
   );

   CREATE TABLE ingredients (
       id INT AUTO_INCREMENT PRIMARY KEY,
       recipe_id INT NOT NULL,
       name VARCHAR(255) NOT NULL,
       quantity VARCHAR(255) NOT NULL,
       FOREIGN KEY (recipe_id) REFERENCES recipes(id)
   );

   CREATE TABLE reviews (
       id INT AUTO_INCREMENT PRIMARY KEY,
       recipe_id INT NOT NULL,
       user_id INT NOT NULL,
       rating INT NOT NULL,
       comment TEXT,
       created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
       FOREIGN KEY (recipe_id) REFERENCES recipes(id),
       FOREIGN KEY (user_id) REFERENCES users(id)
   );
   ```

### 3. Run the Application
Open a web browser and navigate to `http://localhost/RecipeIngredientApp`.

## 🎨 Customization

### 1. Update Styles
Modify the styles in `/css/style.css` to match your design preferences.

### 2. Update JavaScript
Enhance the JavaScript functionality in `/js/script.js` to customize the interactivity.

### 3. Update Content
Modify the HTML content in `index.php` to personalize the text and recipes.

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Contributors

- [Obada Kraishan](https://github.com/obadaKraishan)
![Image](https://github.com/user-attachments/assets/808c37c8-3dec-49f5-8e24-4a89fa4ec423)

![Image](https://github.com/user-attachments/assets/a9dd3496-3262-40df-a623-f74dd2bd660e)

![Image](https://github.com/user-attachments/assets/23f82291-1937-4d10-8c24-9a45336b0342)

![Image](https://github.com/user-attachments/assets/fe170c94-4a17-4757-90bb-d917a8d9f7a7)

![Image](https://github.com/user-attachments/assets/ed8c8581-fea7-4708-9cc8-0c2c36ca4584)

![Image](https://github.com/user-attachments/assets/0f9b6cf4-b740-4833-9e4e-8eb23eef7bdd)

![Image](https://github.com/user-attachments/assets/34cda510-9c24-4343-8d40-8d1d9843572b)

