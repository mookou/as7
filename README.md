# [codepen](https://codepen.io/Leemoo/pen/raBBBNp)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Improved Version</title>
    <style>
        html, body {
            margin: 0;
            padding: 0;
            height: 100%;
            overflow-x: hidden;
        }
        .slide {
            position: relative;
            min-height: 100vh;
            width: 100vw;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            background: 50% 50% / cover no-repeat;
        }
        .slide:before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: inherit;
            z-index: -1;
        }
        .moving-container {
            position: relative;
            width: 100%;
            height: 200px;
            overflow: hidden;
            background-color: #f0f0f0;
        }
        .moving-image {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            animation: moveRight 5s linear infinite;
        }
        @keyframes moveRight {
            0% {
                transform: translateX(-100%);
            }
            100% {
                transform: translateX(100%);
            }
        }
    </style>
</head>
<body>
    <div id="title" class="slide" style="background-image: url('image-url.jpg');">
        <h1 style="color: white; text-shadow: 0px 2px 4px black;">Plastic Cycle</h1>
    </div>
    <div id="slide1" class="slide" style="background-image: url('another-image.jpg');">
        <h1>Plastic Impact on Ecosystems</h1>
    </div>
    <div class="moving-container">
        <img src="moving-image.jpg" alt="Moving Image" class="moving-image">
    </div>
</body>
</html>

