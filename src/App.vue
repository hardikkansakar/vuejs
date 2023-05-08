<template>


  <head>
    <meta charset="utf-8">
    <title>My Single Page Website</title>
   
  </head>
  <body>
    <div id="app">
      <header>
        <h1>Welcome to My Website</h1>
        <nav>
          <ul>
            <li><a href="#about">About</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#contact">Contact</a></li>
          </ul>
        </nav>
      </header>
      
      <main>
        <section id="about">
          <h2>About Us</h2>
          <p>We are a small team of web developers passionate about building beautiful and functional websites.</p>
        </section>
        
        <section id="services">
          <h2>Our Services</h2>
          <ul>
            <li>Web Design</li>
            <li>Web Development</li>
            <li>SEO Optimization</li>
          </ul>
        </section>
        
        <section id="contact">
          <h2>Contact Us</h2>
          <form>
            <label for="name">Name:</label>
            <input type="text" id="name" name="name">
            
            <label for="email">Email:</label>
            <input type="email" id="email" name="email">
            
            <label for="message">Message:</label>
            <textarea id="message" name="message"></textarea>
            
            <button type="submit">Send</button>
          </form>
        </section>
      </main>
      
     
    </div>
    
    
  </body>


</template>


<style scoped>


  body {
    font-family: sans-serif;
    margin: 0;
    padding: 0;
  }

  #app {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }

  header {
    background-color: #333;
    color: #fff;
    padding: 20px;
  }

  nav ul {
    display: flex;
    list-style: none;
    margin: 0;
    padding: 0;
  }

  nav li {
    margin-right: 20px;
  }

  nav a {
    color: #fff;
    text-decoration: none;
  }

  main {
    flex: 1;
    padding: 20px;
  }

  section {
    margin-bottom: 40px;
  }

  h2 {
    font-size: 32px;
    margin-bottom: 20px;
  }

  ul {
    margin: 0;
    padding: 0;
  }

  li {
    list-style: none;
  }

  form {
    display: flex;
    flex-direction: column;
  }

  label {
    margin-bottom: 10px;
  }

  input,
  textarea {
    padding: 10px;
    margin-bottom: 20px;
    border: 2px solid #ccc;
    border-radius: 4px;
  }

  button {
    padding: 10px 20px;
    background-color: #333;
    color: #fff;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }

  button:hover {
    background-color: #444;
  }
</style>