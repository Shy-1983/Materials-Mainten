<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1" />
<title>Air Conditioning Supplies - Home</title>
<style>
  /* Reset and base */
  * {
    box-sizing: border-box;
  }
  body, html {
    margin: 0; padding: 0; height: 100%;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: url('https://images.unsplash.com/photo-1602524817909-4291a55e63b6?auto=format&fit=crop&w=1280&q=80') no-repeat center center fixed;
    background-size: cover;
    color: #222;
  }
  header {
    background: rgba(255 255 255 / 0.9);
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 12px 20px;
    position: sticky;
    top: 0;
    z-index: 1000;
    box-shadow: 0 3px 7px rgb(0 0 0 / 0.2);
  }
  header nav a {
    margin: 0 12px;
    color: #007BFF;
    font-weight: 600;
    text-decoration: none;
    cursor: pointer;
    user-select: none;
  }
  header nav a:hover {
    text-decoration: underline;
  }
  header nav a.active {
    color: #0056b3;
    font-weight: 700;
  }
  #footer-info {
    font-size: 1.15rem;
    font-weight: 700;
    font-style: italic;
    color: #0056b3;
    text-align: center;
    text-shadow: 1px 1px 5px white;
    margin: 14px 4px;
  }
  main {
    max-width: 900px;
    margin: 12px auto 48px;
    padding: 0 12px;
  }
  h1, h2 {
    text-align: center;
    color: #004080;
    text-shadow: 0 0 8px #b0d0ff;
  }
  #content-area > * {
    max-width: 900px;
    margin: auto;
  }
  #boxes-container {
    margin-top: 16px;
    display: grid;
    grid-template-columns: repeat(auto-fit,minmax(180px,1fr));
    grid-gap: 12px;
    justify-content: center;
  }
  .colorful-box {
    background: linear-gradient(135deg, #0099ff, #33ccff);
    color: white;
    font-weight: 700;
    font-size: 0.85rem;
    padding: 18px 12px;
    border-radius: 10px;
    box-shadow: 0 3px 8px rgb(0 102 204 / 0.7);
    cursor: pointer;
    user-select: none;
    text-align: center;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }
  .colorful-box:hover, .colorful-box:focus {
    transform: scale(1.07);
    box-shadow: 0 6px 14px rgb(0 102 204 / 0.9);
    outline: none;
  }
  #signIn, #signUp {
    max-width: 360px;
    background: rgba(255 255 255 / 0.9);
    padding: 18px 20px;
    border-radius: 12px;
    box-shadow: 0 6px 18px rgba(0,0,0,0.2);
    margin: 16px auto 36px;
    display: none;
  }
  #signIn.active, #signUp.active {
    display: block;
  }
  form {
    display: flex;
    flex-wrap: wrap;
    flex-direction: column;
  }
  form label {
    margin-top: 12px;
    font-weight: 600;
    font-size: 0.9rem;
  }
  form input {
    padding: 10px;
    margin-top: 6px;
    border: 2px solid #007BFF;
    border-radius: 6px;
    font-size: 1rem;
  }
  form input:focus {
    border-color: #004080;
    outline: none;
    background-color: #f0f8ff;
  }
  button.submit-btn {
    margin-top: 20px;
    background-color: #0056b3;
    border: none;
    color: white;
    font-weight: 700;
    font-size: 1rem;
    cursor: pointer;
    padding: 12px;
    border-radius: 8px;
    box-shadow: 0 4px 12px #004080;
    transition: background-color 0.3s ease;
  }
  button.submit-btn:hover {
    background-color: #003580;
  }
  .error-msg {
    color: red;
    font-size: 0.9rem;
    margin-top: 6px;
  }

  /* Responsive */
  @media (max-width: 375px) {
    #boxes-container {
      grid-template-columns: repeat(auto-fit,minmax(140px,1fr));
    }
  }
</style>
</head>
<body>
<header>
  <nav>
    <a href="#" id="nav-home" class="active" aria-label="Home" tabindex="0">Home</a>
    <a href="#" id="nav-address" tabindex="0">Address</a>
    <a href="#" id="nav-search" tabindex="0">Search</a>
    <a href="#" id="nav-signin" tabindex="0">Sign In</a>
    <a href="#" id="nav-signup" tabindex="0">Sign Up</a>
  </nav>
