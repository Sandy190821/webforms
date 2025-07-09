<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Sri Sai University Admission Form</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to right, #6a11cb, #2575fc);
      color: #333;
    }

    .container {
      max-width: 720px;
      margin: 50px auto;
      padding: 30px;
      background: #ffffff;
      border-radius: 16px;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
    }

    h1 {
      text-align: center;
      margin-bottom: 30px;
      color: #2c3e50;
    }

    .field {
      margin-bottom: 18px;
    }

    label {
      display: block;
      margin-bottom: 6px;
      font-weight: bold;
      color: #2d3436;
    }

    input[type="text"],
    input[type="email"],
    input[type="tel"],
    input[type="date"],
    select,
    textarea {
      width: 100%;
      padding: 10px 12px;
      border: 2px solid #ccc;
      border-radius: 8px;
      box-sizing: border-box;
      font-size: 15px;
      transition: all 0.3s ease;
    }

    input:focus,
    select:focus,
    textarea:focus {
      border-color: #6c5ce7;
      box-shadow: 0 0 8px rgba(108, 92, 231, 0.4);
      outline: none;
    }

    .inline-field {
      display: flex;
      gap: 20px;
    }

    .inline-field .field {
      flex: 1;
    }

    .submit-btn {
      display: block;
      width: 100%;
      padding: 14px;
      background: linear-gradient(to right, #00c6ff, #0072ff);
      color: white;
      font-size: 18px;
      font-weight: bold;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: background 0.3s ease;
      box-shadow: 0 0 15px rgba(0, 114, 255, 0.6);
    }

    .submit-btn:hover {
      background: linear-gradient(to right, #0072ff, #00c6ff);
      box-shadow: 0 0 25px rgba(0, 114, 255, 0.9);
    }

    @media (max-width: 600px) {
      .inline-field {
        flex-direction: column;
      }
    }
  </style>
</head>
<body>
<img src="sri".png>
  <div class="container">
    <h1>Sri Sai University Admission Form</h1>

    <form action="/submit_admission" method="post" enctype="multipart/form-data">
      <div class="inline-field">
        <div class="field">
          <label for="firstName">First Name</label>
          <input type="text" id="firstName" name="firstName" required>
        </div>
        <div class="field">
          <label for="lastName">Last Name</label>
          <input type="text" id="lastName" name="lastName" required>
        </div>
      </div>

      <div class="inline-field">
        <div class="field">
          <label for="dob">Date of Birth</label>
          <input type="date" id="dob" name="dob" required>
        </div>
        <div class="field">
          <label for="gender">Gender</label>
          <select id="gender" name="gender" required>
            <option value="">--Select--</option>
            <option>Female</option>
            <option>Male</option>
            <option>Other</option>
          </select>
        </div>
      </div>

      <div class="field">
        <label for="email">Email Address</label>
        <input type="email" id="email" name="email" required>
      </div>

      <div class="field">
        <label for="phone">Contact Number</label>
        <input type="tel" id="phone" name="phone" placeholder="+91-" pattern="[0-9]{10}" required>
      </div>

      <div class="field">
        <label for="address">Permanent Address</label>
        <textarea id="address" name="address" required></textarea>
      </div>

      <div class="field">
        <label for="course">Course Applying For</label>
        <select id="course" name="course" required>
          <option value="">--Select Course--</option>
          <option>B.Tech (Computer Science)</option>
          <option>B.Tech (Civil Engineering)</option>
          <option>BBA</option>
          <option>BCA</option>
          <option>MBA</option>
          <option>MCA</option>
          <option>M.Tech (CSE)</option>
        </select>
      </div>

      <div class="inline-field">
        <div class="field">
          <label for="yearPassed">Year of Passing</label>
          <input type="text" id="yearPassed" name="yearPassed" placeholder="e.g., 2024" pattern="[0-9]{4}" required>
        </div>
        <div class="field">
          <label for="percentage">Percentage / CGPA</label>
          <input type="text" id="percentage" name="percentage" placeholder="e.g., 78.5" required>
        </div>
      </div>

      <div class="field">
        <label for="marksheet">Upload Marksheet/Transcript</label>
        <input type="file" id="marksheet" name="marksheet" accept=".pdf,.jpg,.png" required>
      </div>

      <div class="field">
        <label for="achievements">Achievements / Extra-Curricular</label>
        <textarea id="achievements" name="achievements" placeholder="Optional"></textarea>
      </div>

      <button type="submit" class="submit-btn">Submit Application</button>
    </form>
  </div>
</body>
</html>

