# Slider

This is a simple slider with HTML and CSS(sass) and raw JavaScript .

step 1: Add HTML

<div class="container">
  <div class="slide-box"> (first slide box)
    <div class="number">...</div> (number of an image)
    <img src="..." alt="..."> (image)
    <div class="caption">...</div> (caption of an image)
  </div>
  . ... (second slide box)
  . ... (third slide box)
  . ... (the fourth slide box)
  <a href="#" class="prev" onclick="plusSlides(-1)"> (previous slide button)
  <a href="#" class="next" onclick="plusSlides(1)"> (next slide button)
</div>

step 2: Add CSS
.
.
.
step 3: Add JS
  var slideIndex = 1;   // position of each slide
  showSlides(slideIndex); // call the slide show function

  function plusSlides(n) { // prev / next button function
    showSlides((slideIndex += n));
  }

  function showSlides(n) {  // showSlides function
    var i;
    let slides = document.querySelectorAll(".container__box"); // selected all slide boxses
    if (n > slides.length) {
      slideIndex = 1;
    }
    if (n < 1) {
      slideIndex = slides.length;
    }
    for (i = 0; i < slides.length; i++) {
      slides[i].style.display = "none";
    }
    slides[slideIndex - 1].style.display = "block";
  }
