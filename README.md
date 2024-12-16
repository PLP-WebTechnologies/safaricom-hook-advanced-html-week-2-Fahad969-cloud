### Assignment: Building a Multimedia Webpage and a Registration Form  

#### Objective: 
The goal of this assignment is to create a multimedia-rich webpage featuring audio and video elements and design a simple registration form with built-in HTML validation.  

---

### Part 1: Multimedia Webpage 
Create an HTML webpage that includes the following:  
1. **Audio Element**:  
   - Add an audio file using the `<audio>` tag.  
   - Provide controls to play, pause, and adjust the volume.  
   - Use at least one source format (e.g., `.mp3` or `.ogg`).  

2. **Video Element**:  
   - Add a video file using the `<video>` tag.  
   - Provide controls to play, pause, and adjust the volume.  
   - Include at least two source formats for compatibility (e.g., `.mp4` and `.webm`).  
   - Add a poster image that displays before the video plays.  

**Example Output:**  
A webpage where users can play an audio track and watch a video.  

---

### **Part 2: Registration Form **  
Design a user registration form with the following requirements:  

1. **Form Elements**:  
   - Full Name (Text input)  
   - Email Address (Input of type `email`)  
   - Password (Input of type `password`)  
   - Age (Input of type `number`, with a minimum value of 18)  
   - Gender (Radio buttons for Male, Female, Other)  
   - Terms and Conditions (Checkbox to agree before submitting)  

2. **Validation**:  
   - Use HTML5 validation attributes such as `required`, `min`, `maxlength`, etc.  
   - Ensure the email field has proper validation for email format.  
   - Make the password field require at least 8 characters.  

3. **Submit Button**:  
   - Include a "Register" button to submit the form.  

**Example Output:**  
A user-friendly registration form that prevents submission if required fields are not filled correctly.  

---

            ANSWERS(part1)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Multimedia Webpage</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f0f0f0;
            padding: 20px;
        }
        .media-container {
            margin: 20px 0;
        }
        audio, video {
            width: 80%;
            max-width: 600px;
        }
    </style>
</head>
<body>

    <h1>Welcome to the Multimedia Webpage</h1>

    <!-- Audio Element -->
    <div class="media-container">
        <h2>Audio Player</h2>
        <audio controls>
            <source src="your-audio-file.mp3" type="audio/mp3">
            <source src="your-audio-file.ogg" type="audio/ogg">
            Your browser does not support the audio element.
        </audio>
    </div>

    <!-- Video Element -->
    <div class="media-container">
        <h2>Video Player</h2>
        <video controls poster="your-poster-image.jpg">
            <source src="your-video-file.mp4" type="video/mp4">
            <source src="your-video-file.webm" type="video/webm">
            Your browser does not support the video element.
        </video>
    </div>

</body>
</html>

      ANSWERS(part2)

      <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>User Registration Form</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            background-color: #f4f4f9;
        }
        .container {
            max-width: 600px;
            margin: 0 auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            text-align: center;
        }
        label {
            font-weight: bold;
            display: block;
            margin: 10px 0 5px;
        }
        input[type="text"], input[type="email"], input[type="password"], input[type="number"], input[type="radio"], input[type="checkbox"] {
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        input[type="radio"] {
            width: auto;
            display: inline-block;
            margin-right: 10px;
        }
        input[type="checkbox"] {
            width: auto;
            display: inline-block;
        }
        button {
            background-color: #4CAF50;
            color: white;
            padding: 12px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            width: 100%;
        }
        button:hover {
            background-color: #45a049;
        }
        .form-group {
            margin-bottom: 20px;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Register</h1>
        <form action="#" method="POST" id="registrationForm">

            <!-- Full Name -->
            <div class="form-group">
                <label for="fullName">Full Name:</label>
                <input type="text" id="fullName" name="fullName" required maxlength="100" placeholder="Enter your full name">
            </div>

            <!-- Email Address -->
            <div class="form-group">
                <label for="email">Email Address:</label>
                <input type="email" id="email" name="email" required placeholder="Enter your email address">
            </div>

            <!-- Password -->
            <div class="form-group">
                <label for="password">Password:</label>
                <input type="password" id="password" name="password" required minlength="8" placeholder="Enter a password (min. 8 characters)">
            </div>

            <!-- Age -->
            <div class="form-group">
                <label for="age">Age:</label>
                <input type="number" id="age" name="age" required min="18" placeholder="Enter your age">
            </div>

            <!-- Gender -->
            <div class="form-group">
                <label>Gender:</label>
                <input type="radio" id="male" name="gender" value="male" required>
                <label for="male">Male</label>
                <input type="radio" id="female" name="gender" value="female" required>
                <label for="female">Female</label>
                <input type="radio" id="other" name="gender" value="other" required>
                <label for="other">Other</label>
            </div>

            <!-- Terms and Conditions -->
            <div class="form-group">
                <label>
                    <input type="checkbox" id="terms" name="terms" required>
                    I agree to the Terms and Conditions
                </label>
            </div>

            <!-- Submit Button -->
            <button type="submit">Register</button>
        </form>
    </div>

</body>
</html>





