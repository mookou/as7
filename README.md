#[codepen](https://codepen.io/Leemoo/pen/raBBBNp)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Plastic Cycle</title>
    <style>
        html {
            height: 100%;
            overflow: hidden;
        }

        body {
            margin: 0;
            padding: 0;
            perspective: 1px;
            transform-style: preserve-3d;
            height: 100%;
            overflow-y: scroll;
            overflow-x: hidden;
        }

        .slide {
            position: relative;
            min-height: 100vh;
            width: 100vw;
            box-sizing: border-box;
            transform-style: inherit;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        img {
            position: absolute;
            top: 50%;
            left: 35%;
            width: 320px;
            height: 240px;
            transform: translateZ(.25px) scale(.75) translateX(-94%) translateY(-100%) rotate(2deg);
            padding: 10px;
        }

        img:last-of-type {
            transform: translateZ(.4px) scale(.6) translateX(-104%) translateY(-40%) rotate(-5deg);
        }

        .slide:before {
            content: "";
            position: absolute;
            top: 0;
            bottom: 0;
            left: 0;
            right: 0;
        }

        .title {
            width: 50%;
            background: rgba(240, 230, 220, .7);
        }

        .slide, .slide:before {
            background: 50% 50% / cover;
        }

        .header {
            text-align: center;
            font-size: 175%;
            color: #fff;
            text-shadow: 0 2px 2px #000;
        }

        #title {
            background-image: url("https://www.europarl.europa.eu/resources/library/images/20240507PHT21404/20240507PHT21404-cl.jpg");
            z-index: 2;
        }

        /* 動畫效果：向右移動 */
        @keyframes moveRight {
            0% {
                left: -200px; /* 初始位置，圖片在左側外面 */
            }
            100% {
                left: 100%; /* 結束位置，圖片完全移出右側 */
            }
        }

        #title h1 {
            transform: translateZ(.25px) scale(.75);
            transform-origin: 50% 100%;
            font-size: 3rem; /* 可調整字體大小 */
            color: white;
            text-shadow: 0px 4px 6px rgba(0, 0, 0, 0.5); /* 增加立體感 */
        }

        #slide1:before {
            background-image: url("https://yamnews.blob.core.windows.net/20170609/a5a36159-e192-41e2-b30f-6732c883623b.jpg");
            transform: translateZ(-1px) scale(2);
        }

        #slide2 {
            background-image: url("https://static.scientificamerican.com/sciam/cache/file/B7B4EC45-7FAF-4A26-B4AE872ABC0DD2CF_source.jpg");
            z-index: 2;
        }

        #slide3:before {
            background-image: url("https://i0.hippopx.com/photos/694/824/1019/fish-market-sea-fresh-preview.jpg");
            transform: translateZ(-1px) scale(2);
        }

        #slide4 {
            background: #222;
        }

        /* 父容器，限制動畫範圍 */
        .moving-container {
            position: relative;
            width: 100%;
            height: 200px;
            overflow: hidden;
            background-color: #f0f0f0;
        }

        /* 移動的圖片 */
        .moving-image {
            position: absolute;
            top: 50%;
            left: 0;
            transform: translateY(-50%);
            animation: moveRight 5s linear infinite;
        }
    </style>
</head>
<body>
    <div id="title" class="slide header">
        <h1>plastic cycle</h1>
    </div>

    <div id="slide1" class="slide">
        <div class="title">
            <h1>拋棄的塑膠，影響生態環境</h1>
        </div>
    </div>
    <div class="moving-container">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRm24PdBu2JuLBlRJnR3J8uv_GwTcmLZmDlGA&s" alt="Moving Image" class="moving-image">
    </div>

    <div id="slide2" class="slide">
        <div class="title">
            <h1>"________"塑膠微粒 進入海洋生物體內</h1>
        </div>
        <img src="https://img.ltn.com.tw/Upload/news/600/2008/04/27/61.jpg" alt="Plastic">
        <img src="https://i.epochtimes.com/assets/uploads/2024/03/id14212815-GJkx7AmXYAAUHpH-600x400.jpg" alt="Marine Life">
    </div>

    <div id="slide3" class="slide">
        <div class="title">
            <h1>被捕撈的魚 成為盤中餐</h1>
        </div>
    </div>

    <div id="slide4" class="slide header">
        <h1>愛護生態 關注塑膠問題</h1>
    </div>
</body>
</html>

