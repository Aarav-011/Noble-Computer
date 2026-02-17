<html>
<head>
  <base target="_top">
  <title>Noble Computer | Feedback Form</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="format-detection" content="telephone=no">
  <link rel="icon" type="image/png" href="favicon_io/favicon-32x32.png">

  
  <link href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/css/bootstrap.min.css" rel="stylesheet">
  <link href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap-icons/1.11.1/font/bootstrap-icons.min.css" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
  
  <style>
    :root {
  --primary-green: #006466;        /* Main teal */
  --primary-green-dark: #004F4A;  /* Dark teal */
  --primary-green-light: #2BB3B1; /* Soft teal highlight */

  --secondary-green: #F4B400;     /* Logo yellow */
  --accent-green: #FFD966;        /* Light yellow */

  --success-green: #004F4A;

  --bg-green: #F3EDED;            /* Logo background */
  --border-green: #CFE8E6;

  --text-dark: #1F2937;
  --text-muted: #6B7280;
  --white: #FFFFFF;

  --shadow-light: rgba(0, 100, 102, 0.15);
  --shadow-medium: rgba(0, 100, 102, 0.3);

  --gradient-primary: linear-gradient(135deg, #006466 0%, #004F4A 100%);
  --gradient-bg: linear-gradient(135deg, #F3EDED 0%, #FFFFFF 100%);
}

    * {
      box-sizing: border-box;
    }
    
    body {
      background: var(--gradient-bg);
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
      color: var(--text-dark);
      line-height: 1.6;
      min-height: 100vh;
      position: relative;
    }
    
    body::before {
      content: '';
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: 
        radial-gradient(circle at 20% 20%, rgba(16, 185, 129, 0.1) 0%, transparent 50%),
        radial-gradient(circle at 80% 80%, rgba(52, 211, 153, 0.1) 0%, transparent 50%),
        radial-gradient(circle at 50% 50%, rgba(167, 243, 208, 0.05) 0%, transparent 50%);
      pointer-events: none;
      z-index: -1;
    }
    
    .main-container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 2rem 1rem;
      position: relative;
      z-index: 1;
    }
    
    .form-card {
      background: var(--white);
      border: 1px solid var(--border-green);
      border-radius: 24px;
      box-shadow: 
        0 20px 25px -5px rgba(0, 0, 0, 0.1),
        0 10px 10px -5px rgba(0, 0, 0, 0.04),
        0 0 0 1px var(--shadow-light);
      padding: 3rem;
      margin-bottom: 2rem;
      position: relative;
      overflow: hidden;
    }
    
    .form-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 6px;
      background: var(--gradient-primary);
    }
    
    .header-section {
      text-align: center;
      margin-bottom: 3rem;
      position: relative;
    }
    
    .form-title {
      background: var(--gradient-primary);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      font-weight: 700;
      font-size: 2.5rem;
      margin-bottom: 0.5rem;
      letter-spacing: -0.02em;
    }
    
    .form-subtitle {
      color: var(--text-muted);
      font-size: 1.1rem;
      font-weight: 500;
      margin-bottom: 0;
    }
    
    .icon-badge {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 80px;
      height: 80px;
      background: var(--gradient-primary);
      border-radius: 50%;
      margin-bottom: 1.5rem;
      box-shadow: 0 10px 25px var(--shadow-medium);
    }
    
    .icon-badge i {
      font-size: 2rem;
      color: var(--white);
    }
    
    .form-section {
      margin-bottom: 2rem;
    }
    
    .section-title {
      color: var(--text-dark);
      font-weight: 600;
      font-size: 1.1rem;
      margin-bottom: 1.5rem;
      padding-bottom: 0.5rem;
      border-bottom: 2px solid var(--accent-green);
      position: relative;
    }
    
    .section-title::after {
      content: '';
      position: absolute;
      bottom: -2px;
      left: 0;
      width: 60px;
      height: 2px;
      background: var(--primary-green);
    }
    
    .form-label {
      font-weight: 600;
      color: var(--text-dark);
      margin-bottom: 0.75rem;
      font-size: 0.95rem;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }
    
    .form-label i {
      color: var(--primary-green);
      font-size: 1rem;
    }
    
    .form-control, .form-select {
      border: 2px solid #e5e7eb;
      border-radius: 12px;
      padding: 0.875rem 1.25rem;
      font-size: 1rem;
      font-weight: 500;
      transition: all 0.3s ease;
      background-color: var(--white);
      color: var(--text-dark);
      box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
    }
    
    .form-control:focus, .form-select:focus {
      border-color: var(--primary-green);
      box-shadow: 
        0 0 0 3px var(--shadow-light),
        0 4px 6px -1px rgba(0, 0, 0, 0.1);
      background-color: var(--white);
      transform: translateY(-1px);
    }
    
    .form-control.is-invalid, .form-select.is-invalid {
      border-color: #ef4444;
      background-color: #fef2f2;
      box-shadow: 0 0 0 3px rgba(239, 68, 68, 0.1);
    }
    
    .form-control.is-valid, .form-select.is-valid {
      border-color: var(--primary-green);
      background-color: var(--bg-green);
      box-shadow: 0 0 0 3px var(--shadow-light);
    }
    
    .input-group-text {
      background: var(--accent-green);
      border: 2px solid #e5e7eb;
      border-right: none;
      color: var(--success-green);
      font-weight: 600;
      border-radius: 12px 0 0 12px;
    }
    
    .input-group .form-control {
      border-left: none;
      border-radius: 0 12px 12px 0;
    }
    
    .input-group:focus-within .input-group-text {
      border-color: var(--primary-green);
      background: var(--secondary-green);
    }
    
    .btn-primary {
      background: var(--gradient-primary);
      border: none;
      border-radius: 16px;
      padding: 1rem 3rem;
      font-weight: 700;
      font-size: 1.1rem;
      transition: all 0.3s ease;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      box-shadow: 
        0 10px 15px -3px var(--shadow-medium),
        0 4px 6px -2px var(--shadow-light);
      position: relative;
      overflow: hidden;
    }
    
    .btn-primary::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
      transition: left 0.5s ease;
    }
    
    .btn-primary:hover {
      background: linear-gradient(135deg, var(--primary-green-dark) 0%, #047857 100%);
      transform: translateY(-2px);
      box-shadow: 
        0 20px 25px -5px var(--shadow-medium),
        0 10px 10px -5px var(--shadow-light);
    }
    
    .btn-primary:hover::before {
      left: 100%;
    }
    
    .btn-primary:active {
      transform: translateY(0);
    }
    
    .btn-primary:disabled {
      background: var(--text-light);
      transform: none;
      box-shadow: none;
      cursor: not-allowed;
    }
    
    .alert {
      border: none;
      border-radius: 16px;
      font-weight: 500;
      margin-top: 2rem;
      padding: 1.25rem 1.5rem;
      box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
    }
    
    .alert-success {
      background: var(--bg-green);
      color: var(--success-green);
      border-left: 4px solid var(--primary-green);
    }
    
    .alert-danger {
      background: #fef2f2;
      color: #991b1b;
      border-left: 4px solid #ef4444;
    }
    
    .required-asterisk {
      color: #ef4444;
      margin-left: 2px;
      font-weight: 600;
    }
    
    .spinner-border-sm {
      width: 1.2rem;
      height: 1.2rem;
      margin-right: 0.5rem;
      border-width: 2px;
    }
    
    .invalid-feedback {
      font-weight: 500;
      font-size: 0.875rem;
      margin-top: 0.5rem;
    }
    
    .valid-feedback {
      color: var(--success-green);
      font-weight: 500;
      font-size: 0.875rem;
      margin-top: 0.5rem;
    }
    
    .loading-overlay {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: rgba(255, 255, 255, 0.9);
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 24px;
      z-index: 1000;
    }
    
    .loading-spinner {
      width: 50px;
      height: 50px;
      border: 4px solid var(--accent-green);
      border-top: 4px solid var(--primary-green);
      border-radius: 50%;
      animation: spin 1s linear infinite;
    }
    
    @keyframes spin {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }
    
    .form-submitted {
      animation: formSuccess 0.6s ease-out forwards;
    }
    
    @keyframes formSuccess {
      0% { transform: scale(1); }
      50% { transform: scale(1.02); }
      100% { transform: scale(1); }
    }
    
    @media (max-width: 768px) {
      .main-container {
        padding: 1rem 0.75rem;
      }
      
      .form-card {
        padding: 2rem 1.5rem;
        border-radius: 20px;
        margin-bottom: 1rem;
      }
      
      .form-title {
        font-size: 2rem;
      }
      
      .form-subtitle {
        font-size: 1rem;
      }
      
      .icon-badge {
        width: 60px;
        height: 60px;
        margin-bottom: 1rem;
      }
      
      .icon-badge i {
        font-size: 1.5rem;
      }
      
      .btn-primary {
        padding: 0.875rem 2rem;
        font-size: 1rem;
        width: 100%;
      }
      
      .form-control, .form-select {
        padding: 0.75rem 1rem;
        font-size: 1rem;
      }
      
      .section-title {
        font-size: 1rem;
      }
    }
    
    @media (max-width: 576px) {
      .form-card {
        padding: 1.5rem 1rem;
        border-radius: 16px;
      }
      
      .form-title {
        font-size: 1.75rem;
      }
      
      .header-section {
        margin-bottom: 2rem;
      }
      
      .icon-badge {
        width: 50px;
        height: 50px;
      }
      
      .icon-badge i {
        font-size: 1.25rem;
      }
    }
    
    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after {
        animation-duration: 0.01ms !important;
        animation-iteration-count: 1 !important;
        transition-duration: 0.01ms !important;
      }
    }
    
    @media (prefers-color-scheme: dark) {
      :root {
        --text-dark: #f9fafb;
        --text-muted: #d1d5db;
        --white: #1f2937;
        --bg-green: #064e3b;
        --border-green: #065f46;
      }
      
      body {
        background: linear-gradient(135deg, #111827 0%, #1f2937 100%);
      }
      
      .form-card {
        background: #374151;
        border-color: #4b5563;
      }
      
      .form-control, .form-select {
        background-color: #4b5563;
        border-color: #6b7280;
        color: #f9fafb;
      }
      
      .form-control:focus, .form-select:focus {
        background-color: #4b5563;
      }
    }
    
    .was-validated .form-control:invalid,
    .was-validated .form-select:invalid {
      border-color: #ef4444;
      background-color: #fef2f2;
    }
    
    .was-validated .form-control:valid,
    .was-validated .form-select:valid {
      border-color: var(--primary-green);
      background-color: var(--bg-green);
    }
  </style>
</head>
<body>
  <div class="main-container">
    <div class="form-card">
      <div class="header-section">
        <div class="icon-badge">
          <i class="bi bi-person-fill-add"></i>
        </div>
        <h1 class="form-title">Noble Computers</h1>
        <p class="form-subtitle">Student Feedback & Quality Review Form</p>
      </div>
      
      <form id="feedbackForm">
        <input type="hidden" name="fvv" value="1">
<input type="hidden" name="draftResponse" value="">
<input type="hidden" name="pageHistory" value="0">
<input type="hidden" name="fbzx" value="1271047527177834934">



        <!-- Student Info -->
        <div class="form-section">
          <h3 class="section-title">
            <i class="bi bi-person-circle me-2"></i>
            Student Information
          </h3>
      
          <div class="row g-4">
            <div class="col-md-4">
              <label class="form-label">
                <i class="bi bi-person"></i>
                Full Name<span class="required-asterisk">*</span>
              </label>
              <input type="text" name="entry.485428648" class="form-control" required placeholder="Enter your full name">
              <div class="invalid-feedback">Full name is required.</div>
            </div>
      
            <div class="col-md-4">
              <label class="form-label">
                <i class="bi bi-book"></i>
                Course Name<span class="required-asterisk">*</span>
              </label>
              <input type="text" name="entry.879531967" class="form-control" required placeholder="Enter course name">
              <div class="invalid-feedback">Course name is required.</div>
            </div>
      
            <div class="col-md-4">
              <label class="form-label">
                <i class="bi bi-person-badge"></i>
                Instructor Name<span class="required-asterisk">*</span>
              </label>
              <input type="text" name="entry.1757985765" class="form-control" required placeholder="Enter instructor name">
              <div class="invalid-feedback">Instructor name is required.</div>
            </div>
          </div>
        </div>
      
        <!-- Ratings -->
        <div class="form-section">
          <h3 class="section-title">
            <i class="bi bi-star-fill me-2"></i>
            Course Experience
          </h3>
      
          <div class="row g-4">
      
            <div class="col-md-6">
              <label class="form-label">Overall Teaching Quality<span class="required-asterisk">*</span></label>
              <select class="form-select" name="entry.1885014829" required>
                <option value="">Select</option>
                <option>Excellent</option>
                <option>Good</option>
                <option>Average</option>
                <option>Poor</option>
              </select>
              <div class="invalid-feedback">Please select a rating.</div>
            </div>
      
            <div class="col-md-6">
              <label class="form-label">Course Content Quality<span class="required-asterisk">*</span></label>
              <select class="form-select" name="entry.1796758144" required>
                <option value="">Select</option>
                <option>Excellent</option>
                <option>Good</option>
                <option>Average</option>
                <option>Poor</option>
              </select>
            </div>
      
            <div class="col-md-6">
              <label class="form-label">Lab / Practical Experience<span class="required-asterisk">*</span></label>
              <select name="entry.659421965" class="form-select" required>
                <option value="">Select</option>
                <option>Excellent</option>
                <option>Good</option>
                <option>Average</option>
                <option>Poor</option>
              </select>
            </div>
      
            <div class="col-md-6">
              <label name="entry.179318365" class="form-label">Would you recommend Noble Computers?<span class="required-asterisk">*</span></label>
              <select class="form-select" name="entry.179318365" required>
                <option value="">Select</option>
                <option>Yes</option>
                <option>Maybe</option>
                <option>No</option>
              </select>
            </div>
      
            <div class="col-12">
              <label class="form-label">
                <i class="bi bi-chat-dots"></i>
                Your Suggestions
              </label>
              <textarea name="entry.355701664" class="form-control" rows="4" placeholder="Write your suggestions here..."></textarea>
            </div>
      
          </div>
        </div>
      
        <!-- Submit -->
        <div class="row mt-5">
          <div class="col-12 text-center">
            <button type="submit" class="btn btn-primary btn-lg" id="submitBtn">
              <i class="bi bi-send me-2"></i>
              Submit Feedback
            </button>
          </div>
        </div>
      
      </form>

      <iframe name="hidden_iframe" style="display:none;"></iframe>

      
      <div id="messageDiv"></div>
      
      
      <div id="messageDiv"></div>
      
      
      <div id="messageDiv"></div>
    </div>
  </div>

  <script>
    const form = document.getElementById("feedbackForm");
    const messageDiv = document.getElementById("messageDiv");
    
    form.addEventListener("submit", function () {
      setTimeout(() => {
        messageDiv.innerHTML = `
          <div class="alert alert-success">
            ✅ Thank you! Your feedback has been submitted.
          </div>`;
        form.reset();
      }, 1000);
    });
    </script>

<script>
  document.getElementById("feedbackForm").addEventListener("submit", function(e){
    e.preventDefault();
  
    const form = e.target;
    const data = new FormData(form);
  
    fetch("https://docs.google.com/forms/u/0/d/e/1FAIpQLScOD8RR07LN2GKfrF-qKOq299-kvJKphif75x11Sr9E-NAMeQ/formResponse", {
      method: "POST",
      mode: "no-cors",
      body: data
    });
  
    // UI feedback
    document.getElementById("submitBtn").innerHTML = "✔ Submitted";
    document.getElementById("submitBtn").disabled = true;
  
    setTimeout(() => {
      form.reset();
      document.getElementById("submitBtn").innerHTML = "Submit Feedback";
      document.getElementById("submitBtn").disabled = false;
    }, 1000);
  });
  </script>
  
  

<iframe name="hidden_iframe" style="display:none;"></iframe>

    
</body>
</html>
