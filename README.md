<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bleacher Report</title>
    <style>
        /* CSS styles */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #333;
            color: #fff;
            padding: 10px 0;
            text-align: center;
        }
        nav {
            background-color: #444;
            padding: 10px 0;
            text-align: center;
        }
        nav a {
            color: #fff;
            text-decoration: none;
            padding: 10px 20px;
            margin: 0 5px;
            border-radius: 5px;
            background-color: #666;
        }
        nav a:hover {
            background-color: #888;
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }
        .article {
            display: flex;
            margin-bottom: 20px;
            border-bottom: 1px solid #ccc;
            padding-bottom: 20px;
        }
        .article img {
            width: 120px;
            height: 120px;
            margin-right: 20px;
        }
        .article h2 {
            font-size: 1.4rem;
            margin-bottom: 5px;
        }
        .article .meta {
            color: #666;
            margin-bottom: 10px;
        }
        .article .meta span {
            margin-right: 10px;
        }
        .featured {
            background-color: #f0f0f0;
            padding: 10px;
            margin-bottom: 20px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Bleacher Report</h1>
    </header>
    <nav>
        <a href="#" class="active">All</a>
        <a href="#">Sports</a>
        <a href="#">Entertainment</a>
        <a href="#">Politics</a>
        <a href="#">Technology</a>
        <a href="#">Health</a>
    </nav>
    <div class="container">
        <!-- Featured Articles -->
        <div class="featured">
            <h2>Featured Articles</h2>
            <div class="article">
                <img src="featured1.jpg" alt="Featured Article 1">
                <div>
                    <h2>Featured Article 1</h2>
                    <div class="meta">
                        <span>Author: John Doe</span>
                        <span>Date: March 17, 2024</span>
                    </div>
                    <p>Description of Featured Article 1</p>
                </div>
            </div>
            <div class="article">
                <img src="featured2.jpg" alt="Featured Article 2">
                <div>
                    <h2>Featured Article 2</h2>
                    <div class="meta">
                        <span>Author: Jane Smith</span>
                        <span>Date: March 16, 2024</span>
                    </div>
                    <p>Description of Featured Article 2</p>
                </div>
            </div>
        </div>
        
        <!-- Articles list -->
        <div id="articles">
            <!-- Articles will be dynamically added here using JavaScript -->
        </div>
    </div>

    <script>
        // JavaScript for fetching articles data and rendering them dynamically
        const articles = [
            { title: "Article 1", image: "image1.jpg", description: "Description of Article 1", author: "John Doe", date: "March 15, 2024", category: "Sports" },
            { title: "Article 2", image: "image2.jpg", description: "Description of Article 2", author: "Jane Smith", date: "March 14, 2024", category: "Entertainment" },
            { title: "Article 3", image: "image3.jpg", description: "Description of Article 3", author: "Alex Johnson", date: "March 13, 2024", category: "Politics" },
            { title: "Article 4", image: "image4.jpg", description: "Description of Article 4", author: "Emily Brown", date: "March 12, 2024", category: "Technology" },
            { title: "Article 5", image: "image5.jpg", description: "Description of Article 5", author: "Michael Wilson", date: "March 11, 2024", category: "Health" }
        ];

        // Function to render articles
        function renderArticles(category = '') {
            const articlesContainer = document.getElementById("articles");
            articlesContainer.innerHTML = "";
            articles.forEach(article => {
                if (category === '' || article.category === category) {
                    const articleElem = document.createElement("div");
                   
