<script>
    // Track mobile menu state
    let mobileMenuOpen = $state(false);
    
    // Toggle mobile menu
    function toggleMobileMenu() {
      mobileMenuOpen = !mobileMenuOpen;
    }
    
    // Props for customization
    let { 
      logoUrl = '/images/logo.png',
      logoText = 'Saferaj',
      accentColor = '#059FEC'  // bright blue accent color like in template
    } = $props();
    
    // Navigation items
    const navItems = [
      { text: 'Home', href: '/' },
      { text: 'About', href: '/about' },
      { text: 'Services', href: '/services' },
      { text: 'Shop', href: '/shop' },
      { text: 'Blog', href: '/blog' },
      { text: 'Contact', href: '/contact' }
    ];
  </script>
  
  <!-- Main Navigation - Combining both top bar and navigation into a cleaner design -->
  <header class="bg-white py-4 shadow-md sticky top-0 z-50">
    <div class="container mx-auto px-4">
      <div class="flex justify-between items-center">
        <!-- Logo -->
        <div class="flex items-center">
          <a href="/" class="flex items-center">
            <span class="text-2xl font-bold">
              <span class="text-navy">S</span>aferaj
              <span class="text-accent">•</span>
            </span>
          </a>
        </div>
        
        <!-- Desktop Navigation Links -->
        <div class="hidden md:flex space-x-8">
          {#each navItems as item}
            <a 
              href={item.href} 
              class="text-gray-700 hover:text-accent font-medium transition duration-300 text-sm"
            >
              {item.text}
            </a>
          {/each}
        </div>
        
        <!-- Mobile Menu Button -->
        <div class="md:hidden">
          <button 
            class="text-navy hover:text-accent focus:outline-none"
            aria-label="Toggle menu"
            on:click={toggleMobileMenu}
          >
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d={mobileMenuOpen ? "M6 18L18 6M6 6l12 12" : "M4 6h16M4 12h16M4 18h16"} />
            </svg>
          </button>
        </div>
        
        <!-- CTA Button -->
        <div class="hidden md:block">
          <a href="/get-started" class="bg-accent hover:bg-accent-dark text-white font-medium py-2 px-6 rounded-md transition duration-300 text-sm">
            Get Started
          </a>
        </div>
      </div>
      
      <!-- Mobile Navigation Menu -->
      {#if mobileMenuOpen}
        <div class="md:hidden mt-4 py-2 border-t border-gray-200">
          <div class="flex flex-col space-y-3">
            {#each navItems as item}
              <a 
                href={item.href} 
                class="text-navy hover:text-accent font-medium transition duration-300 py-2"
                on:click={toggleMobileMenu}
              >
                {item.text}
              </a>
            {/each}
            <a href="/get-started" class="bg-accent hover:bg-accent-dark text-white font-medium py-2 px-4 rounded-md transition duration-300 text-center mt-3">
              Get Started
            </a>
          </div>
        </div>
      {/if}
    </div>
  </header>
  
  <style>
    /* Custom color variables based on the template */
    :root {
      --color-navy: #151c61;
      --color-accent: #059FEC;
      --color-accent-dark: #048AD0;
    }
    
    .text-navy {
      color: var(--color-navy);
    }
    
    .text-accent {
      color: var(--color-accent);
    }
    
    .bg-accent {
      background-color: var(--color-accent);
    }
    
    .bg-accent-dark {
      background-color: var(--color-accent-dark);
    }
    
    .hover\:text-accent:hover {
      color: var(--color-accent);
    }
    
    .hover\:bg-accent-dark:hover {
      background-color: var(--color-accent-dark);
    }
    
    /* Adding a slight animation for mobile menu */
    [class*="md:hidden"] > div {
      transition: max-height 0.3s ease-in-out, opacity 0.2s ease-in-out;
      overflow: hidden;
    }
    
    /* Logo styling */
    .logo-dot {
      display: inline-block;
      width: 6px;
      height: 6px;
      background-color: var(--color-accent);
      border-radius: 50%;
      margin-left: 2px;
    }
  </style>