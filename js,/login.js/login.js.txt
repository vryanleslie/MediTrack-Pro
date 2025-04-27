document.addEventListener('DOMContentLoaded', function() {
    const loginForm = document.querySelector('form');

    loginForm.addEventListener('submit', function(event) {
        event.preventDefault();
        
        const username = document.querySelector('#username').value;
        const password = document.querySelector('#password').value;

        // Perform basic client-side validation
        if(username && password) {
            alert("Logging in...");
            // Normally, here you would send data to server via AJAX or a form submit
            window.location.href = 'index.html';  // Redirect to dashboard (for now)
        } else {
            alert("Please enter both username and password.");
        }
    });
});