</header>

<main>
  <section id="footer-info" aria-label="Company Contact Info" role="contentinfo">
    Contromoist Engineering Pvt Ltd<br />
    <span style="font-style: italic;">Shyamal Sutradhar</span><br />
    Ph: 7044497369<br />
    <a href="mailto:shyamal.sutradhar@contromoist.com" style="color:#003580;">shyamal.sutradhar@contromoist.com</a>
  </section>

  <!-- Sign In Form -->
  <section id="signIn" aria-live="polite" aria-labelledby="signin-title" role="region">
    <h2 id="signin-title">Sign In</h2>
    <form id="signin-form" novalidate>
      <label for="signin-email">Email</label>
      <input id="signin-email" name="signin-email" type="email" required autocomplete="username" />
      <label for="signin-password">Password</label>
      <input id="signin-password" name="signin-password" type="password" required autocomplete="current-password" />
      <div class="error-msg" id="signin-error"></div>
      <button type="submit" class="submit-btn">Sign In</button>
    </form>
  </section>

  <!-- Sign Up Form -->
  <section id="signUp" aria-live="polite" aria-labelledby="signup-title" role="region">
    <h2 id="signup-title">Sign Up</h2>
    <form id="signup-form" novalidate>
      <label for="signup-name">Full Name</label>
      <input id="signup-name" name="signup-name" type="text" required autocomplete="name" />
      <label for="signup-mail">Mail ID</label>
      <input id="signup-mail" name="signup-mail" type="email" required autocomplete="email" />
      <label for="signup-phone">Phone Number</label>
      <input id="signup-phone" name="signup-phone" type="tel" required autocomplete="tel" pattern="^(\+\d{1,3}[- ]?)?\d{10}$" placeholder="e.g. 1234567890" />
      <label for="signup-password">Password</label>
      <input id="signup-password" name="signup-password" type="password" required autocomplete="new-password" />
      <label for="signup-repeatpassword">Repeat Password</label>
      <input id="signup-repeatpassword" name="signup-repeatpassword" type="password" required autocomplete="new-password" />
      <div class="error-msg" id="signup-error"></div>
      <button type="submit" class="submit-btn">Register</button>
    </form>
  </section>

  <section id="content-area" tabindex="0" aria-label="Main items selection">
    <h2>Select Items</h2>
    <div id="boxes-container" role="list" aria-live="polite">
      <!-- Boxes inserted by JS -->
    </div>
  </section>
</main>

