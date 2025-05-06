
<html lang="en">
  <style>
    :root {
    --main-bg-color: #f8f9fa;
    --main-text-color: #333;
    --sidebar-bg-color: #2c3e50;
    --sidebar-text-color: #ecf0f1;
    --accent-color: #3498db;
    --code-bg-color: #f1f1f1;
    --border-color: #ddd;
}

* {
    margin: auto;
    padding: auto;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    color: var(--main-text-color);
    background-color: var(--main-bg-color);
    display: flex;
    flex-direction: row;
}

/* Navigation sidebar */
#navbar {
    background-color: var(--sidebar-bg-color);
    color: var(--sidebar-text-color);
    width: 300px;
    height: 100vh;
    position: fixed;
    overflow-y: auto;
    transition: transform 0.3s ease;
}

#navbar header {
    font-size: 1.8rem;
    padding: 1.5rem;
    text-align: center;
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}

.nav-list {
    list-style: none;
}

.nav-link {
    display: block;
    padding: 1rem 1.5rem;
    color: var(--sidebar-text-color);
    text-decoration: none;
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
    transition: background-color 0.2s;
}

.nav-link:hover {
    background-color: rgba(255, 255, 255, 0.1);
}

.nav-link.active {
    background-color: var(--accent-color);
}

/* Mobile menu toggle */
#menu-toggle {
    display: none;
    position: fixed;
    top: 10px;
    right: 10px;
    z-index: 100;
    background-color: var(--accent-color);
    color: white;
    border: none;
    border-radius: 5px;
    padding: 0.5rem;
    cursor: pointer;
}

/* Main content */
#main-doc {
    margin-left: 300px;
    padding: 2rem;
    max-width: 100%;
}

.main-section {
    padding-bottom: 2rem;
    margin-bottom: 2rem;
    border-bottom: 1px solid var(--border-color);
}

.main-section:last-child {
    border-bottom: none;
}

.main-section header {
    font-size: 2rem;
    margin-bottom: 1.5rem;
    color: var(--accent-color);
}

p {
    margin-bottom: 1rem;
}

/* Code formatting */
pre {
    background-color: var(--code-bg-color);
    border-radius: 5px;
    padding: 1rem;
    overflow-x: auto;
    margin: 1rem 0;
}

code {
    font-family: 'Courier New', Courier, monospace;
    color:  #36827F;
    background-color: var(--code-bg-color);
    padding: 0.2rem 0.4rem;
    border-radius: 3px;
    white-space: nowrap;
    font-size: 20px;
}

/* Tables */
table {
    width: 99%;
    border-collapse: collapse;
    margin: 1rem 0;

}

th, td {
    padding: 0.75rem;
    text-align: left;
    border: 1px solid var(--border-color);
}

th {
    background-color: var(--accent-color);
    color: white;
}

/* Lists */
ul, ol {
    margin: 1rem 0 1rem 2rem;
}

li {
    margin-bottom: 0.5rem;
}

/* Media queries for responsive design */
@media screen and (max-width: 768px) {
    body {
        flex-direction: column;
    }
    
    #navbar {
        width: 100%;
        height: auto;
        max-height: 100vh;
        position: relative;
        transform: translateX(-100%);
        z-index: 10;
    }
    
    #navbar.active {
        transform: translateX(0);
    }
    
    #main-doc {
        margin-left: 0;
        padding: 1rem;
    }
    
    #menu-toggle {
        display: block;
    }
    
    .main-section header {
        font-size: 1.6rem;
    }
}

mark{
    background-color: var(--accent-color);
    color: white;
    padding: 0.1rem .1rem;
    border-radius: 3px;
}

u{
    width: 100%;
    text-decoration: underline;
    text-decoration-thickness: 2px;
}

.space{
    padding-top: 20px;
}

h2{
    font-size: 1.3rem;
    margin-bottom: 1rem;
    color:#00996b;
    font-weight: 350;
}

