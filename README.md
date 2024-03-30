<h1 align="center">Login Page using Ruby on Rails</h1>

<p align="center">This project demonstrates a simple login page implementation using Ruby on Rails for the backend and frontend code.</p>

<h2 align="center">Setup Instructions</h2>

<ol>
  <li><strong>Install Ruby on Rails:</strong> Make sure you have Ruby and Rails installed on your system. You can install them via Ruby Version Manager (RVM) or RubyInstaller (for Windows).</li>
  
  <li><strong>Create a New Rails App:</strong> Open your terminal and run the following command to create a new Rails application:</li>
  
  <pre><code>rails new login_page</code></pre>
  
  <li><strong>Generate Scaffold for User:</strong> Scaffold a User model with attributes for username and password. Run the following command:</li>
  
  <pre><code>rails generate scaffold User username:string password:string</code></pre>
  
  <li><strong>Run Migrations:</strong> Execute migrations to create the users table in the database:</li>
  
  <pre><code>rails db:migrate</code></pre>
  
  <li><strong>Create Routes:</strong> Open <code>config/routes.rb</code> and define routes for the login page:</li>
  
  <pre><code>Rails.application.routes.draw do
    resources :users
    get 'login', to: 'sessions#new'
    post 'login', to: 'sessions#create'
    delete 'logout', to: 'sessions#destroy'
    root 'users#index'
  end
  </code></pre>
  
  <li><strong>Create Sessions Controller:</strong> Generate a sessions controller to handle login/logout functionality:</li>
  
  <pre><code>rails generate controller sessions new create destroy</code></pre>
  
  <li><strong>Implement Authentication Logic:</strong> Implement login/logout functionality in <code>app/controllers/sessions_controller.rb</code>.</li>
  
  <li><strong>Create Views:</strong> Develop views for the login page in <code>app/views/sessions</code>.</li>
  
  <li><strong>Implement Frontend:</strong> Write frontend code for the login page using HTML, CSS, and optionally JavaScript. Place the frontend files in <code>app/views/sessions</code>.</li>
  
  <li><strong>Test:</strong> Start the Rails server and test the login page functionality in your browser:</li>
  
  <pre><code>rails server</code></pre>
</ol>

<h2 align="center">Directory Structure</h2>

<p align="center"><img src="directory_structure.png" alt="Directory Structure"></p>

<p align="center"><em>Directory structure for the Rails application.</em></p>

<h2 align="center">Additional Notes</h2>

<ul>
  <li>Ensure to handle authentication securely, such as using encryption for passwords.</li>
  <li>Implement validations for user input to enhance security and user experience.</li>
  <li>Consider integrating with a frontend framework like React or Vue.js for a more interactive user interface.</li>
</ul>

<p align="center">This README provides a basic guide to set up a login page using Ruby on Rails. Customize and expand upon it according to your project requirements and preferences.</p>
