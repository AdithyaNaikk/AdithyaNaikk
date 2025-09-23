
  



  



  
  
    
  



 About My Mission

  
    🌱 Currently Mastering: Computer Vision, Generative AI, Natural Language Processing
    👯 Seeking Collaborations: Innovative AIML Projects
    👨‍💻 Explore My Work: GitHub Repositories
    💬 Ask Me About: AI Software Development
    📫 Reach Me: naikadithya904@gmail.com
  



 Connect with Me

  
    
  



 Languages & Tools

  
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
    
      
    
  



 GitHub Analytics

  
  



  



 Cosmic Voyage Animation

  
  Navigating the AI Cosmos, One Code at a Time! 🚀



const canvas = document.getElementById('spaceGame');
const ctx = canvas.getContext('2d');

// Stars
const stars = [];
for (let i = 0; i < 50; i++) {
  stars.push({
    x: Math.random() * canvas.width,
    y: Math.random() * canvas.height,
    size: Math.random() * 2 + 1,
    speed: Math.random() * 2 + 1
  });
}

// Spaceship
const spaceship = {
  x: 50,
  y: canvas.height / 2,
  width: 30,
  height: 20,
  speed: 2,
  dy: 0
};

// Animation loop
function animate() {
  ctx.fillStyle = '#0D1117';
  ctx.fillRect(0, 0, canvas.width, canvas.height);

  // Draw stars
  ctx.fillStyle = '#FFFFFF';
  stars.forEach(star => {
    ctx.beginPath();
    ctx.arc(star.x, star.y, star.size, 0, Math.PI * 2);
    ctx.fill();
    star.x -= star.speed;
    if (star.x < 0) star.x = canvas.width;
  });

  // Draw spaceship (pixel-art style)
  ctx.fillStyle = '#00FFFF';
  ctx.beginPath();
  ctx.moveTo(spaceship.x, spaceship.y);
  ctx.lineTo(spaceship.x + spaceship.width, spaceship.y - spaceship.height / 2);
  ctx.lineTo(spaceship.x + spaceship.width * 0.7, spaceship.y);
  ctx.lineTo(spaceship.x + spaceship.width, spaceship.y + spaceship.height / 2);
  ctx.closePath();
  ctx.fill();
  ctx.fillStyle = '#FF00FF';
  ctx.fillRect(spaceship.x - 10, spaceship.y - 5, 5, 10); // Thruster

  // Update spaceship position
  spaceship.y += spaceship.dy;
  if (spaceship.y < spaceship.height / 2) spaceship.y = spaceship.height / 2;
  if (spaceship.y > canvas.height - spaceship.height / 2) spaceship.y = canvas.height - spaceship.height / 2;

  // Simulate movement
  spaceship.dy = Math.sin(Date.now() * 0.002) * 2; // Smooth oscillation

  requestAnimationFrame(animate);
}

// Keyboard controls (optional interactivity)
document.addEventListener('keydown', (e) => {
  if (e.key === 'ArrowUp') spaceship.dy = -spaceship.speed;
  if (e.key === 'ArrowDown') spaceship.dy = spaceship.speed;
});
document.addEventListener('keyup', () => spaceship.dy = 0);

// Start animation
animate();




  



@keyframes glow {
  from { box-shadow: 0 0 5px #00FFFF, 0 0 10px #00FFFF; }
  to { box-shadow: 0 0 10px #00FFFF, 0 0 20px #00FFFF; }
}
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}
