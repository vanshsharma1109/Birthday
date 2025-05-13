<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Happy Birthday Aanya!</title>
  <style>
    * {
      margin: 0; padding: 0; box-sizing: border-box;
    }
    body {
      font-family: 'Segoe UI', sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      background: linear-gradient(135deg, #ffdde1, #fcb69f);
      color: #333;
      padding: 20px;
      text-align: center;
    }
    .card {
      max-width: 500px;
      width: 100%;
      background: white;
      border-radius: 15px;
      box-shadow: 0 10px 20px rgba(0,0,0,0.2);
      padding: 20px;
      transition: all 0.4s ease-in-out;
    }
    img {
      max-width: 100%;
      border-radius: 10px;
      margin: 15px 0;
    }
    .nav-buttons {
      margin-top: 15px;
      display: flex;
      justify-content: space-between;
    }
    button {
      background: #ff6f91;
      color: white;
      border: none;
      padding: 10px 20px;
      border-radius: 10px;
      font-size: 1rem;
      cursor: pointer;
    }
    button:disabled {
      background: #ddd;
      color: #999;
      cursor: not-allowed;
    }
    p {
      white-space: pre-wrap;
      line-height: 1.6;
    }
  </style>
</head>
<body>
  <div class="card" id="card">
    <!-- Content loaded by JavaScript -->
  </div>

  <script>
    const pages = [
      {
        text: `🎉 Happy Birthday Aanya! 🎂

On your special day, may every moment bring joy to your heart and a smile to your face. You are a treasure to everyone who knows you.

Let this day be filled with laughter, warmth, and beautiful surprises just like you.`
      },
      {
        image: "mongia.PNG",
        text: `🌸 A Radiant Glow 🌸

Your smile’s a spark that lights the skies,
With grace that softens cloudy eyes.
The calm you bring in every room,
Can turn the thorns of life to bloom.

Your laughter dances on the breeze,
A melody that puts hearts at ease.
Each glance from you, a gentle grace,
Like moonlight's touch upon my face.

The way you walk, the way you shine,
It feels as though the stars align.
Aanya, you’re a dream so sweet,
A poem the world longs to repeat.`
      },
      {
        image: "mongia1.PNG",
        text: `🌼 Gentle Heart 🌼

A soul so kind, a heart so pure,
Your presence is a perfect cure.
For aching thoughts and cloudy days,
You bring the sun in quiet ways.

With every word you softly say,
You chase the bitter gloom away.
A gentle fire in winter's chill,
You warm the world, you always will.

Like petals bloom in early spring,
You make the silent robins sing.
You're poetry that comes to life,
A rhythm cutting through the strife.`
      },
      {
        image: "mongia3.PNG",
        text: `🌷 Painted with Light 🌷

You're painted from a dreamer's mind,
With colors even stars can't find.
A face that holds a thousand tales,
That whisper through the evening gales.

Your eyes—they hold a gentle glow,
Like lanterns dancing through the snow.
A universe within your gaze,
That shines through all of life’s malaise.

You're not just beauty, but a muse,
A spark that no one can refuse.
You’re every poem ever penned,
And every wish the heavens send.`
      },
      {
        image: "mongia4.PNG",
        text: `🌺 Forever Bloom 🌺

Among the flowers, you're the queen,
With elegance in every scene.
A wonder woven into time,
A living verse, a perfect rhyme.

You hold the morning in your eyes,
A thousand dreams beneath blue skies.
Your voice, a song the sparrows know,
A hush that makes the wild winds slow.

May you forever bloom and rise,
Aanya—the starlight in disguise.
With all my heart I send this cheer,
Happy birthday, bright and dear.`
      },
      {
        text: `💖 From the Heart 💖

Aanya, I just want to say what words often fail to express.

You are more than just beautiful — you are a soul full of kindness, strength, and silent courage. Your presence brings peace, your smile brings joy, and your heart? It carries a rare kind of warmth. I hope this little card made you smile even a little because that's what you've done for me — again and again.

Never stop being you. You're magical. 🌷`
      }
    ];

    let currentPage = 0;

    function renderPage() {
      const card = document.getElementById("card");
      const content = pages[currentPage];

      card.innerHTML = `
        ${content.image ? `<img src="${content.image}" alt="Birthday Image" />` : ""}
        <p>${content.text}</p>
        <div class="nav-buttons">
          <button onclick="prevPage()" ${currentPage === 0 ? "disabled" : ""}>⬅ Prev</button>
          <button onclick="nextPage()" ${currentPage === pages.length - 1 ? "disabled" : ""}>Next ➡</button>
        </div>
      `;
    }

    function nextPage() {
      if (currentPage < pages.length - 1) {
        currentPage++;
        renderPage();
      }
    }

    function prevPage() {
      if (currentPage > 0) {
        currentPage--;
        renderPage();
      }
    }

    renderPage();
  </script>
</body>
</html>

