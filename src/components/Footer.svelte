<script>
    // Props for customization
    let {
      companyName = "Quiety",
      logoUrl = "/images/logo-white.png",
      companyTagline = "Your Safety and Compliance Partner for the transportation industry. We provide comprehensive solutions to keep your fleet safe and compliant.",
      address = "Abbotsford, BC, Canada",
      email = "saferajbc@gmail.com",
      phone = "+1 (236) 622-4504",
      quickLinks = [
        { text: "About Us", url: "/about" },
        { text: "Our Services", url: "/services" },
        { text: "Driver Training", url: "/training" },
        { text: "Compliance Management", url: "/compliance" },
        { text: "Blog & News", url: "/blog" },
        { text: "Contact Us", url: "/contact" }
      ],
      serviceLinks = [
        { text: "Driver Training", url: "/services/driver-training" },
        { text: "DOT Audit Preparation", url: "/services/dot-audits" },
        { text: "CSA Score Management", url: "/services/csa-management" },
        { text: "Regulatory Compliance", url: "/services/compliance" },
        { text: "Safety Consulting", url: "/services/safety-consulting" },
        { text: "ELD Solutions", url: "/services/eld-solutions" }
      ]
    } = $props();
  
    // Current year for copyright
    const currentYear = new Date().getFullYear();
    
    // Form submission
    let email_input = $state("");
    
    function handleSubscribe() {
      // This would connect to your email service in a real implementation
      if (email_input && email_input.includes('@') && email_input.includes('.')) {
        alert(`Thank you for subscribing with ${email_input}! You'll receive our newsletter soon.`);
        email_input = "";
      } else {
        alert("Please enter a valid email address.");
      }
    }
  </script>
  
  <footer class="footer-section bg-primary text-white pt-16 pb-8 relative overflow-hidden">
    <!-- Background decoration elements -->
    <div class="absolute top-0 right-0 w-32 h-32 bg-white opacity-5 rounded-full -translate-y-1/2 translate-x-1/3"></div>
    <div class="absolute bottom-0 left-0 w-48 h-48 bg-secondary opacity-5 rounded-full translate-y-1/4 -translate-x-1/4"></div>
    <div class="absolute top-1/3 left-1/2 w-4 h-4 bg-white opacity-10 rounded-full"></div>
    <div class="absolute bottom-1/4 right-1/4 w-6 h-6 bg-secondary opacity-10 rounded-full"></div>
    
    <div class="container mx-auto px-4 relative z-10">
      <!-- Main Footer Content -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 mb-12">
        <!-- Company Info -->
        <div>
          <img src={logoUrl} alt="{companyName} Logo" class="h-10 mb-6">
          <p class="mb-6 text-gray-300 leading-relaxed">{companyTagline}</p>
          <div class="flex space-x-4">
            <a href="#" class="w-10 h-10 rounded-full bg-primary-dark flex items-center justify-center text-white hover:bg-secondary transition-all duration-300" aria-label="Facebook">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                <path d="M9.198 21.5h4v-8.01h3.604l.396-3.98h-4V7.5a1 1 0 0 1 1-1h3v-4h-3a5 5 0 0 0-5 5v2.01h-2l-.396 3.98h2.396v8.01Z" />
              </svg>
            </a>
            <a href="#" class="w-10 h-10 rounded-full bg-primary-dark flex items-center justify-center text-white hover:bg-secondary transition-all duration-300" aria-label="Twitter">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                <path d="M7.6 21.5c8.65 0 13.38-7.16 13.38-13.38 0-.2 0-.41-.01-.61A9.59 9.59 0 0 0 23 5.41c-.82.37-1.7.61-2.61.72a4.57 4.57 0 0 0 2-2.52c-.87.52-1.84.9-2.86 1.1a4.55 4.55 0 0 0-7.76 4.15a12.93 12.93 0 0 1-9.4-4.76a4.56 4.56 0 0 0 1.41 6.09a4.52 4.52 0 0 1-2.07-.57v.06c0 2.2 1.57 4.05 3.65 4.47a4.54 4.54 0 0 1-2.06.08a4.56 4.56 0 0 0 4.25 3.16a9.14 9.14 0 0 1-5.67 1.95a9.38 9.38 0 0 1-1.09-.06a12.87 12.87 0 0 0 6.97 2.05" />
              </svg>
            </a>
            <a href="#" class="w-10 h-10 rounded-full bg-primary-dark flex items-center justify-center text-white hover:bg-secondary transition-all duration-300" aria-label="LinkedIn">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                <path d="M6.5 8.5v10h-3v-10h3ZM5 6.5a1.5 1.5 0 1 1 0-3a1.5 1.5 0 0 1 0 3ZM13 8.5v10h-3v-10h3Zm3 10h3v-5.5c0-3.5-4-3-4 0V18.5h-3v-10h3v1.5c1.4-2.5 7-2.6 7 2.5v6Z" />
              </svg>
            </a>
            <a href="#" class="w-10 h-10 rounded-full bg-primary-dark flex items-center justify-center text-white hover:bg-secondary transition-all duration-300" aria-label="Instagram">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                <path d="M12 2c2.717 0 3.056.01 4.122.06c1.065.05 1.79.217 2.428.465c.66.254 1.216.598 1.772 1.153a4.908 4.908 0 0 1 1.153 1.772c.247.637.415 1.363.465 2.428c.047 1.066.06 1.405.06 4.122c0 2.717-.01 3.056-.06 4.122c-.05 1.065-.218 1.79-.465 2.428a4.883 4.883 0 0 1-1.153 1.772a4.915 4.915 0 0 1-1.772 1.153c-.637.247-1.363.415-2.428.465c-1.066.047-1.405.06-4.122.06c-2.717 0-3.056-.01-4.122-.06c-1.065-.05-1.79-.218-2.428-.465a4.89 4.89 0 0 1-1.772-1.153a4.904 4.904 0 0 1-1.153-1.772c-.248-.637-.415-1.363-.465-2.428C2.013 15.056 2 14.717 2 12c0-2.717.01-3.056.06-4.122c.05-1.066.217-1.79.465-2.428a4.88 4.88 0 0 1 1.153-1.772A4.897 4.897 0 0 1 5.45 2.525c.638-.248 1.362-.415 2.428-.465C8.944 2.013 9.283 2 12 2zm0 1.802c-2.67 0-2.986.01-4.04.059c-.976.045-1.505.207-1.858.344c-.466.182-.8.398-1.15.748c-.35.35-.566.684-.748 1.15c-.137.353-.3.882-.344 1.857c-.048 1.055-.058 1.37-.058 4.04c0 2.67.01 2.986.058 4.04c.045.977.207 1.505.344 1.858c.182.466.399.8.748 1.15c.35.35.684.566 1.15.748c.353.137.882.3 1.857.344c1.054.048 1.37.058 4.04.058c2.67 0 2.987-.01 4.04-.058c.976-.045 1.505-.207 1.858-.344c.466-.182.8-.398 1.15-.748c.35-.35.566-.684.748-1.15c.137-.353.3-.882.344-1.857c.048-1.055.058-1.37.058-4.04c0-2.67-.01-2.986-.058-4.04c-.045-.976-.207-1.505-.344-1.858a3.097 3.097 0 0 0-.748-1.15a3.098 3.098 0 0 0-1.15-.748c-.353-.137-.882-.3-1.857-.344c-1.054-.048-1.37-.058-4.04-.058zm0 3.063a5.135 5.135 0 1 1 0 10.27a5.135 5.135 0 0 1 0-10.27zm0 1.802a3.333 3.333 0 1 0 0 6.666a3.333 3.333 0 0 0 0-6.666zm6.538-3.11a1.2 1.2 0 1 1-2.4 0a1.2 1.2 0 0 1 2.4 0z"/>
              </svg>
            </a>
          </div>
        </div>
        
        <!-- Quick Links -->
        <div>
          <h3 class="text-xl font-bold mb-6 relative after:content-[''] after:absolute after:w-16 after:h-1 after:bg-secondary after:left-0 after:-bottom-2">Quick Links</h3>
          <ul class="space-y-3">
            {#each quickLinks as link}
              <li>
                <a href={link.url} class="text-gray-300 hover:text-white transition-all duration-300 flex items-center">
                  <svg class="w-3 h-3 mr-2 text-secondary" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M9 18L15 12L9 6" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                  </svg>
                  {link.text}
                </a>
              </li>
            {/each}
          </ul>
        </div>
        
        <!-- Services -->
        <div>
          <h3 class="text-xl font-bold mb-6 relative after:content-[''] after:absolute after:w-16 after:h-1 after:bg-secondary after:left-0 after:-bottom-2">Our Services</h3>
          <ul class="space-y-3">
            {#each serviceLinks as link}
              <li>
                <a href={link.url} class="text-gray-300 hover:text-white transition-all duration-300 flex items-center">
                  <svg class="w-3 h-3 mr-2 text-secondary" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M9 18L15 12L9 6" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                  </svg>
                  {link.text}
                </a>
              </li>
            {/each}
          </ul>
        </div>
        
        <!-- Contact Info -->
        <div>
          <h3 class="text-xl font-bold mb-6 relative after:content-[''] after:absolute after:w-16 after:h-1 after:bg-secondary after:left-0 after:-bottom-2">Contact Information</h3>
          <ul class="space-y-4">
            <li class="flex items-start">
              <div class="w-10 h-10 rounded-lg bg-primary-dark flex items-center justify-center mr-3 shrink-0">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-secondary" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                </svg>
              </div>
              <span class="text-gray-300">{address}</span>
            </li>
            <li class="flex items-center">
              <div class="w-10 h-10 rounded-lg bg-primary-dark flex items-center justify-center mr-3 shrink-0">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-secondary" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                </svg>
              </div>
              <span class="text-gray-300">{phone}</span>
            </li>
            <li class="flex items-center">
              <div class="w-10 h-10 rounded-lg bg-primary-dark flex items-center justify-center mr-3 shrink-0">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-secondary" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                </svg>
              </div>
              <span class="text-gray-300">{email}</span>
            </li>
            <li class="flex items-center mt-6">
              <a href="/contact" class="bg-white hover:bg-opacity-90 text-primary font-medium py-3 px-6 rounded-md transition-all duration-300">
                Get In Touch
              </a>
            </li>
          </ul>
        </div>
      </div>
      
      <!-- Newsletter -->
      <div class="rounded-lg bg-primary-dark p-8 mb-8">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
          <div>
            <h3 class="text-xl font-bold mb-3">Subscribe to Our Newsletter</h3>
            <p class="text-gray-300">Stay updated with the latest safety regulations and industry best practices.</p>
          </div>
          <div>
            <form class="flex flex-col sm:flex-row gap-3" on:submit|preventDefault={handleSubscribe}>
              <input 
                type="email" 
                placeholder="Your Email Address" 
                bind:value={email_input}
                class="px-4 py-3 rounded-md flex-grow focus:outline-none focus:ring-2 focus:ring-secondary text-gray-900"
                required
              >
              <button 
                type="submit" 
                class="bg-secondary hover:bg-secondary-dark text-white font-medium py-3 px-6 rounded-md transition-all duration-300"
              >
                Subscribe
              </button>
            </form>
          </div>
        </div>
      </div>
      
      <!-- Bottom Footer -->
      <div class="border-t border-gray-700 pt-8 mt-6">
        <div class="flex flex-col md:flex-row justify-between items-center">
          <p class="text-gray-400 text-sm mb-4 md:mb-0">&copy; {currentYear} {companyName}. All rights reserved.</p>
          <div class="flex space-x-6">
            <a href="/privacy-policy" class="text-gray-400 hover:text-white text-sm transition-all duration-300">
              Privacy Policy
            </a>
            <a href="/terms-of-service" class="text-gray-400 hover:text-white text-sm transition-all duration-300">
              Terms of Service
            </a>
            <a href="/sitemap" class="text-gray-400 hover:text-white text-sm transition-all duration-300">
              Sitemap
            </a>
          </div>
        </div>
      </div>
      
      <!-- Back to top button -->
      <div class="fixed bottom-8 right-8 z-50">
        <a 
          href="#top" 
          class="w-12 h-12 bg-secondary hover:bg-secondary-dark text-white rounded-full shadow-lg transition-all duration-300 flex items-center justify-center"
          aria-label="Back to top"
        >
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 10l7-7m0 0l7 7m-7-7v18" />
          </svg>
        </a>
      </div>
    </div>
  </footer>
  
  <style>
    /* Custom color variables */
    :root {
      --color-primary: #0b163f;
      --color-primary-dark: #070e29;
      --color-secondary: #3b82f6;
      --color-secondary-dark: #1d4ed8;
    }
    
    .bg-primary {
      background-color: var(--color-primary);
    }
    
    .bg-primary-dark {
      background-color: var(--color-primary-dark);
    }
    
    .bg-secondary {
      background-color: var(--color-secondary);
    }
    
    .bg-secondary-dark {
      background-color: var(--color-secondary-dark);
    }
    
    .text-primary {
      color: var(--color-primary);
    }
    
    .text-secondary {
      color: var(--color-secondary);
    }
    
    .focus\:ring-secondary:focus {
      --tw-ring-color: var(--color-secondary);
    }
    
    /* Container width control */
    .container {
      max-width: 1200px;
    }
    
    /* Smooth scroll for back to top button */
    html {
      scroll-behavior: smooth;
    }
    
    /* Add subtle gradient to the footer background */
    .footer-section {
      background: linear-gradient(to bottom, var(--color-primary) 0%, #0f1f4d 100%);
    }
    
    /* Transition effects */
    .transition-all {
      transition-property: all;
      transition-duration: 300ms;
    }
    
    /* Back to top button shadow */
    .shadow-lg {
      box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
    }
  </style>