<script>
  const items = [
    "VRF Copper Pipe hard 1-1/8", "VRF Copper Pipe hard 7/8", "VRF Copper Pipe hard 3/4",
    "VRF Copper Pipe soft 5/8", "VRF Copper Pipe soft 1/2", "VRF Copper Pipe soft 3/8",
    "VRF Copper Pipe soft 1/4", "NON VRF Copper Pipe hard 1-1/8", "NON VRF Copper Pipe hard 7/8",
    "NON VRF Copper Pipe hard 3/4", "NON VRF Copper Pipe soft 5/8", "NON VRF Copper Pipe soft 1/2",
    "NON VRF Copper Pipe soft 3/8", "NON VRF Copper Pipe soft 1/4", "Brazing Sticks",
    "Insulation Tube 1-1/8 x 19mm", "Insulation Tube 7/8 x 19mm", "Insulation Tube 3/4 x 19mm",
    "Insulation Tube 5/8 x 13mm", "Insulation Tube 1/2 x 13mm", "Insulation Tube 3/8 x 13mm",
    "Insulation Tube 1/4 x 13mm", "PVC Drain Pipe 40mm", "PVC Drain Pipe 32mm", "PVC Drain Pipe 25mm",
    "PVC Drain Pipe 50mm", "PVC Drain Pipe 75mm", "PVC Drain Pipe 65mm", "PVC Elbow 32mm",
    "PVC Elbow 25mm", "PVC Socket 32mm", "PVC Socket 25mm", "PVC Tee 32mm", "PVC Tee 25mm",
    "PVC Reducer 32mmx40mm", "PVC Reducer 32mmx25mm", "PVC Solvent", "Copper Elbow 1-1/8",
    "Copper Socket 1-1/8", "Copper Elbow 7/8", "Copper Socket 7/8", "Copper Elbow 3/4",
    "Copper Socket 3/4", "Control Cable", "Supporting Items", "24swg GI Sheets", "22swg GI Sheets",
    "13mm Nitrile Plain Sheets", "13mm Nitrile FSK Sheets", "19mm Nitrile Plain Sheets",
    "19mm Nitrile FSK Sheets", "Accoustic Insulation", "Refnet", "Equipment"
  ];

  // Elements
  const signInSection = document.getElementById('signIn');
  const signUpSection = document.getElementById('signUp');
  const contentArea = document.getElementById('content-area');
  const navSignIn = document.getElementById('nav-signin');
  const navSignUp = document.getElementById('nav-signup');
  const navHome = document.getElementById('nav-home');

  // Boxes container
  const boxesContainer = document.getElementById('boxes-container');

  // Helper to clear active nav and sections
  function clearActive() {
    signInSection.classList.remove('active');
    signUpSection.classList.remove('active');
    contentArea.style.display = 'block';
    navHome.classList.remove('active');
    navSignIn.classList.remove('active');
    navSignUp.classList.remove('active');
  }

  // Show functions for navigation
  function showHome() {
    clearActive();
    contentArea.style.display = 'block';
    navHome.classList.add('active');
  }
  function showSignIn() {
    clearActive();
    signInSection.classList.add('active');
    contentArea.style.display = 'none';
    navSignIn.classList.add('active');
  }
  function showSignUp() {
    clearActive();
    signUpSection.classList.add('active');
    contentArea.style.display = 'none';
    navSignUp.classList.add('active');
  }

  navSignIn.addEventListener('click', (e) => {
    e.preventDefault();
    showSignIn();
  });
  navSignUp.addEventListener('click', (e) => {
    e.preventDefault();
    showSignUp();
  });
  navHome.addEventListener('click', (e) => {
    e.preventDefault();
    showHome();
  });

  // Build colorful boxes
  function createBoxes() {
    items.forEach((item, index) => {
      const box = document.createElement('div');
      box.className = 'colorful-box';
      box.setAttribute('role','listitem');
      box.setAttribute('tabindex','0');
      box.textContent = item;
      // Create URL safe item name for query
      const safeName = encodeURIComponent(item);
      box.addEventListener('click', () => {
        window.location.href = `item.html?item=${safeName}`;
      });
      box.addEventListener('keypress', (e) => {
        if (e.key === "Enter" || e.key === " ") {
          e.preventDefault();
          box.click();
        }
      });
      boxesContainer.appendChild(box);
    });
  }

  // Form validation and dummy auth simulation

  // Sign In logic
  const signinForm = document.getElementById('signin-form');
  const signinError = document.getElementById('signin-error');

  signinForm.addEventListener('submit', (e) => {
    e.preventDefault();
    // Simple static dummy email/password for demo
    const email = e.target['signin-email'].value.trim();
    const password = e.target['signin-password'].value.trim();
    if(email === "" || password === "") {
      signinError.textContent = "Please fill in all fields.";
      return;
    }
    // For demo, accept any non-empty input
    signinError.textContent = "";
    alert("Sign in successful! You can now use the site.");
    showHome();
  });

  // Sign Up logic
  const signupForm = document.getElementById('signup-form');
  const signupError = document.getElementById('signup-error');

  signupForm.addEventListener('submit', (e) => {
    e.preventDefault();
    const fullName = e.target['signup-name'].value.trim();
    const email = e.target['signup-mail'].value.trim();
    const phone = e.target['signup-phone'].value.trim();
    const pass = e.target['signup-password'].value;
    const passRepeat = e.target['signup-repeatpassword'].value;
    signupError.textContent = "";
    if(!fullName || !email || !phone || !pass || !passRepeat){
      signupError.textContent = "Please fill in all fields.";
      return;
    }
    // Simple phone pattern check
    const phonePattern = /^(\+\d{1,3}[- ]?)?\d{10}$/;
    if(!phonePattern.test(phone)) {
      signupError.textContent = "Please enter a valid phone number (10 digits).";
      return;
    }
    if(pass !== passRepeat) {
      signupError.textContent = "Passwords do not match.";
      return;
    }
    // For demo: registration success alert & switch to sign in
    alert("Registration successful! Please sign in.");
    showSignIn();
  });

  createBoxes();
  showHome();
</script>

</body>
</html>

