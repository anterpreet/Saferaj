<script>
    // Props for customization
    let {
      title = "Your Safety and Compliance Partner",
      subtitle = "Saferaj provides comprehensive safety solutions for transportation fleets, reducing risks, ensuring regulatory compliance, and protecting your drivers and assets.",
      primaryButtonText = "Explore Solutions",
      primaryButtonLink = "/services",
      secondaryButtonText = "Get a Consultation",
      secondaryButtonLink = "/contact"
    } = $props();
  </script>
  
  <section class="hero-section relative bg-primary text-white py-20 md:py-28 overflow-hidden">
    <!-- Content Container -->
    <div class="container mx-auto px-4 relative z-10">
      <div class="grid grid-cols-1 md:grid-cols-2 items-center gap-8">
        <!-- Left Content (Text & Buttons) -->
        <div class="hero-content">
          <!-- Headline -->
          <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6 leading-tight">
            {title}
          </h1>
          
          <!-- Subtitle -->
          <p class="text-lg opacity-90 mb-8 max-w-xl">
            {subtitle}
          </p>
          
          <!-- Call to Action Buttons -->
          <div class="flex flex-wrap gap-4">
            <a 
              href={primaryButtonLink} 
              class="bg-white hover:bg-opacity-90 text-primary font-medium py-3 px-6 rounded-md transition duration-300"
            >
              {primaryButtonText}
            </a>
            <a 
              href={secondaryButtonLink} 
              class="flex items-center justify-center bg-transparent border-2 border-white/30 hover:border-white text-white font-medium py-3 px-6 rounded-md transition duration-300"
            >
              <span class="flex items-center">
                <span class="inline-flex items-center justify-center w-8 h-8 mr-2 rounded-full bg-white/20">
                  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-4 h-4">
                    <path d="M20 4h-3.17L15 2H9L7.17 4H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm-5 11.5V13H9v2.5L5.5 12 9 8.5V11h6V8.5l3.5 3.5-3.5 3.5z"/>
                  </svg>
                </span>
                {secondaryButtonText}
              </span>
            </a>
          </div>
          
          <!-- Stats highlight -->
          <div class="grid grid-cols-3 gap-4 mt-10">
            <div class="text-center">
              <div class="text-3xl font-bold text-secondary mb-1">95%</div>
              <div class="text-sm text-gray-300">Compliance Rate</div>
            </div>
            <div class="text-center">
              <div class="text-3xl font-bold text-secondary mb-1">1000+</div>
              <div class="text-sm text-gray-300">Fleets Protected</div>
            </div>
            <div class="text-center">
              <div class="text-3xl font-bold text-secondary mb-1">30%</div>
              <div class="text-sm text-gray-300">Accident Reduction</div>
            </div>
          </div>
        </div>
        
        <!-- Right Content (Image) -->
        <div class="hero-illustration hidden md:block relative">
          <div class="relative">
            <!-- Truck fleet safety image -->
            <img 
              src="https://images.unsplash.com/photo-1601584115197-04ecc0da31d7?ixlib=rb-4.0.3&auto=format&fit=crop&w=1200&h=800&q=80" 
              alt="Fleet Safety and Compliance" 
              class="w-full h-auto rounded-lg shadow-2xl"
            />
  
            <!-- Decorative elements for the image -->
            <div class="absolute -bottom-4 -right-4 w-full h-full border-4 border-secondary/30 rounded-lg -z-10"></div>
            
            <!-- Safety graphic overlay -->
            <div class="absolute top-0 left-0 w-full h-full bg-gradient-to-br from-primary/30 to-secondary/20 rounded-lg flex items-center justify-center">
              <!-- Overlay safety elements -->
              <div class="absolute top-6 right-6 bg-white/20 backdrop-blur-sm p-3 rounded-lg">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="#ffffff" class="w-8 h-8">
                  <path d="M12 1L3 5v6c0 5.55 3.84 10.74 9 12 5.16-1.26 9-6.45 9-12V5l-9-4zm0 10.99h7c-.53 4.12-3.28 7.79-7 8.94V12H5V6.3l7-3.11v8.8z"/>
                </svg>
              </div>
              
              <!-- Compliance check mark -->
              <div class="absolute bottom-6 left-6 bg-white/20 backdrop-blur-sm p-3 rounded-lg">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="#ffffff" class="w-8 h-8">
                  <path d="M9 16.17L4.83 12l-1.42 1.41L9 19 21 7l-1.41-1.41z"/>
                </svg>
              </div>
            </div>
            
            <!-- Certification badge -->
            <div class="absolute -top-5 -right-5 bg-secondary text-white p-3 rounded-full shadow-lg">
              <div class="relative">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-10 h-10">
                  <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 15l-5-5 1.41-1.41L10 14.17l7.59-7.59L19 8l-9 9z"/>
                </svg>
                <span class="absolute inset-0 flex items-center justify-center text-xs font-bold">DOT</span>
              </div>
            </div>
            
            <!-- Blue glow effect -->
            <div class="absolute -inset-0.5 bg-secondary opacity-20 blur-xl rounded-lg"></div>
          </div>
        </div>
      </div>
      
      <!-- Trusted by companies -->
      <div class="mt-16 text-center">
        <p class="text-sm text-gray-300 mb-6">TRUSTED BY TRANSPORTATION COMPANIES ACROSS NORTH AMERICA</p>
        <div class="flex justify-center flex-wrap gap-8 opacity-70">
          <div class="h-8 w-auto">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 80 24" fill="currentColor" class="h-full w-auto">
              <rect x="0" y="8" width="16" height="8" rx="2" />
              <rect x="20" y="5" width="18" height="14" rx="2" />
              <rect x="42" y="2" width="16" height="20" rx="2" />
              <rect x="62" y="6" width="18" height="12" rx="2" />
            </svg>
          </div>
          <div class="h-8 w-auto">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 80 24" fill="currentColor" class="h-full w-auto">
              <circle cx="12" cy="12" r="10" />
              <path d="M30 12 L40 2 L50 12 L40 22 Z" />
              <path d="M60 2 L70 2 L70 22 L60 22 Z" />
              <path d="M78 12 A 10 10 0 1 1 58 12 A 10 10 0 0 1 78 12 Z" />
            </svg>
          </div>
          <div class="h-8 w-auto">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 80 24" fill="currentColor" class="h-full w-auto">
              <path d="M10 4 L10 20 L20 20 L20 4 Z" />
              <path d="M25 4 L25 20 L35 20 L35 4 Z" />
              <path d="M40 4 L40 20 L50 20 L50 4 Z" />
              <path d="M55 4 L70 4 L70 12 L55 12 L55 20 L70 20" />
            </svg>
          </div>
          <div class="h-8 w-auto">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 80 24" fill="currentColor" class="h-full w-auto">
              <path d="M2 12 A 10 10 0 1 0 22 12 A 10 10 0 0 0 2 12 Z" />
              <path d="M30 2 L50 2 L50 22 L30 22 Z" />
              <path d="M58 2 L78 2 L78 22 L58 22 Z" />
            </svg>
          </div>
        </div>
      </div>
    </div>
    
    <!-- Geometric shapes/dots background elements -->
    <div class="absolute top-0 right-0 w-1/3 h-1/3 opacity-10">
      <div class="w-32 h-32 rounded-full bg-blue-300 absolute -top-16 -right-16"></div>
    </div>
    <div class="absolute bottom-0 left-0 w-1/2 h-1/2 opacity-10">
      <div class="w-48 h-48 rounded-full bg-blue-400 absolute -bottom-24 -left-24"></div>
    </div>
    <div class="absolute top-1/3 left-1/4 w-4 h-4 rounded-full bg-blue-200 opacity-30"></div>
    <div class="absolute bottom-1/4 right-1/3 w-6 h-6 rounded-full bg-blue-200 opacity-30"></div>
    
    <!-- Additional floating elements -->
    <div class="absolute top-1/2 right-1/5 w-3 h-3 rounded-full bg-secondary opacity-40"></div>
    <div class="absolute bottom-1/3 left-1/3 w-5 h-5 rounded-full bg-white opacity-20"></div>
  </section>
  
  <style>
    /* Custom color variables */
    :root {
      --color-primary: #0b163f;
      --color-secondary: #3b82f6;
    }
    
    .bg-primary {
      background-color: var(--color-primary);
    }
    
    .text-primary {
      color: var(--color-primary);
    }
    
    .text-secondary {
      color: var(--color-secondary);
    }
    
    .bg-secondary {
      background-color: var(--color-secondary);
    }
    
    .border-secondary\/30 {
      border-color: rgba(59, 130, 246, 0.3);
    }
    
    /* Add subtle gradient to the background */
    .hero-section {
      background: linear-gradient(135deg, var(--color-primary) 0%, #1a365d 100%);
    }
    
    /* Animation for floating elements */
    @keyframes float {
      0% { transform: translateY(0px); }
      50% { transform: translateY(-10px); }
      100% { transform: translateY(0px); }
    }
    
    .hero-illustration {
      animation: float 6s ease-in-out infinite;
    }
    
    /* Shadow for image */
    .shadow-2xl {
      box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5);
    }
    
    /* Container width control */
    .container {
      max-width: 1200px;
    }
    
    /* Backdrop blur */
    .backdrop-blur-sm {
      backdrop-filter: blur(4px);
    }
  </style>