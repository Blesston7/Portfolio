# Portfolio

#scripts
const sections = document.querySelectorAll("section");
const projects = document.querySelectorAll(".project");
const aboutBox = document.querySelector(".about-box");



const revealOnScroll = () => {
  const triggerBottom = window.innerHeight * 0.9;

  // Reveal sections
  sections.forEach(section => {
    const sectionTop = section.getBoundingClientRect().top;
    if (sectionTop < triggerBottom) {
      section.classList.add("visible");
    }
  });

  // Reveal individual project boxes
  projects.forEach(project => {
    const projectTop = project.getBoundingClientRect().top;
    if (projectTop < triggerBottom) {
      project.classList.add("visible");
    }
  });
};

window.addEventListener("scroll", revealOnScroll);
window.addEventListener("load", revealOnScroll);

window.addEventListener("scroll", revealOnScroll);
window.addEventListener("load", revealOnScroll); // trigger on load too


document.addEventListener("DOMContentLoaded", function () {
  const enterBtn = document.getElementById("enter-btn");
  const welcomePage = document.getElementById("welcome-page");

  enterBtn.addEventListener("click", function () {
    welcomePage.classList.add("fade-out");

    // Optional: delay hiding the welcome page completely
    setTimeout(() => {
      welcomePage.style.display = "none";
    }, 800); // match the animation duration
  });
});
const enterButton = document.getElementById("enter-btn");
const welcomePage = document.getElementById("welcome-page");

enterButton.addEventListener("click", () => {
  welcomePage.style.display = "none";  // Hide the welcome page when clicked
});

