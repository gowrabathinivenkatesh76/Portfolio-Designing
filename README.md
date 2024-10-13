# Portfolio-Designing
This portfolio is completely about me and my progree in learning 
HTML Code :                                                                                                                     <!DOCTYPE html> 
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <style>
        .hidden { display: none; }
    </style>
</head>
<body class="bg-gray-100">
    <header class="bg-red-600 text-white py-5">
        <div class="container mx-auto text-center">
            <h1 class="text-4xl font-bold">Gowrabathini Venkatesh</h1>
            <p class="mt-2">B.Tech Computer Science and Business Systems </p>
            <center><img src="c:\Users\venky\Downloads\venky iv.JPG" width="200px"></center>
        </div>
    </header>
    <main class="container mx-auto my-10">
        <section id="about" class="mb-10">
            <h2 class="text-3xl font-semibold mb-5">About Me</h2>
            <p class="text-gray-700">I am a computer science student with some experience in designing user-friendly interfaces. I like coding and creating visually appealing applications.</p>
        </section>
        
        <section id="projects" class="mb-10">
            <h2 class="text-3xl font-semibold mb-5">Projects</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                <div class="bg-white p-5 rounded shadow cursor-pointer" onclick="toggleProject('project1')">
                    <h3 class="font-semibold">Project 1</h3>
                    <p>Basic Event webpage. Technologies used: HTML.</p>
                    <div id="project1" class="hidden">
                        <img src="c:\Users\venky\Pictures\Screenshots\HTML Project 1\2.png" alt="Project 1 Image" class="mb-3">
                        <p>Detailed description of Project 1...This project involved creating a responsive and visually appealing webpage to promote an upcoming event. Utilizing HTML, I designed a layout that showcases essential details such as event date, location, and schedule, ensuring a user-friendly experience. The webpage also includes interactive elements, enhancing engagement and providing visitors with easy access to registration and additional information.</p>
                    </div>
                </div>
                <div class="bg-white p-5 rounded shadow cursor-pointer" onclick="toggleProject('project2')">
                    <h3 class="font-semibold">Project 2</h3>
                    <p>EMC Project Webpage. Technologies used: HTML, CSS.</p>
                    <div id="project2" class="hidden">
                        <img src="c:\Users\venky\Pictures\Screenshots\HTML Project 2\3.png" alt="Project 2 Image" class="mb-3">
                        <p>Detailed description of Project 2... This project focused on building a user-friendly registration page using HTML. It features input fields for user information, including name, email, and password, ensuring secure data collection. The design emphasizes simplicity and accessibility, making it easy for users to complete their registration smoothly.</p>
                    </div>
                </div>
                <div class="bg-white p-5 rounded shadow cursor-pointer" onclick="toggleProject('project3')">
                    <h3 class="font-semibold">Project 3</h3>
                    <p>Game Development. Technologies used: PyGame.</p>
                    <div id="project3" class="hidden">
                        <img src="c:\Users\venky\Downloads\pygame.png" alt="Project 3 Image" class="mb-3">
                        <p>Detailed description of Project 3...This project involved creating an engaging 2D game using the PyGame library. I designed interactive gameplay mechanics, including character movement and collision detection, while utilizing graphics and sound to enhance the user experience. The project emphasizes creativity and programming skills, showcasing my ability to develop entertaining applications.</p>
                    </div>
                </div>
                <div class="bg-white p-5 rounded shadow cursor-pointer" onclick="toggleProject('project4')">
                    <h3 class="font-semibold">Project 4</h3>
                    <p>Android App Development. Technologies used: Python, HTML5.</p>
                    <div id="project4" class="hidden">
                        <img src="c:\Users\venky\Downloads\android app development.jfif" alt="Project 4 Image" class="mb-3">
                        <p>Detailed description of Project 4...In this project, I developed a functional Android application that allows users to track their daily activities. Using HTML5 for the front end and integrating it with backend services, I focused on creating an intuitive user interface and seamless navigation. The app features real-time data updates and enhances user engagement through interactive elements.</p>
                    </div>
                </div>
            </div>
        </section>
        
        <section id="contact" class="mb-10">
            <h2 class="text-3xl font-semibold mb-5">Contact Me</h2>
            <form id="contact-form" class="space-y-4">
                <input type="text" placeholder="Your name" class="w-full p-2 border rounded" required>
                <input type="email" placeholder="Your Email" class="w-full p-2 border rounded" required>
                <textarea placeholder="Your Message" class="w-full p-2 border rounded" rows="5" required></textarea>
                <button type="submit" class="bg-blue-600 text-white py-2 px-4 rounded">Send Message</button>
            </form>
        </section>
    </main>

    <footer class="bg-gray-800 text-white text-center py-4">
        <p>&copy; 2024 Gowrabathini Venkatesh. All rights reserved.</p>
    </footer>

    <script>
        document.getElementById('contact-form').addEventListener('submit', function(event) {
            event.preventDefault();
            alert('Thank you for your message!');
            this.reset();
        });

        function toggleProject(projectId) {
            const projectElement = document.getElementById(projectId);
            projectElement.classList.toggle('hidden');
        }
    </script>
</body>
</html>                                                                                                                                              JS Code :                                                                                                                                           document.addEventListener('DOMContentLoaded', function() {
    document.getElementById('contact-form').addEventListener('submit', function(event) {
        event.preventDefault(); // Prevent the default form submission
        
        // Get form values
        const name = this.elements['name'].value.trim();
        const email = this.elements['email'].value.trim();
        const message = this.elements['message'].value.trim();
        
        // Basic validation
        if (!name || !email || !message) {
            alert('Please fill in all fields.');
            return;
        }

        // Simple email validation (very basic)
        const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
        if (!emailPattern.test(email)) {
            alert('Please enter a valid email address.');
            return;
        }

        // Simulate sending the message (you can replace this with actual API call)
        alert('Thank you for your message, ' + name + '! We will get back to you soon.');

        // Reset the form
        this.reset();
    });
});                 
