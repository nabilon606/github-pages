
<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AI Video Finder</title>
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
</head>
<body class="bg-gray-900 text-white">
  <div class="container mx-auto p-6">
    <h1 class="text-3xl font-bold mb-6 text-center">AI Video Finder</h1><!-- Video Upload Section -->
<div class="bg-gray-800 p-6 rounded-lg mb-8">
  <h2 class="text-xl font-semibold mb-4">Upload a Video</h2>
  <form id="uploadForm" enctype="multipart/form-data">
    <input type="file" name="video" accept="video/*" class="block w-full mb-4 p-2 bg-gray-700 rounded">
    <button type="submit" class="bg-blue-600 hover:bg-blue-700 px-4 py-2 rounded">Upload</button>
  </form>
</div>

<!-- Similar Videos Section -->
<div id="similarVideos" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
  <!-- Dynamic content will be loaded here -->
</div>

  </div>  <script>
    const form = document.getElementById('uploadForm');
    const videoContainer = document.getElementById('similarVideos');

    form.addEventListener('submit', async (e) => {
      e.preventDefault();
      const formData = new FormData(form);

      // Fake loading for demonstration
      videoContainer.innerHTML = '<p class="col-span-3 text-center">Finding similar videos...</p>';

      // Simulate fetching similar videos
      setTimeout(() => {
        videoContainer.innerHTML = '';
        for (let i = 1; i <= 10; i++) {
          const video = document.createElement('div');
          video.className = 'bg-gray-800 p-4 rounded';
          video.innerHTML = `
            <video controls class="w-full mb-2">
              <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4">
            </video>
            <p>Similar Video ${i}</p>
          `;
          videoContainer.appendChild(video);
        }
      }, 2000);
    });
  </script></body>
</html>
