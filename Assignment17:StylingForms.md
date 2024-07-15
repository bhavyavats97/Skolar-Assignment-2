<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Styled Form Elements</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            background-color: #f0f0f0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .form-container {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            width: 300px;
        }
        .form-container h1 {
            text-align: center;
            margin-bottom: 20px;
        }
        .form-container label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        .form-container input[type="text"],
        .form-container input[type="email"],
        .form-container input[type="password"],
        .form-container select,
        .form-container textarea {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
            transition: border-color 0.3s ease;
        }
        .form-container input:focus,
        .form-container select:focus,
        .form-container textarea:focus {
            border-color: #007BFF;
            outline: none;
        }
        .form-container input[type="checkbox"],
        .form-container input[type="radio"] {
            margin-right: 10px;
        }
        .form-container button {
            width: 100%;
            padding: 10px;
            background-color: #007BFF;
            color: white;
            border: none;
            border-radius: 4px;
            font-size: 16px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        .form-container button:hover {
            background-color: #0056b3;
        }
        .form-container .error {
            border-color: #FF0000;
        }
        .form-container .error-message {
            color: #FF0000;
            font-size: 12px;
            margin-top: -10px;
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
    <div class="form-container">
        <h1>Registration Form</h1>
        <form id="registrationForm">
            <label for="name">Name</label>
            <input type="text" id="name" name="name" required>
            <div class="error-message" id="nameError">Please enter your name.</div>

            <label for="email">Email</label>
            <input type="email" id="email" name="email" required>
            <div class="error-message" id="emailError">Please enter a valid email address.</div>

            <label for="password">Password</label>
            <input type="password" id="password" name="password" required>
            <div class="error-message" id="passwordError">Please enter your password.</div>

            <label for="gender">Gender</label>
            <input type="radio" id="male" name="gender" value="male">
            <label for="male">Male</label>
            <input type="radio" id="female" name="gender" value="female">
            <label for="female">Female</label>

            <label for="hobbies">Hobbies</label>
            <input type="checkbox" id="hobby1" name="hobbies" value="reading">
            <label for="hobby1">Reading</label>
            <input type="checkbox" id="hobby2" name="hobbies" value="traveling">
            <label for="hobby2">Traveling</label>
            <input type="checkbox" id="hobby3" name="hobbies" value="cooking">
            <label for="hobby3">Cooking</label>

            <label for="country">Country</label>
            <select id="country" name="country" required>
                <option value="">Select your country</option>
                <option value="usa">USA</option>
                <option value="canada">Canada</option>
                <option value="uk">UK</option>
            </select>
            <div class="error-message" id="countryError">Please select your country.</div>

            <label for="bio">Bio</label>
            <textarea id="bio" name="bio" rows="4" required></textarea>
            <div class="error-message" id="bioError">Please enter your bio.</div>

            <button type="submit">Submit</button>
        </form>
    </div>

    <script>
        document.getElementById('registrationForm').addEventListener('submit', function(event) {
            var valid = true;

            var name = document.getElementById('name');
            var nameError = document.getElementById('nameError');
            if (name.value === '') {
                name.classList.add('error');
                nameError.style.display = 'block';
                valid = false;
            } else {
                name.classList.remove('error');
                nameError.style.display = 'none';
            }

            var email = document.getElementById('email');
            var emailError = document.getElementById('emailError');
            if (email.value === '') {
                email.classList.add('error');
                emailError.style.display = 'block';
                valid = false;
            } else {
                email.classList.remove('error');
                emailError.style.display = 'none';
            }

            var password = document.getElementById('password');
            var passwordError = document.getElementById('passwordError');
            if (password.value === '') {
                password.classList.add('error');
                passwordError.style.display = 'block';
                valid = false;
            } else {
                password.classList.remove('error');
                passwordError.style.display = 'none';
            }

            var country = document.getElementById('country');
            var countryError = document.getElementById('countryError');
            if (country.value === '') {
                country.classList.add('error');
                countryError.style.display = 'block';
                valid = false;
            } else {
                country.classList.remove('error');
                countryError.style.display = 'none';
            }

            var bio = document.getElementById('bio');
            var bioError = document.getElementById('bioError');
            if (bio.value === '') {
                bio.classList.add('error');
                bioError.style.display = 'block';
                valid = false;
            } else {
                bio.classList.remove('error');
                bioError.style.display = 'none';
            }

            if (!valid) {
                event.preventDefault();
            }
        });
    </script>
</body>
</html>
