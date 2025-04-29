<script>
    // Props for customization
    let {
      companyName = "Saferaj",
      welcomeImage = "https://images.unsplash.com/photo-1600320254374-ce2d293c324e?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&h=400&q=80",
      servicesData = [
        {
          title: "Safe and Smart Driver Training",
          description: "Comprehensive training programs designed to create skilled, safety-conscious drivers for your fleet.",
          image: "https://images.unsplash.com/photo-1544620347-c4fd4a3d5957?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&h=400&q=80",
          link: "/services/driver-training"
        },
        {
          title: "MTO-DOT Audits",
          description: "Thorough preparation and representation for regulatory audits to ensure compliance and minimize risks.",
          image: "https://images.unsplash.com/photo-1517502884422-41eaead166d4?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&h=400&q=80",
          link: "/services/dot-audits"
        },
        {
          title: "CSA Administration Service",
          description: "Proactive management of your CSA scores to maintain favorable ratings and avoid compliance issues.",
          image: "https://images.unsplash.com/photo-1530309324784-b7c91108a8c8?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&h=400&q=80",
          link: "/services/csa-administration"
        }
      ]
    } = $props();
    
    // Progress metrics
    const progressMetrics = [
      { label: "Safety Tips", percentage: 85 },
      { label: "Driver Training", percentage: 90 },
      { label: "Core Values", percentage: 95 }
    ];
    
    // Core values
    const coreValues = [
      { 
        title: "Integrity", 
        description: "We maintain the highest standards of professional conduct and ethics in all of our business relationships.",
        icon: "M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z",
        background: "bg-primary-light"
      },
      { 
        title: "Understanding", 
        description: "We take time to understand each client's unique challenges and develop customized solutions that work.",
        icon: "M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z",
        background: "bg-secondary"
      },
      { 
        title: "Excellence", 
        description: "We strive for excellence in everything we do, continuously improving our processes and services to deliver superior results.",
        icon: "M9 12l2 2 4-4M7.835 4.697a3.42 3.42 0 001.946-.806 3.42 3.42 0 014.438 0 3.42 3.42 0 001.946.806 3.42 3.42 0 013.138 3.138 3.42 3.42 0 00.806 1.946 3.42 3.42 0 010 4.438 3.42 3.42 0 00-.806 1.946 3.42 3.42 0 01-3.138 3.138 3.42 3.42 0 00-1.946.806 3.42 3.42 0 01-4.438 0 3.42 3.42 0 00-1.946-.806 3.42 3.42 0 01-3.138-3.138 3.42 3.42 0 00-.806-1.946 3.42 3.42 0 010-4.438 3.42 3.42 0 00.806-1.946 3.42 3.42 0 013.138-3.138z",
        background: "bg-primary-light"
      },
      { 
        title: "Core Values", 
        description: "Our values form the foundation of our company culture and guide our decision-making processes and client interactions.",
        icon: "M13 10V3L4 14h7v7l9-11h-7z",
        background: "bg-secondary"
      }
    ];
  </script>
  
  <!-- Welcome Section -->
  <section class="py-16 bg-white" id="welcome">
    <div class="container mx-auto px-4">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
        <div class="order-2 lg:order-1">
          <div class="mb-4">
            <span class="text-secondary font-medium">About Us</span>
            <h2 class="text-3xl font-bold text-primary mt-2 mb-6">Welcome to {companyName}</h2>
          </div>
          <p class="text-gray-600 mb-6">{companyName} was established to provide value-creating safety and compliance solutions for companies seeking a safer and more compliant way to operate their transportation fleet.</p>
          <p class="text-gray-600 mb-8">We believe our experience and knowledge will not only improve your company's SAFETY RATING but will save your company substantial amounts on non-compliance fines, equipment costs, and the overall cost of managing a fleet by implementing proven safety protocols.</p>
          <a href="/about" class="inline-block bg-primary hover:bg-primary-dark text-white font-medium py-3 px-6 rounded-md transition duration-300">
            Learn More About Us
          </a>
        </div>
        <div class="order-1 lg:order-2">
          <div class="relative">
            <div class="absolute -top-4 -right-4 w-full h-full bg-primary rounded-lg"></div>
            <img src={welcomeImage} alt="Professional Truck Driver" class="rounded-lg shadow-lg w-full h-auto relative z-10">
            <div class="absolute -z-10 -bottom-3 -left-3 w-24 h-24 bg-secondary opacity-30 rounded-full"></div>
          </div>
        </div>
      </div>
    </div>
  </section>
  
  <!-- Vision & Mission -->
  <section class="py-16 bg-gray-50" id="vision-mission">
    <div class="container mx-auto px-4">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <div class="bg-white rounded-lg shadow-lg p-8 transform transition-all duration-300 hover:translate-y-[-10px]">
          <div class="flex items-center mb-6">
            <div class="w-14 h-14 flex items-center justify-center bg-blue-100 rounded-lg text-primary">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
              </svg>
            </div>
            <h3 class="text-2xl font-bold text-primary ml-4">Our Vision</h3>
          </div>
          <p class="text-gray-600">To excel in Safety & Compliance to a level that is compatible with excellence in other business parameters such as Quality, Productivity, and Profitability.</p>
        </div>
        
        <div class="bg-primary rounded-lg shadow-lg p-8 text-white transform transition-all duration-300 hover:translate-y-[-10px]">
          <div class="flex items-center mb-6">
            <div class="w-14 h-14 flex items-center justify-center bg-primary-dark rounded-lg text-white">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
              </svg>
            </div>
            <h3 class="text-2xl font-bold ml-4">Our Mission</h3>
          </div>
          <p>Our mission is to provide our clients with exceptional Safety & Compliance Management Services, Training, and Customer Service in the transportation industry.</p>
        </div>
      </div>
    </div>
  </section>
  
  <!-- Services Section -->
  <section class="py-16 bg-white" id="services">
    <div class="container mx-auto px-4">
      <div class="text-center mb-12">
        <span class="text-secondary font-medium">What We Do</span>
        <h2 class="text-3xl font-bold text-primary mt-2">Our Services</h2>
        <div class="w-20 h-1 bg-secondary mx-auto mt-4 mb-6"></div>
        <p class="text-gray-600 max-w-3xl mx-auto">Comprehensive safety and compliance solutions tailored to your fleet's specific needs.</p>
      </div>
      
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        {#each servicesData as service}
          <div class="bg-white rounded-lg shadow-lg overflow-hidden transition-all duration-300 hover:shadow-xl hover:translate-y-[-10px]">
            <div class="relative h-48 overflow-hidden">
              <img src={service.image} alt={service.title} class="w-full h-full object-cover transition-transform duration-500 hover:scale-110">
            </div>
            <div class="p-6">
              <h3 class="text-xl font-bold text-primary mb-3">{service.title}</h3>
              <p class="text-gray-600 mb-4">{service.description}</p>
              <a href={service.link} class="flex items-center justify-center w-full text-center bg-primary hover:bg-primary-dark text-white font-medium py-2 px-4 rounded-md transition duration-300">
                Learn More
                <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 ml-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3" />
                </svg>
              </a>
            </div>
          </div>
        {/each}
      </div>
      
      <div class="text-center mt-10">
        <a href="/services" class="inline-block bg-secondary hover:bg-secondary-dark text-white font-medium py-3 px-8 rounded-md transition duration-300">
          View All Services
        </a>
      </div>
    </div>
  </section>
  
  <!-- Excellence Section -->
  <section class="py-16 bg-gray-50 relative" id="excellence">
    <div class="container mx-auto px-4">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
        <div>
          <span class="text-secondary font-medium">Why Choose Us</span>
          <h2 class="text-3xl font-bold text-primary mt-2 mb-6">Proud to Deliver Excellence Every Time</h2>
          <p class="text-gray-600 mb-6">{companyName} takes pride in the fact that we have built our business from day one on trust, high ethical standards, and over-delivering on our promise to our broad list of clients. Surviving many peaks and valleys experienced by the transportation industry, {companyName}'s record of longevity is a testimonial to our underlying motto of "always putting clients' needs first".</p>
          
          <!-- Progress Bars -->
          <div class="space-y-6 mb-8">
            {#each progressMetrics as metric}
              <div>
                <div class="flex justify-between mb-2">
                  <span class="text-primary font-medium">{metric.label}</span>
                  <span class="text-secondary font-medium">{metric.percentage}%</span>
                </div>
                <div class="w-full bg-gray-200 rounded-full h-2.5">
                  <div class="bg-secondary h-2.5 rounded-full" style="width: {metric.percentage}%"></div>
                </div>
              </div>
            {/each}
          </div>
        </div>
        
        <div>
          <div class="relative">
            <div class="absolute -top-4 -left-4 w-full h-full bg-secondary opacity-20 rounded-lg"></div>
            <img 
              src="https://images.unsplash.com/photo-1586191582151-9ee5f5c42a9f?ixlib=rb-4.0.3&auto=format&fit=crop&w=1200&h=400&q=80" 
              alt="Fleet of Trucks" 
              class="rounded-lg shadow-xl relative z-10"
            >
            <div class="absolute -bottom-4 -right-4 w-32 h-32 bg-primary opacity-10 rounded-full"></div>
          </div>
        </div>
      </div>
    </div>
  </section>
  
  <!-- Values Section -->
  <section class="py-16 bg-white" id="values">
    <div class="container mx-auto px-4">
      <div class="text-center mb-12">
        <span class="text-secondary font-medium">Our Core Values</span>
        <h2 class="text-3xl font-bold text-primary mt-2">{companyName} has always been values-driven</h2>
        <div class="w-20 h-1 bg-secondary mx-auto mt-4 mb-6"></div>
      </div>
      
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
        {#each coreValues as value, i}
          <div class="bg-white rounded-lg shadow-lg p-6 text-center transition-all duration-300 hover:shadow-xl hover:translate-y-[-10px] border-t-4 border-{value.background === 'bg-primary-light' ? 'primary' : 'secondary'}">
            <div class="w-16 h-16 rounded-full flex items-center justify-center bg-gray-100 text-{value.background === 'bg-primary-light' ? 'primary' : 'secondary'} mx-auto mb-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d={value.icon} />
              </svg>
            </div>
            <h3 class="text-xl font-bold text-primary mb-3">{value.title}</h3>
            <p class="text-gray-600">{value.description}</p>
          </div>
        {/each}
      </div>
    </div>
  </section>
  
  <!-- CTA Section -->
  <section class="py-16 bg-primary text-white" id="cta">
    <div class="container mx-auto px-4 text-center">
      <h2 class="text-3xl font-bold mb-6">Ready to Transform Your Fleet's Safety Culture?</h2>
      <p class="text-lg mb-8 max-w-3xl mx-auto opacity-90">Partner with {companyName} for comprehensive safety solutions that protect your drivers, assets, and bottom line.</p>
      <div class="flex flex-col sm:flex-row justify-center space-y-4 sm:space-y-0 sm:space-x-4">
        <a href="/contact" class="bg-white hover:bg-opacity-90 text-primary font-medium py-3 px-8 rounded-md transition duration-300">
          Contact Us Today
        </a>
        <a href="/demo" class="bg-transparent hover:bg-white/10 border-2 border-white text-white font-medium py-3 px-8 rounded-md transition duration-300">
          Request a Demo
        </a>
      </div>
    </div>
    
    <!-- Decorative elements -->
    <div class="absolute top-0 right-0 w-24 h-24 bg-white opacity-5 rounded-full -translate-y-1/2"></div>
    <div class="absolute bottom-0 left-0 w-32 h-32 bg-secondary opacity-10 rounded-full translate-y-1/3"></div>
  </section>
  
  <style>
    /* Custom color variables */
    :root {
      --color-primary: #0b163f;
      --color-primary-dark: #070e29;
      --color-primary-light: #2563eb;
      --color-secondary: #3b82f6;
      --color-secondary-dark: #1d4ed8;
    }
    
    .bg-primary {
      background-color: var(--color-primary);
    }
    
    .bg-primary-dark {
      background-color: var(--color-primary-dark);
    }
    
    .bg-primary-light {
      background-color: var(--color-primary-light);
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
    
    .border-primary {
      border-color: var(--color-primary);
    }
    
    .border-secondary {
      border-color: var(--color-secondary);
    }
    
    /* Hover animations */
    .hover\:translate-y-\[-10px\]:hover {
      transform: translateY(-10px);
    }
    
    /* Container width control */
    .container {
      max-width: 1200px;
    }
    
    /* Section spacing consistency */
    section {
      position: relative;
      overflow: hidden;
    }
  </style>