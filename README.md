


**HTML: index.html**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Netflix Clone</title>
</head>
<body>
    <div class="header">
        <img class="logo" src="netflix-logo.png" alt="Netflix Logo">
    </div>

    <div class="main">
        <div class="movie-list">
            <!-- Movie/series cards go here -->
            <!-- Example card: -->
            <div class="movie-card" onclick="showDetails('Title', 'Description', 'videoURL')">
                <img src="movie-poster.jpg" alt="Movie Poster">
            </div>
        </div>

        <div class="details" id="details-section">
            <!-- Details of the selected title go here -->
            <!-- Example details: -->
            <h2 id="title"></h2>
            <p id="description"></p>
            <video id="video" controls></video>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
```

**CSS: styles.css**
```css
body {
    margin: 0;
    padding: 0;
    font-family: 'Arial', sans-serif;
    background-color: #111;
    color: #fff;
}

.header {
    padding: 20px;
    background-color: #111;
}

.logo {
    width: 120px;
}

.main {
    display: flex;
    justify-content: space-between;
    padding: 20px;
}

.movie-list {
    display: flex;
    flex-wrap: wrap;
}

.movie-card {
    width: 200px;
    margin: 10px;
    cursor: pointer;
}

.movie-card img {
    width: 100%;
    border-radius: 5px;
}

.details {
    width: 60%;
    display: none;
}

.details video {
    width: 100%;
    border-radius: 5px;
}
```

**JavaScript: script.js**
```js
function showDetails(title, description, videoURL) {
    document.getElementById('title').innerText = title;
    document.getElementById('description').innerText = description;
    
    const video = document.getElementById('video');
    video.src = videoURL;

    document.getElementById('details-section').style.display = 'block';
}
```
