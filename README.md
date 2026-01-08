# Linkedin-Front-End Clone Dashboard
Developed a LinkedIn front-end clone using HTML, CSS, and JavaScript to practice modern web design and layout structuring.
The project replicates the core UI, including the navigation bar and login/signup interface, with basic interactivity using JavaScript. 
This helped me strengthen my front-end skills and understand real-world website design.
Code for this is below:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>LinkedIn Login</title>
</head>

<body>

<!-- ================= HTML ================= -->

<header class="header">
    <h1 class="logo">Linked<span>in</span></h1>
</header>

<div class="left">
    <h2>Welcome to your professional<br>
         community</h2>
</div>

<div class="right">

    <!-- Login Form -->
    <div class="form active" id="loginForm">
        <h3>Sign in</h3>

        <input type="email" placeholder="Email or phone number">
        <input type="password" placeholder="Password">

        <a href="#" class="forgot">Forgot password?</a>

        <button class="primary-btn">Sign in</button>

        <p class="divider">or</p>

        <button class="google-btn">Sign in with Google</button>

        <p class="switch">
            New to LinkedIn?
            <span onclick="showSignup()">Join now</span>
        </p>
    </div>

    <!-- Signup Form -->
    <div class="form" id="signupForm">
        <h3>Make the most of your professional life</h3>

        <label>Email or phone number</label>
        <input type="email">

        <label>Password (6+ characters)</label>
        <input type="password">

        <button class="primary-btn">Agree & Join</button>

        <p class="divider">or</p>

        <button class="google-btn">Continue with Google</button>

        <p class="switch">
            Already on LinkedIn?
            <span onclick="showLogin()">Sign in</span>
        </p>
    </div>

</div>

<!-- ================= CSS ================= -->
<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

body {
    background: whitesmoke;
}

/* Header */
.header {
    padding: 20px 40px;
}

.logo {
    font-size: 34px;
    font-weight: bold;
    color: royalblue;
    text-align: center;
}

.logo span {
    background: royalblue;
    color: white;
    padding: 2px 6px;
    border-radius: 4px;
}

/* Welcome text */
.left {
    text-align: center;
    margin: 20px 0;
    text-decoration-color: black;
}

.left h2 {
    font-size: 36px;
    font-weight: normal;
    color: black;
    animation: fadeIn 1s;
}

/* Form box */
.right {
    width: 400px;
    background: white;
    margin: auto;
    padding: 25px;
    border-radius: 8px;
    box-shadow: 0 6px 15px gray;
}

/* Forms */
.form {
    display: none;
    animation: slideUp 0.5s;
}

.form.active {
    display: block;
}

h3 {
    margin-bottom: 15px;
}

/* Inputs */
input {
    width: 100%;
    padding: 12px;
    margin: 8px 0;
    border: 1px solid lightgray;
    border-radius: 4px;
}

input:focus {
    border-color: royalblue;
    outline: none;
}

/* Buttons */
.primary-btn {
    width: 100%;
    padding: 12px;
    background: royalblue;
    color: white;
    border: none;
    border-radius: 25px;
    font-size: 16px;
    cursor: pointer;
}

.primary-btn:hover {
    background: dodgerblue;
}

.google-btn {
    width: 100%;
    padding: 12px;
    background: white;
    color: royalblue;
    border: 1px solid royalblue;
    border-radius: 25px;
    cursor: pointer;
}

/* Text & links */
.forgot {
    display: block;
    margin: 10px 0;
    color: royalblue;
    text-decoration: none;
}

.divider {
    text-align: center;
    margin: 15px 0;
    color: gray;
}

.switch {
    text-align: center;
    margin-top: 15px;
}

.switch span {
    color: royalblue;
    font-weight: bold;
    cursor: pointer;
}


</style>

<!-- ================= JavaScript ================= -->
<script>
function showSignup() {
    document.getElementById("loginForm").classList.remove("active");
    document.getElementById("signupForm").classList.add("active");
}

function showLogin() {
    document.getElementById("signupForm").classList.remove("active");
    document.getElementById("loginForm").classList.add("active");
}
</script>

</body>
</html>
