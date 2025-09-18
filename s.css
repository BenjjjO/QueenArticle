const scrollers = document.querySelectorAll(".scroller");
if(!window.matchMedia("(prefers-reduced-motion: reduce)").matches){
    addAnimation();
}
function addAnimation(){
  scrollers.forEach((scroller)=>{
    scroller.setAttribute("data-animated",true)

    const scrollerInner = scroller.querySelector(".scroller__inner")
    const scrollerContent = Array.from(scrollerInner.children);
    scrollerContent.forEach((item)=>{
const duplicatedItem = item.cloneNode(true)
duplicatedItem.setAttribute("aria-hidden", true);
scrollerInner.appendChild(duplicatedItem);
    })
  });
}

const slides = document.querySelectorAll(".slide")
let slideIndex = 0;
let intervalId = null;


document.addEventListener("DOMContentLoaded",initializeSlider)

function initializeSlider(){
    if(slides.length > 0){
        slides[slideIndex].classList.add("displaySlide")
        intervalId = setInterval(nextslide,5000)
    }

}

function showSlide(index){
    if(index  >= slides.length){
        slideIndex = 0;
    }
    else if(index < 0){
        slideIndex = slides.length -1;
    }
slides.forEach(slide =>{
    slide.classList.remove("displaySlide")
    
});
slides[slideIndex].classList.add("displaySlide")
}
function prevslide(){
    clearInterval(intervalId)
    slideIndex--;
    showSlide(slideIndex)
}
function nextslide(){
slideIndex++;
showSlide(slideIndex)
}
