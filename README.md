<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>birthday-pia.html</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      height: 100vh;
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #ffd6e8, #ffc0d9);
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .container {
      text-align: center;
      padding: 20px;
    }

    .card {
      background: #fff;
      border-radius: 30px;
      box-shadow: 0 0 40px rgba(255, 100, 150, 0.3);
      padding: 40px 30px;
      max-width: 700px;
      color: #ff3c8f;
      font-size: 16px;
      line-height: 1.8;
      white-space: pre-wrap;
      overflow: hidden;
    }

    .cursor {
      display: inline-block;
      width: 8px;
      height: 22px;
      background-color: #ff3c8f;
      vertical-align: bottom;
      animation: blink 0.8s infinite;
    }

    @keyframes blink {
      0%, 50% { opacity: 1; }
      51%, 100% { opacity: 0; }
    }
  </style>
</head>
<body>
  <audio id="bg-music" autoplay loop>
    <source src="https://cdn.pixabay.com/download/audio/2023/03/20/audio_57ce9f0f33.mp3?filename=soft-piano-melody-14357.mp3" type="audio/mpeg">
  </audio>

  <div class="container">
    <div class="card">
      <span id="text"></span><span class="cursor"></span>
    </div>
  </div>

  <script>
    const message = `HAIII (PPIIIAAAAAA) 

Happy birthday to one of the most genuine, kind-hearted, and beautiful souls I’ve ever known 🎂✨
Another year older, another chapter of your story — and I’m so proud of how far you’ve come.

Aku tau kadang hidup nggak selalu ramah, nggak selalu gampang, dan kamu sering banget pura-pura kuat biar orang lain nggak khawatir.
Tapi aku lihat kok, betapa kamu berjuang, betapa kamu tetap berusaha jadi versi terbaik dari dirimu sendiri.
And honestly, that’s one of the many reasons why I admire you so much.

Kamu itu punya cara yang unik buat bikin orang nyaman.
Even in silence, you make people feel safe.
You don’t even have to say much, tapi kehadiran kamu aja udah cukup buat ngebuat suasana tenang.
I’m really thankful to have someone like you in my life muah.

aku juga pengen minta maaf…
Maaf karena aku sering datang bukan buat kasih kabar bahagia, tapi buat ngeluh, buat curhat, buat nyari tempat pelarian dari semua hal yang bikin aku capek.
Kadang aku lupa kalau kamu juga bisa lelah, tapi tetap kamu dengerin aku, sabar, nggak pernah nyalahin.
That’s something I’ll never take for granted.

Aku tau aku bukan temen terbaik, bukan yang paling seru, bukan juga yang paling bisa diandalkan.
But somehow, you still choose to stay, and I’m really grateful for that.
You’re like a soft reminder that kindness still exists in this world, and I’m so lucky to be someone who gets to see that every day through you heheheh.

Semoga di umur yang baru ini, kamu dikasih banyak banget alasan buat senyum.
Semoga orang-orang di sekitarmu selalu baik, tapi lebih dari itu — semoga kamu juga belajar buat lebih baik ke diri kamu sendiri.
Because you deserve everything good this world could possibly give.

Don’t let anyone dim your light, okay?
You have this soft glow that makes everything feel a little less heavy — don’t lose that.
Even when days get rough, even when you feel tired, remember that there are people who love you deeply, and I’m one of them (in a totally friendly but still very sincere way 🩷).

I hope this year gives you more laughter than tears, more peace than chaos, and more love than you could ever imagine.
May all the dreams you whisper to the stars slowly find their way to reality 🌙✨

Dan sekali lagi, makasih udah jadi kamu —
yang tulus, yang sabar, yang tetap bisa senyum walaupun dunia lagi nggak sebaik itu.
Aku harap kamu nggak pernah berubah, tapi juga nggak berhenti tumbuh.
Keep becoming the best version of yourself, step by step.

happy birthday once again, my favorite person 💕
I know this message is long (I hope your eyes are still okay by now hahahah😭),
but that’s just how much I appreciate you.

You deserve all the love, joy, and peace in the world — and I’ll always be cheering for you, from near or far.
Please keep shining, keep smiling, and never forget how special you are.

With love (and a little bit of chaos, as always wkkwkwkwkw💗),
— (dindaaaa)`;

    const textElement = document.getElementById("text");
    let index = 0;

    function typeEffect() {
      if (index < message.length) {
        textElement.textContent += message.charAt(index);
        index++;
        setTimeout(typeEffect, 40);
      }
    }

    document.body.addEventListener("click", () => {
      const music = document.getElementById("bg-music");
      music.play();
    });

    window.onload = typeEffect;
  </script>
</body>
</html>
