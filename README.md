# contactform
<!DOCTYPE html>
<html>
<head>
  <title>Contact Form</title>
  <style>
    .container {
      max-width: 400px;
      margin: 0 auto;
      padding: 20px;
      border: 1px solid #ccc;
      border-radius: 5px;
      background-color: #f2f2f2;
    }

    .container label {
      font-weight: bold;
    }

    .container input[type="text"],
    .container textarea {
      width: 100%;
      padding: 12px;
      border: 1px solid #ccc;
      border-radius: 4px;
      box-sizing: border-box;
      resize: vertical;
    }

    .container button[type="submit"] {
      background-color: #4CAF50;
      color: white;
      padding: 12px 20px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      float: right;
    }

    .container button[type="submit"]:hover {
      background-color: #45a049;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>Contact Form</h2>
    <form id="contactForm">
      <label for="name">Name</label>
      <input type="text" id="name" name="name" placeholder="Your name..">

      <label for="email">Email</label>
      <input type="text" id="email" name="email" placeholder="Your email..">

      <label for="message">Message</label>
      <textarea id="message" name="message" placeholder="Write something.." style="height:200px"></textarea>

      <button type="submit">Submit</button>
    </form>
  </div>

  <script>
    const contactForm = document.querySelector('#contactForm');

    contactForm.addEventListener('submit', function(event) {
      event.preventDefault();
      const formData = new FormData(this);

      // Now you can send the form data to your server using AJAX or any other method
      // For simplicity, let's just log the form data to the console
      for (let pair of formData.entries()) {
        console.log(pair[0] + ': ' + pair[1]);
      }
    });
  </script>
</body>
</html>
