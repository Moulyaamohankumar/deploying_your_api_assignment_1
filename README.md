# **Lab Exercise: Working with ENV Variables**

## **🎯 Objectives**

This assignment focuses on:

- Understanding the importance of **Environment (ENV) variables**.
- Learning to use the **dotenv** package for managing these variables.
- Implementing a script that securely retrieves and utilizes ENV variables.
- Demonstrating knowledge through a recorded explanation video.
- Implementing environment-specific configurations in a Node.js application.

---

## **📚 Prerequisites**

Before starting, ensure you have:

- Basic knowledge of **JavaScript**.
- Familiarity with **terminal/command line** operations.
- Access to the provided **Stackblitz boilerplate code**.

---

## **🚀 Steps to Complete the Assignment**

### **Step 1: Install the dotenv Package**

Install the `dotenv` package using npm to help load ENV variables from a `.env` file into your application.

Run the following command:

```bash
npm install dotenv
```

---

### **Step 2: Require dotenv in Your File**

Include the `dotenv` package in your Node.js application by requiring it in your script.

```javascript
require('dotenv').config();
```

---

### **Step 3: Create an .env File**

Create a file named `.env` in your project directory and add the following variables:

```plaintext
API_KEY=your_api_key_here
SERVER_SECRET=your_server_secret_here
IS_KALVIAN=true
```

Replace `your_api_key_here` and `your_server_secret_here` with actual values.

---

### **Step 4: Access Environment Variables**

Write a JavaScript script to retrieve and use these variables with the **dotenv** package.

Example implementation:

```javascript
// Load the dotenv package
require('dotenv').config();

// Access environment variables
const config = {
  apiKey: process.env.API_KEY,
  serverSecret: process.env.SERVER_SECRET,
  isKalvian: process.env.IS_KALVIAN === 'true',
};

// Export the config object
module.exports = config;

// Log the variables (Optional for testing)
console.log(config);
```

---

### **Step 5: Return Different Data Based on Environment Variables**

Modify your script to handle different environments dynamically.

Example:

```javascript
const environment = process.env.NODE_ENV || 'development';

const config = {
  apiKey: process.env.API_KEY,
  serverSecret: process.env.SERVER_SECRET,
  isKalvian: process.env.IS_KALVIAN === 'true',
  environment,
};

console.log(`Running in ${environment} mode`);
module.exports = config;
```

---

### **Step 6: Run the Script**

Execute the script to verify that the environment variables are loaded and accessible.

```bash
node <your_script_name>.js
```

You should see the environment variables printed in the console if everything is set up correctly.

---

## **🏁 Outcome**

By completing this exercise, you will:

- Understand how to manage and manipulate application configurations using environment variables.
- Learn how to handle different environments securely and with flexibility.
- Create a script that securely retrieves and uses ENV variables.
- Enhance the **security** and **flexibility** of your code by separating sensitive data from your source files.

---

## **📹 Video Recording Instructions**

To complete your submission, you need to record a video explaining the assignment.

### **Recording Guidelines:**

1. **Turn on your camera** – Ensure your camera is on throughout the recording.
2. **Share your entire screen** – Avoid sharing just a single tab or window.
3. **Use Google Meet** – Record using your kalvium.community email.
4. **Explain your code step by step** – Walk through your implementation and demonstrate understanding.
5. **Save and share the file** – Name the recording appropriately (e.g., `ENV_Variables_<YourName>`). Ensure the recording has view access for anyone with a kalvium.community email.

---

## **📤 Submission Guidelines**

Submit the following:

- **GitHub repository link** – Containing your completed code.
- **Recorded video link** – Explaining your implementation.

🎉 **Congratulations!** You've successfully implemented a secure environment variable management system using the **dotenv** package and completed the assignment!

