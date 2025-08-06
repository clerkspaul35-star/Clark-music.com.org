<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Music Website</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-900 text-white font-sans">
  <div class="container mx-auto p-6">
    <h1 class="text-4xl font-bold mb-6 text-center">🎶 My Music Player</h1>

    <div id="music-list" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
      <!-- Songs will be inserted here -->
    </div>
  </div>

  <script>
    const songs = [
      {
        title: "Dreamscape",
        artist: "Lofi Artist",
        src: "https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3"
      },
      {
        title: "Chill Vibes",
        artist: "DJ Cool",
        src: "https://www.soundhelix.com/examples/mp3/SoundHelix-Song-2.mp3"
      },
      {
        title: "Night Ride",
        artist: "Synthwave",
        src: "https://www.soundhelix.com/examples/mp3/SoundHelix-Song-3.mp3"
      }
    ];

    const musicList = document.getElementById('music-list');

    songs.forEach(song => {
      const songCard = document.createElement('div');
      songCard.className = "bg-gray-800 rounded-xl p-4 shadow-lg";

      songCard.innerHTML = `
        <h2 class="text-xl font-semibold">${song.title}</h2>
        <p class="text-sm text-gray-400 mb-2">by ${song.artist}</p>
        <audio controls class="w-full">
          <source src="${song.src}" type="audio/mpeg">
          Your browser does not support the audio element.
        </audio>
      `;

      musicList.appendChild(songCard);
    });
  </script>
</body>
</html>

# Clark-music.com.org