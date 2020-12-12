Personal Resume Page

Notable Features:

Light/Dark Mode-

CSS Root Styling for easy swapping

:root {

  --primary-color: rgb(255, 92, 92);
  
  --primary-variant: #ff2d2d;
  
  --secondary-color: #1b9999;
  
  --on-primary: rgb(250, 250, 250);
  
  --on-background: rgb(66, 66, 66);
  
  --on-background-alt: rgba(66, 66, 66, 0.7);
  
  --background: rgb(255, 255, 255);
  
  --box-shadow: 0 5px 20px 1px rgba(0, 0, 0, 0.5);
  
}

[data-theme="dark"] {

  --primary-color: rgb(150, 65, 255);
  
  --primary-variant: #6c63ff;
  
  --secondary-color: #03dac5;
  
  --on-primary: #000;
  
  --on-background: rgba(255, 255, 255, 0.9);
  
  --on-background-alt: rgba(255, 255, 255, 0.7);
  
  --background: #121212;
}


JS to swap between color schemes - 

// Toggle Dark and Light

function toggleDarkLightMode(isDark) {

    nav.style.backgroundColor = isDark ? 'rgb(0 0 0 / 50%)' : 'rgb(255 255 255 / 50%)';
    
    textBox.style.backgroundColor = isDark ? 'rgb(255 255 255 / 50%)' : 'rgb(0 0 0 / 50%)';
    
    toggleIcon.children[0].textContent = isDark ? 'Dark Mode' : 'Light Mode';
    
    isDark? toggleIcon.children[1].classList.replace('fa-sun', 'fa-moon') :
    
        toggleIcon.children[1].classList.replace('fa-moon', 'fa-sun');
        
    isDark ? imageMode('Dark') : imageMode('light');
}

// Switch Theme Dynamically

function switchTheme(event) {

    if (event.target.checked) {
    
        document.documentElement.setAttribute('data-theme', 'dark');
        
        localStorage.setItem('theme', 'dark');
        
        toggleDarkLightMode(true);
        
    } else {
    
        document.documentElement.setAttribute('data-theme', 'light');
        
        localStorage.setItem('theme', 'light');
        
        toggleDarkLightMode(false);
        
    }
}

Multiple Anchored Projects

Modal View for Resume

<!-- The Modal -->
        <div id="myModal" class="modal">

            <!-- The Close Button -->
            <span class="close">&times;</span>
        
            <!-- Modal Content (The Image) -->
            <img src="img\Resume.png" class="modal-content" id="img01">
        
            <!-- Modal Caption (Image Text) -->
            <div id="caption"></div>
            
        </div>

Mobile and Web Responsive
