<script>
    import Header from '../components/Header.svelte';
    import Footer from '../components/Footer.svelte';
    import '../app.css'; // Tailwind CSS import
  </script>
  
  <Header logoUrl="/images/saferaj-logo.png" />
  
  <main>
    <slot />
  </main>
    <Footer />