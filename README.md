<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Profile Page</title>
</head>
<body style="font-family: Arial, sans-serif; margin: 20px; background-color: #f5f5f5;">

  <h1>My Profile</h1>

  <!-- Profile Picture Upload -->
  <label for="profilePic">Upload Profile Picture:</label><br>
  <input type="file" id="profilePic" accept="image/*"><br><br>
  <img id="preview" src="Internal storage/Pictures/100PINT/Pins/4b3c6c70e92c9fa7ed2beb8d1 361b917.jpg" alt="Profile Picture Preview" style="max-width:150px; display:none;">

  <hr>

  <!-- Profile Information -->
  <p><strong>First Name:</strong> yash</p>
  <p><strong>Last Name:</strong> singh </p>
  <p><strong>Hobbies:</strong> Gaming, Sports, Editing</p>
  <p><strong>Contact Number:</strong> 7878370377</p>
  <p><strong>Gmail Address:</strong> yashkhichi73@gmail.com</p>
  <p><strong>Country:</strong> India</p>
  <p><strong>Nationality:</strong> Hindu</p>
  <p><strong>Address:</strong>nagori gate,bagarchowk </p>

  <h2>About Me</h2>
  <p>
    I am a passionate learner who loves coding, technology, and creativity. 
    Always eager to explore new skills and improve myself every day.
  </p>

  <!-- Script to preview uploaded image -->
  <script>
    const profilePicInput = document.getElementById('profilePic');
    const preview = document.getElementById('preview');

    profilePicInput.addEventListener('change', function () {
      const file = this.files[0];
      if (file) {
        const reader = new FileReader();
        reader.onload = function (e) {
          preview.style.display = "block";
          preview.src = e.target.result;
        }
        reader.readAsDataURL(file);
      }
    });
  </script>

</body>
</html>