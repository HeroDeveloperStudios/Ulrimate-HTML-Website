<!DOCTYPE html>
<html>
<head>
  <title>Ultimate HTML Website</title>
  <style>
    /* CSS for loading animation */
    .loader {
      border: 16px solid #f3f3f3;
      border-top: 16px solid #3498db;
      border-radius: 50%;
      width: 120px;
      height: 120px;
      animation: spin 2s linear infinite;
      margin: 20px auto;
      display: none;
    }

    @keyframes spin {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }

    body {
      font-family: Arial, sans-serif;
      background-color: #f9f9f9;
      color: #333;
    }

    h1 {
      text-align: center;
      color: #555;
      padding-top: 40px;
    }

    .name {
      position: absolute;
      top: 10px;
      right: 10px;
      font-size: 14px;
      color: #777;
    }

    .button-container {
      display: flex;
      justify-content: center;
      margin: 40px auto;
    }

    .button-container button {
      margin: 0 10px;
      padding: 10px 20px;
      font-size: 16px;
      border: none;
      border-radius: 5px;
      color: #fff;
      cursor: pointer;
    }

    .button-container button:nth-child(1) {
      background-color: #ff8080;
    }

    .button-container button:nth-child(2) {
      background-color: #80b3ff;
    }

    .button-container button:nth-child(3) {
      background-color: #b3ffb3;
    }

    .button-container button:nth-child(4) {
      background-color: #ffcc99;
    }

    .info {
      display: none;
      margin: 20px auto;
      max-width: 600px;
      background-color: #fff;
      padding: 20px;
      border-radius: 5px;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    }

    .info h2 {
      color: #555;
      margin-top: 0;
    }

    .info p {
      line-height: 1.5;
    }

    .loader-container {
      text-align: center;
    }
  </style>
</head>
<body>
  <h1> HTML WEBSITE (STILL IN DEVELOPMENT) </h1>

  <div class="name">Website made by DheerajKumar.N, VIII B (RKM)</div>

  <div class="button-container">
    <button onclick="showInfo(1)">Introduction to Computer (Hardware) Basic</button>
    <button onclick="showInfo(2)">Computer Softwares</button>
    <button onclick="showInfo(3)">Introduction to HTML</button>
    <button onclick="showInfo(4)">HTML Colorful Texts and Types</button>
  </div>

  <div class="loader-container">
    <div id="loader" class="loader"></div>
  </div>

  <div id="info1" class="info">
    <h2>Introduction to Computer (Hardware) Basic</h2>
    <p>Computer hardware refers to the physical components of a computer system. It includes the central processing unit (CPU), motherboard, random access memory (RAM), storage devices (hard drive, solid-state drive), graphics card, sound card, and other peripherals like keyboard, mouse, and monitor. Understanding the basics of computer hardware is essential for building and troubleshooting computer systems.</p>
    <p>In this section, we will cover the key hardware components in detail. The CPU, often referred to as the brain of the computer, performs the majority of the processing tasks. The motherboard connects all the components together and facilitates communication between them. RAM stores the data and instructions that the CPU is currently using. Storage devices such as hard drives and solid-state drives are used to store data even when the computer is turned off. Graphics cards are responsible for rendering images and videos. Sound cards provide audio capabilities to the computer. Peripherals like keyboards, mice, and monitors allow users to interact with the computer.</p>
  </div>
  <div id="info2" class="info">
    <h2>Computer Softwares</h2>
    <p>Computer software refers to the programs and applications that run on a computer. In this section, we will explore different types of software and their functionalities.</p>
    <p>An operating system (OS) is the core software that manages computer hardware and provides a user interface. Windows, macOS, iOS, Android, and Linux (e.g., Ubuntu) are popular operating systems. Productivity software includes word processors, spreadsheets, presentation tools, and note-taking applications. Multimedia software allows users to create, edit, and play media content such as images, videos, and audio. Web browsers enable users to access and browse the World Wide Web. Games are software applications designed for entertainment and can range from simple puzzles to complex simulations.</p>
  </div>
  <div id="info3" class="info">
    <h2>Introduction to HTML</h2>
    <p>HTML (Hypertext Markup Language) is the standard markup language used to create web pages. It provides a structure for organizing and presenting content on the web. In this section, we will cover the fundamentals of HTML.</p>
    <p>HTML uses tags and elements to define the structure and layout of a web page. Headings (h1 to h6) are used to define the importance and hierarchy of text. Paragraphs (p) allow for the organization of textual content. Links (a) enable navigation between web pages. Lists (ul, ol) are used to create bulleted or numbered lists. Images (img) can be inserted into a web page. Tables (table) allow for the presentation of data in rows and columns. Forms (form) provide interactive elements for user input, such as text fields, checkboxes, and buttons.</p>
  </div>
  <div id="info4" class="info">
    <h2>HTML Colorful Texts and Types</h2>
    <p>In HTML, you can style your text in various ways to make it more visually appealing. CSS (Cascading Style Sheets) is used to apply styles to HTML elements. In this section, we will explore how to create colorful texts and different text types.</p>
    <p>With CSS, you can change the color of text by specifying the desired color value. You can also modify other text properties such as font size, font family, and font weight. Additionally, HTML offers different text types, such as headings (h1 to h6) that provide different levels of importance to text. You can also create emphasis using strong and emphasis tags. Furthermore, HTML supports inline styles and classes, allowing you to customize text styles according to your preferences.</p>
  </div>

  <script>
    function showInfo(id) {
      var infoDiv = document.getElementById("info" + id);
      var loaderDiv = document.getElementById("loader");

      // Show loading animation
      loaderDiv.style.display = "block";

      // Hide all other information divs
      var allInfoDivs = document.getElementsByClassName("info");
      Array.from(allInfoDivs).forEach(function(div) {
        if (div !== infoDiv) {
          div.style.display = "none";
        }
      });

      // Show selected information div after a delay (simulating loading)
      setTimeout(function() {
        infoDiv.style.display = "block";
        loaderDiv.style.display = "none";
      }, 2000);
    }
  </script>
</body>
</html>



