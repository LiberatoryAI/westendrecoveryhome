I have 20 photographs.  I would like to build a website that displays the photographs in a gallery format.  I would like the gallery to be 4x5 and have a title bar.  At the bottom of the site I would like to have two buttons.  One for a link to Twitter and another to Vimeo.

It sounds like a straightforward website design, and I can certainly help with the concept. Given your requirements, I'm going to write some basic HTML/CSS code for you to get started. For simplicity, this example assumes you have all the images in the same directory as the HTML file and they're named photo1.jpg, photo2.jpg, etc.

HTML:

<!DOCTYPE html>
<html>
<head>
  <title>Your Photo Gallery</title>
  <link rel="stylesheet" type="text/css" href="styles.css">
</head>
<body>
  <header>
    <h1>Your Photo Gallery</h1>
  </header>

  <div class="gallery">
    <!-- Repeat this for each image -->
    <div class="photo">
      <img src="photo1.jpg" alt="Photo 1">
    </div>
    <!-- ... -->
  </div>

  <footer>
    <a href="https://twitter.com/_benjamin_group" class="btn" target="_blank">Twitter</a>
    <a href="https://vimeo.com/user203270079" class="btn" target="_blank">Vimeo</a>
  </footer>
</body>
</html>

CSS (styles.css):

body {
  display: flex;
  flex-direction: column;
  align-items: center;
  font-family: Arial, sans-serif;
}

header {
  margin-bottom: 20px;
}

.gallery {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

.photo img {
  max-width: 100%;
  height: auto;
}

footer {
  margin-top: 20px;
}

.btn {
  display: inline-block;
  background-color: #333;
  color: #fff;
  padding: 10px 20px;
  margin: 5px;
  text-decoration: none;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}

.btn:hover {
  background-color: #777;
}

This is just a starting point and it can be adjusted to suit your exact needs. For instance, you might want to add navigation, additional sections, or modify the styling to match your preferred aesthetics.

Please note that handling responsiveness for different device sizes or adding more interactive behavior might require additional code or the use of JavaScript. You may also want to consider using a CMS or a site builder like Wordpress, Wix, or Squarespace if you prefer a more visual approach to site building or if you plan to update the site frequently.