.back-to-top {
    position: fixed;
    bottom: 30px;
    right: 30px;
    z-index: 999;
    transform: translateY(100px);
    opacity: 0;
    visibility: hidden;
    transition: all 0.5s ease;
  }
  
  .back-to-top.show {
    transform: translateY(0);
    opacity: 1;
    visibility: visible;
  }
  
  .back-to-top-button {
    position: relative;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background: linear-gradient(135deg, #4a90e2, #7e57c2);
    border: none;
    color: white;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: all 0.3s ease;
    overflow: hidden;
  }
  
  .back-to-top-button:hover {
    transform: scale(1.1);
    box-shadow: 0 6px 20px rgba(0, 0, 0, 0.25);
  }
  
  .back-to-top-button:focus {
    outline: none;
  }
  
  .progress-indicator {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    background-color: rgba(255, 255, 255, 0.3);
    transition: height 0.3s ease;
  }
  
  .arrow-icon {
    position: relative;
    z-index: 2;
    transition: transform 0.3s ease;
    width: 18px;
    height: 18px;
  }
  
  .back-to-top-button:hover .arrow-icon {
    transform: translateY(-3px);
  }
    </style>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>RFLIB reviewer ni israel</title>
</head>
<body>
    <button id="menu-toggle">☰ Menu</button>
    
    <nav id="navbar">
        <header>RFLIB</header>
        <ul class="nav-list">
            <li><a class="nav-link active" href="#introduction">Checks Wihout Sufficient funds</a></li>
            <li><a class="nav-link" href="#getting_started">Evidence of Knowledge of insufficient funds</a></li>
            <li><a class="nav-link" href="#authentication">duty of the drawer</a></li>
            <li><a class="nav-link" href="#endpoints">Credit Construed</a></li>
            <li><a class="nav-link" href="#request_examples">Elements of the Offense</a></li>
            <li><a class="nav-link" href="#error_handling">Defenses in BP 22</a></li>
         
        </ul>
    </nav>
    
    <main id="main-doc">
        <section class="main-section" id="introduction">
            <header>Checks Wihout Sufficient funds</header>
            <p>Any person who <mark>draws or makes</mark> a check knowing he/she has <u>insufficient funds or lacks credit</u> will be penalized by the following:</p>
        <ul>
            <li>Check will be <mark>dishonored</mark></li>
            <li><mark>Imprisonment</mark> of not less than <u> 30 days</u> but not more than <u>1 year.</u></li>
            <li>or by a <mark>fine</mark> of not less than but not more than <u>double</u> the amount of the check issued which fine shall in no case exceed two hundred thousand pesos(P200,000).</li>
            <li>or <mark>both</mark> fine and imprisonmenmt at the <u>discretion</u> of the court.</li>
        </ul>
        <code>
            can be avoided if has <u> valid reason</u> or has <u>ordered the bank to stop payment</u>
        </code>

        <h2 class="space">Checks with Sufficient funds</h2>
<p>same penalty for the person who makes or draws a check with sufficient funds but:</p>
<ul>
    <li>Fails to keep enough funds for the payment.</li>
    <li>and the check is presented for payment within 90 days from it's date.</li>
    <li>but it bounces because of no funds.</ul>

        <h2 class="space">Who is liable:</h2>
<p>The person or persons who actually signed the check.</p>
<p>-even if they signed it on behalf of a corporation or company will be personally liable under BP22</p>
           
<h2 class="space">Example:</h2>
<p>Juan buys a pet dragon for P150,000 pesos but he knows he on has P10,000 pesos
    on his bank and no credit line but he issued a check anyways. When the seller tries to deposit 
    the check it bounces and gives the notice of dishonor but juan fails to make payments or arrangements within 5 banking days.
</p>
<ul>
    <li>Juan is liable for the check.</li>
    <li>Juan will be imprisoned for 30 days to 1 year.</li>
    <li>Juan will be fined double the amount but not exceeding P200,000</li>
    <li>or both imprisonment and fine at the discretion of the court.</li>
</ul>


        
        <section class="main-section" id="getting_started">
            <header>Evidence of Knowledge of insufficient funds</header>
            <p>If your check was presented to the bank within 90 days from the date of the check
                and it bounces due to insufficient funds it is <mark>prima facie</mark> Evidence
                that you knew you don't have enough funds to cover the check</p>
            
            
        </section>
        
        <section class="main-section" id="authentication">
            <header>Duty of the drawer</header>
            
            <h3>these are the duties of the drawer</h3>
            <ul>
                <li>when the cehck is presented but it bounces the bank must explain why.</li>
                <ul>
                    <li>the reason must be:</li>
                    <ul>
                        <li>written, printed, or stamped on the check or</li>
                        <li>attached to the check</li>
                </ul>
               
                <li>Explanation must be in plain language.</li> 
            </ul>
            <pre><code>If the reason is "insufficient funds or credit" that must always be <u>clearly</u> stated in the <mark>notice of hishonor</mark> or refusal.</code></pre>
            
            <h3>Why is it important?</h3>
            <p>Someone might try to escape <mark>criminal liability</mark> by <u>stopping payment</u> on a check to make it look like they hadfunds but just canceled the check for another reason.</p>
<p>This loophole was dimolished by making the bank clearly state the problem on the notice of dishonor.</p>
        
        
        <section class="main-section" id="endpoints">
            <header>Credit Construed</header>
            <p>Any <mark>agreement</mark> with the bank to deal with your payments.</p>
            <p>sila na bahala sa mga pinagbibili-bayadan mo ngalang later.</p>
            
            
        </section>
        
        <section class="main-section" id="request_examples">
            <header>Elements of the Offense</header>
            <ol>
                <li>A person makes, draws, and issues a check.</li>
                <li>The person knows that:</li>
                <ul>
                    <li>There are insufficient funds in the account.</li>
                    <li>There is no credit with the bank.</li>
                </ul>
                <li>The check is dishonored by the bank due to:</li>
                <ul>
                    <li>Insufficient funds.</li>
                    <li>No credit.</li>
                    <li>Would have been dishonored but for a stop-payment order without valid reason.</li>
                </ul>
                <li>Failure to pay the amount or arrange payment within 5 banking days after receiving the notice of dishonor.</li>
            </ol>
            <p>Once all these conditions are met, the one who issued the check can be criminally liable under BP 22.</p>
        </section>
        
        
        <section class="main-section" id="error_handling">
            <header>Defenses in BP 22</header>
            <ol>
                <li>Payment or arrangemennt within 5 banking days after receiving the notice of dishonor.</li>
                <li>Nop notice of dishonor.</li>
                <li>Check was not issued for value.</li>
                <li>Forgery</li>
               </ol>
        </section>

    
    
    
    
    <script>
        // Mobile menu toggle functionality
        const menuToggle = document.getElementById('menu-toggle');
        const navbar = document.getElementById('navbar');
        const navLinks = document.querySelectorAll('.nav-link');
        
        menuToggle.addEventListener('click', () => {
            navbar.classList.toggle('active');
        });
        
        // Close menu when a link is clicked (on mobile)
        navLinks.forEach(link => {
            link.addEventListener('click', () => {
                if (window.innerWidth <= 768) {
                    navbar.classList.remove('active');
                }
            });
        });
        
        // Highlight active section on scroll
        document.addEventListener('scroll', () => {
            const sections = document.querySelectorAll('.main-section');
            const scrollPosition = window.scrollY + 100;
            
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.offsetHeight;
                
                if (scrollPosition >= sectionTop && scrollPosition < sectionTop + sectionHeight) {
                    const currentId = section.getAttribute('id');
                    
                    navLinks.forEach(link => {
                        link.classList.remove('active');
                        if (link.getAttribute('href') === `#${currentId}`) {
                            link.classList.add('active');
                        }
                    });
                }
            });
        });
    </script>

<div class="back-to-top" id="backToTop">
    <button class="back-to-top-button" aria-label="Back to top">
      <div class="progress-indicator" id="scrollProgress"></div>
      <svg class="arrow-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <line x1="12" y1="19" x2="12" y2="5"></line>
        <polyline points="5 12 12 5 19 12"></polyline>
      </svg>
    </button>
  </div>
    <script>
        // Back to top button functionality
        const backToTopButton = document.getElementById('backToTop');
        const scrollProgress = document.getElementById('scrollProgress');
    
        window.addEventListener('scroll', () => {
            if (document.body.scrollTop > 100 || document.documentElement.scrollTop > 100) {
                backToTopButton.style.display = 'block';
            } else {
                backToTopButton.style.display = 'none';
            }
    
            // Update progress indicator
            const scrollHeight = document.documentElement.scrollHeight - document.documentElement.clientHeight;
            const scrollPosition = (document.documentElement.scrollTop / scrollHeight) * 100;
            scrollProgress.style.width = `${scrollPosition}%`;
        });
    
        backToTopButton.addEventListener('click', () => {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        });
</body>
</html>
