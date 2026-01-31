# Free-unlimited-thumbnail-

<!DOCTYPE html><html lang="hi">
<head>
  <meta charset="UTF-8" />
  <title>Unlimited YouTube Thumbnails</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #0f172a;
      color: #fff;
    }
    header {
      padding: 15px;
      text-align: center;
      background: #020617;
      font-size: 22px;
      font-weight: bold;
    }
    .search-box {
      padding: 15px;
      text-align: center;
    }
    .search-box input {
      width: 90%;
      max-width: 400px;
      padding: 10px;
      border-radius: 6px;
      border: none;
      outline: none;
      font-size: 16px;
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
      gap: 15px;
      padding: 15px;
    }
    .thumb {
      background: #020617;
      border-radius: 10px;
      overflow: hidden;
      cursor: pointer;
      transition: transform 0.2s;
    }
    .thumb:hover {
      transform: scale(1.05);
    }
    .thumb img {
      width: 100%;
      display: block;
    }
    .thumb p {
      padding: 8px;
      font-size: 14px;
      text-align: center;
    }
    footer {
      text-align: center;
      padding: 10px;
      font-size: 13px;
      background: #020617;
    }
  </style>
</head>
<body><header>Unlimited YouTube Long Video Thumbnails</header><div class="search-box">
  <input type="text" id="search" placeholder="Search thumbnail (gaming, vlog, tech...)" />
</div><div class="grid" id="thumbnailGrid">
  <!-- Thumbnails JS se load honge -->
</div><footer>
  © 2026 Thumbnail Hub | Free to Use
</footer><script>
  const thumbnails = [
    { title: "Gaming Epic Win", img: "https://picsum.photos/400/225?random=1" },
    { title: "Minecraft Survival", img: "https://picsum.photos/400/225?random=2" },
    { title: "Vlog Travel", img: "https://picsum.photos/400/225?random=3" },
    { title: "Tech Review", img: "https://picsum.photos/400/225?random=4" },
    { title: "Free Fire Gameplay", img: "https://picsum.photos/400/225?random=5" },
    { title: "YouTube Tips", img: "https://picsum.photos/400/225?random=6" }
  ];

  const grid = document.getElementById("thumbnailGrid");
  const search = document.getElementById("search");

  function loadThumbnails(list) {
    grid.innerHTML = "";
    list.forEach(t => {
      const div = document.createElement("div");
      div.className = "thumb";
      div.innerHTML = `
        <img src="${t.img}" alt="${t.title}">
        <p>${t.title}</p>
      `;
      div.onclick = () => window.open(t.img, '_blank');
      grid.appendChild(div);
    });
  }

  loadThumbnails(thumbnails);

  search.addEventListener("input", () => {
    const value = search.value.toLowerCase();
    const filtered = thumbnails.filter(t => t.title.toLowerCase().includes(value));
    loadThumbnails(filtered);
  });
</script></body>
</html>
