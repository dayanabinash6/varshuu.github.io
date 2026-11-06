
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="theme-color" content="#f8f5ff">
  <meta name="description" content="A little note from Abi to Varshi.">
  <title>A little note for Varshi</title>

  <style>
    :root {
      color-scheme: light;
      --ink: #302642;
      --muted: #706681;
      --purple: #7551a8;
      --purple-dark: #513779;
      --lavender: #eee7fb;
      --line: rgba(112, 84, 153, 0.14);
      --white: rgba(255, 255, 255, 0.86);
    }

    * {
      box-sizing: border-box;
    }

    body {
      position: relative;
      min-height: 100vh;
      margin: 0;
      overflow-x: hidden;
      color: var(--ink);
      background:
        radial-gradient(circle at 8% 8%, rgba(222, 207, 255, 0.48), transparent 27rem),
        radial-gradient(circle at 92% 40%, rgba(246, 222, 247, 0.45), transparent 25rem),
        #fbf9ff;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    }

    /* Little stars scattered across the page */
    body::before {
      position: fixed;
      z-index: 0;
      inset: 0;
      pointer-events: none;
      content: "";
      opacity: 0.44;
      background-image:
        radial-gradient(1.5px 1.5px at 8% 17%, #8f73bd 98%, transparent),
        radial-gradient(2px 2px at 88% 13%, #a48bcc 98%, transparent),
        radial-gradient(1.5px 1.5px at 76% 53%, #9a7ec3 98%, transparent),
        radial-gradient(1.5px 1.5px at 16% 71%, #ad91d1 98%, transparent),
        radial-gradient(2px 2px at 93% 82%, #9f83c6 98%, transparent),
        radial-gradient(1.5px 1.5px at 48% 91%, #b49bd5 98%, transparent);
    }

    .page {
      position: relative;
      z-index: 1;
      width: min(1000px, calc(100% - 36px));
      margin: 0 auto;
      padding: 24px 0 30px;
    }

    .topline {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 14px;
      margin-bottom: 18px;
    }

    .brand {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      color: var(--ink);
      font-size: 0.76rem;
      font-weight: 800;
      letter-spacing: 0.14em;
      text-decoration: none;
    }

    .brand-icon {
      display: grid;
      width: 36px;
      height: 36px;
      place-items: center;
      border: 1px solid rgba(117, 81, 168, 0.14);
      border-radius: 50%;
      background: #eee6fb;
      color: var(--purple);
      font-size: 1.1rem;
    }

    .topline-note {
      color: var(--muted);
      font-size: 0.68rem;
      font-weight: 750;
      letter-spacing: 0.12em;
      text-align: right;
    }

    .hero {
      position: relative;
      display: grid;
      grid-template-columns: minmax(0, 1.25fr) minmax(230px, 0.75fr);
      align-items: center;
      gap: 20px;
      min-height: 350px;
      overflow: hidden;
      padding: clamp(30px, 6vw, 66px);
      isolation: isolate;
      border: 1px solid rgba(127, 99, 170, 0.16);
      border-radius: 32px;
      background: linear-gradient(125deg, #f0eaff 0%, #faf6ff 56%, #fff8ff 100%);
      box-shadow: 0 22px 65px rgba(66, 44, 98, 0.09);
    }

    .hero::before {
      position: absolute;
      z-index: -1;
      right: 14%;
      bottom: -190px;
      width: 390px;
      height: 390px;
      border-radius: 50%;
      background: rgba(214, 197, 244, 0.3);
      content: "";
    }

    .hero-copy {
      position: relative;
      z-index: 2;
      max-width: 620px;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      margin: 0;
      color: var(--purple);
      font-size: 0.72rem;
      font-weight: 800;
      letter-spacing: 0.13em;
    }

    .eyebrow::before {
      color: #a183ca;
      content: "✦";
      font-size: 1rem;
    }

    h1 {
      margin: 20px 0 16px;
      font-family: Georgia, "Times New Roman", serif;
      font-size: clamp(3rem, 7vw, 5.2rem);
      font-weight: 600;
      line-height: 0.98;
      letter-spacing: -0.055em;
    }

    h1 span {
      color: var(--purple);
    }

    .hero-text {
      max-width: 490px;
      margin: 0;
      color: var(--muted);
      font-size: 1.05rem;
      line-height: 1.75;
    }

    .hero-illustration {
      position: relative;
      z-index: 1;
      justify-self: end;
      width: min(100%, 350px);
      animation: float 6s ease-in-out infinite;
    }

    .hero-illustration svg {
      display: block;
      width: 100%;
      height: auto;
      filter: drop-shadow(0 14px 16px rgba(81, 55, 121, 0.1));
    }

    .twinkle {
      position: absolute;
      color: #9675c4;
      animation: twinkle 3s ease-in-out infinite;
    }

    .twinkle-one {
      top: 5%;
      right: 12%;
      font-size: 1.5rem;
    }

    .twinkle-two {
      top: 30%;
      left: -2%;
      animation-delay: 1s;
      font-size: 1.05rem;
    }

    .content-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.45fr) minmax(260px, 0.85fr);
      align-items: stretch;
      gap: 18px;
      margin-top: 18px;
    }

    .letter-card,
    .reminder-card {
      border: 1px solid var(--line);
      border-radius: 26px;
      box-shadow: 0 14px 40px rgba(66, 44, 98, 0.06);
      backdrop-filter: blur(10px);
    }

    .letter-card {
      padding: clamp(24px, 4.3vw, 38px);
      background: var(--white);
    }

    .section-label {
      display: flex;
      align-items: center;
      gap: 9px;
      margin: 0 0 24px;
      color: var(--purple);
      font-size: 0.7rem;
      font-weight: 800;
      letter-spacing: 0.13em;
    }

    .section-label::before {
      color: #a183ca;
      content: "✧";
      font-size: 1.1rem;
    }

    .letter-card p:not(.section-label) {
      color: var(--muted);
      font-size: 0.98rem;
      line-height: 1.85;
    }

    .letter-card .salutation {
      color: var(--ink) !important;
      font-weight: 700;
    }

    .signoff {
      margin-top: 24px;
    }

    .signoff strong {
      color: var(--purple-dark);
    }

    .reminder-card {
      position: relative;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      justify-content: center;
      overflow: hidden;
      padding: clamp(25px, 4vw, 34px);
      background: linear-gradient(150deg, #eee6fb 0%, #faf6ff 58%, #fff9ff 100%);
    }

    .reminder-card::after {
      position: absolute;
      right: -42px;
      bottom: -53px;
      width: 150px;
      height: 150px;
      border: 1px solid rgba(117, 81, 168, 0.12);
      border-radius: 50%;
      box-shadow:
        0 0 0 18px rgba(117, 81, 168, 0.035),
        0 0 0 38px rgba(117, 81, 168, 0.025);
      content: "";
      pointer-events: none;
    }

    .reminder-icon {
      margin-bottom: 12px;
      color: var(--purple);
      font-size: 1.6rem;
    }

    .reminder-card h2 {
      margin: 0 0 12px;
      font-family: Georgia, "Times New Roman", serif;
      font-size: 1.85rem;
      font-weight: 600;
      letter-spacing: -0.03em;
    }

    .reminder-count {
      margin-bottom: 13px;
      color: var(--purple);
      font-size: 0.67rem;
      font-weight: 800;
      letter-spacing: 0.12em;
    }

    .reminder-text {
      position: relative;
      z-index: 1;
      min-height: 130px;
      margin: 0 0 22px;
      color: #635774;
      font-size: 1.02rem;
      line-height: 1.75;
    }

    .reminder-text.is-changing {
      animation: reminder-in 260ms ease both;
    }

    .reminder-help {
      margin: 0 0 18px;
      color: var(--muted);
      font-size: 0.82rem;
      line-height: 1.6;
    }

    button {
      position: relative;
      z-index: 1;
      width: 100%;
      padding: 14px 17px;
      border: 0;
      border-radius: 999px;
      background: var(--purple-dark);
      color: #fff;
      cursor: pointer;
      font: inherit;
      font-size: 0.9rem;
      font-weight: 750;
      box-shadow: 0 8px 18px rgba(81, 55, 121, 0.17);
      transition: background 160ms ease, transform 160ms ease, box-shadow 160ms ease;
    }

    button:hover {
      background: #684692;
      box-shadow: 0 11px 22px rgba(81, 55, 121, 0.22);
      transform: translateY(-2px);
    }

    button:active {
      transform: translateY(0);
    }

    button:focus-visible {
      outline: 3px solid #b89bdf;
      outline-offset: 4px;
    }

    footer {
      display: flex;
      justify-content: space-between;
      gap: 12px;
      margin-top: 20px;
      padding: 0 4px;
      color: var(--muted);
      font-size: 0.78rem;
    }

    @keyframes twinkle {
      0%, 100% {
        opacity: 0.65;
        transform: scale(0.9);
      }
      50% {
        opacity: 1;
        transform: scale(1.15);
      }
    }

    @keyframes float {
      0%, 100% {
        transform: translateY(0);
      }
      50% {
        transform: translateY(-7px);
      }
    }

    @keyframes reminder-in {
      from {
        opacity: 0.35;
        transform: translateY(5px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @media (max-width: 720px) {
      .page {
        width: calc(100% - 26px);
        padding-top: 17px;
      }

      .topline-note {
        max-width: 140px;
        font-size: 0.58rem;
      }

      .hero {
        display: block;
        min-height: 0;
        padding: 34px 24px 42px;
        border-radius: 26px;
      }

      h1 {
        font-size: clamp(3rem, 12vw, 4.2rem);
      }

      .hero-text {
        max-width: 420px;
        font-size: 0.98rem;
      }

      .hero-illustration {
        position: absolute;
        right: -25px;
        bottom: -34px;
        width: 195px;
        opacity: 0.25;
      }

      .twinkle-one {
        top: 3%;
        right: 10%;
      }

      .twinkle-two {
        top: 44%;
        left: -4%;
      }

      .content-grid {
        grid-template-columns: 1fr;
      }

      .reminder-text {
        min-height: auto;
      }

      footer {
        flex-direction: column;
        text-align: center;
      }
    }

    @media (max-width: 390px) {
      .topline-note {
        max-width: 115px;
        line-height: 1.5;
      }

      .hero {
        padding-right: 20px;
        padding-left: 20px;
      }

      h1 {
        font-size: 2.8rem;
      }
    }

    @media (prefers-reduced-motion: reduce) {
      *,
      *::before,
      *::after {
        scroll-behavior: auto !important;
        animation-duration: 0.01ms !important;
        animation-iteration-count: 1 !important;
        transition-duration: 0.01ms !important;
      }
    }
  </style>
</head>

<body>
  <main class="page">
    <header class="topline">
      <a class="brand" href="#" aria-label="A little note from Abi">
        <span class="brand-icon" aria-hidden="true">✦</span>
        <span>A LITTLE NOTE</span>
      </a>
      <span class="topline-note">A LITTLE SOMETHING JUST FOR YOU</span>
    </header>

    <section class="hero" aria-labelledby="page-title">
      <div class="hero-copy">
        <p class="eyebrow">A LITTLE NOTE FROM ABI</p>
        <h1 id="page-title">Your dance cover<br><span>deserves applause.</span></h1>
        <p class="hero-text">
          A quiet comment section can feel disappointing, but it can’t measure
          your talent, your effort, or all the wonderful things that make you you.
        </p>
      </div>

      <div class="hero-illustration" aria-hidden="true">
        <span class="twinkle twinkle-one">✦</span>
        <span class="twinkle twinkle-two">✧</span>

        <!-- A little bouquet of tulips -->
        <svg viewBox="0 0 360 340" xmlns="http://www.w3.org/2000/svg">
          <circle cx="180" cy="170" r="145" fill="#eee6fb"/>
          <circle cx="180" cy="170" r="127" fill="none" stroke="#ffffff" stroke-opacity=".65" stroke-width="2"/>

          <!-- Decorative stars -->
          <path d="M75 87l4 10 10 4-10 4-4 10-4-10-10-4 10-4z" fill="#fff" opacity=".95"/>
          <path d="M278 71l3 8 8 3-8 3-3 8-3-8-8-3 8-3z" fill="#b99cdd"/>
          <path d="M286 213l2.5 6.5 6.5 2.5-6.5 2.5-2.5 6.5-2.5-6.5-6.5-2.5 6.5-2.5z" fill="#fff"/>
          <circle cx="91" cy="190" r="3" fill="#b99cdd"/>
          <circle cx="259" cy="93" r="2.5" fill="#fff"/>

          <!-- Stems -->
          <g fill="none" stroke="#7eaa8b" stroke-linecap="round" stroke-width="7">
            <path d="M180 151c-3 43-3 90 0 141"/>
            <path d="M119 180c7 42 22 78 50 113"/>
            <path d="M241 170c-8 48-24 89-55 123"/>
          </g>

          <!-- Leaves -->
          <path d="M167 247c-24-31-56-36-76-29 12 28 39 43 78 38z" fill="#90b69a"/>
          <path d="M190 258c23-31 53-38 76-29-13 30-40 45-78 39z" fill="#83aa8e"/>
          <path d="M164 277c-23-19-46-21-62-13 15 21 36 29 65 25z" fill="#a1c2a4"/>
          <path d="M195 281c19-20 42-24 59-17-13 22-34 32-63 29z" fill="#9abb9b"/>

          <!-- Left tulip -->
          <path d="M119 184c-23-1-29-20-23-47 9 8 17 3 23-19 7 24 15 27 24 19 5 27-2 46-24 47z" fill="#dfa5d0"/>
          <path d="M119 122c-2 20-2 41 0 59" fill="none" stroke="#f7d7ec" stroke-linecap="round" stroke-width="3"/>
          <path d="M97 143c5 20 11 29 22 36" fill="none" stroke="#f3c5e3" stroke-linecap="round" stroke-width="2"/>

          <!-- Right tulip -->
          <path d="M241 174c-23-1-29-20-23-47 9 8 17 3 23-19 7 24 15 27 24 19 5 27-2 46-24 47z" fill="#b69bdf"/>
          <path d="M241 112c-2 20-2 41 0 59" fill="none" stroke="#e4d6f6" stroke-linecap="round" stroke-width="3"/>
          <path d="M219 133c5 20 11 29 22 36" fill="none" stroke="#d8c6f0" stroke-linecap="round" stroke-width="2"/>

          <!-- Tall middle tulip -->
          <path d="M180 158c-25-1-32-22-27-53 10 9 19 4 27-27 9 31 18 36 28 27 5 31-2 52-28 53z" fill="#9473c7"/>
          <path d="M180 82c-2 25-2 51 0 73" fill="none" stroke="#d8c8ef" stroke-linecap="round" stroke-width="3"/>
          <path d="M155 105c6 24 14 38 25 48" fill="none" stroke="#c5afe6" stroke-linecap="round" stroke-width="2"/>
          <path d="M205 105c-6 24-14 38-25 48" fill="none" stroke="#c5afe6" stroke-linecap="round" stroke-width="2"/>

          <!-- A tiny ribbon around the stems -->
          <path d="M156 291c16 8 33 8 49 0l-4 17c-13 7-27 7-40 0z" fill="#d9b9e8"/>
          <path d="M164 298l-13 17 19-5m27-12 13 17-19-5" fill="#c8a8de"/>
          <circle cx="181" cy="299" r="7" fill="#f5eafb"/>
        </svg>
      </div>
    </section>

    <section class="content-grid" aria-label="A note and reminders for Varshi">
      <article class="letter-card">
        <p class="section-label">A NOTE FOR VARSHI</p>

        <p class="salutation">Hey Varshi,</p>

        <p>
          I know it can feel disappointing to share a dance cover and find the
          comments quiet. But it’s not only about the comments. I want you to
          know that I think everything you do is amazing. I notice the effort
          and heart you put into things, and I hope you remember how special that is.
        </p>

        <p>
          I know I can overdo things sometimes, and yes, I used AI to help make
          this page. I had a hard time researching how to build something like
          this when I didn’t have a single idea where to start, but I still
          wanted to make something for you. So yeah, I hope you feel a little better.
        </p>

        <p>
          Also, there’s a “Give me another reminder” button. Just press it and
          you’ll get another reminder each time.
        </p>

        <p class="signoff">
          I’m cheering you on,<br>
          <strong>Abi</strong>
        </p>
      </article>

      <aside class="reminder-card" aria-labelledby="reminder-heading">
        <span class="reminder-icon" aria-hidden="true">✦</span>
        <h2 id="reminder-heading">A gentle reminder</h2>
        <span class="reminder-count" id="reminder-count">REMINDER 1 OF 100</span>

        <p class="reminder-text" id="reminder-text" aria-live="polite">
          Varshi, you are allowed to feel proud of how far you've come.
        </p>

        <p class="reminder-help">
          There are 100 little reminders. Tap the button whenever you want another.
        </p>

        <button id="reminder-button" type="button">
          Give me another reminder
        </button>
      </aside>
    </section>

    <footer>
      <span>A little note, made with care by Abi.</span>
      <span>One post is just one moment.</span>
    </footer>
  </main>

  <script>
    const reminders = [
      // 1–10
      "Varshi, you are allowed to feel proud of how far you've come.",
      "Your effort matters, even when nobody sees all of it.",
      "One quiet post cannot define your talent.",
      "You deserve kindness from yourself, too.",
      "Every time you keep trying, you're building confidence.",
      "Your creativity is worth sharing at your own pace.",
      "It takes courage to put something you love out into the world.",
      "Your dance journey doesn't have to look like anyone else's.",
      "You don't have to be perfect to be worth celebrating.",
      "A slow beginning is still a beginning.",

      // 11–20
      "Your progress can be real even when it's hard to notice.",
      "You bring your own style to what you create.",
      "It's okay to take a break and come back when you're ready.",
      "You are more than the numbers on a screen.",
      "Your happiness matters more than chasing approval.",
      "Practice is progress, even when it feels small.",
      "The things you make can matter before anyone comments.",
      "Keep the parts of dancing that make you feel alive.",
      "Your effort is something you can be proud of.",
      "You don't need to rush your growth.",

      // 21–30
      "Being new doesn't make you any less worthy of support.",
      "You deserve to celebrate small wins.",
      "It is okay to feel disappointed without giving up on yourself.",
      "Your voice and style belong here.",
      "You've already done something brave by sharing your work.",
      "You can learn as you go; nobody starts knowing everything.",
      "One day doesn't tell the whole story of your journey.",
      "Your dedication is worth noticing.",
      "You get to create for joy, not just for reactions.",
      "You are allowed to be a beginner and still be proud.",

      // 31–40
      "The right audience can take time to find you.",
      "Your value doesn't change with the number of comments.",
      "What you do with heart is worth something.",
      "You've got permission to grow at your own pace.",
      "Your ideas deserve room to develop.",
      "Even small steps move you forward.",
      "It's okay if today feels hard; it won't always feel this way.",
      "You don't have to earn rest.",
      "Every bit of practice adds to your journey.",
      "You have more to offer than one post can show.",

      // 41–50
      "Your courage is already something to celebrate.",
      "Keep learning, keep creating, and be gentle with yourself.",
      "A quiet moment online isn't proof that nobody cares.",
      "You are allowed to enjoy your progress before it's perfect.",
      "Your creativity makes your work your own.",
      "You deserve encouragement, including from yourself.",
      "You can be proud of trying, whatever the response is.",
      "There is no single timeline for success.",
      "You are still growing, and that's a good thing.",
      "Your next step doesn't need to be a giant leap.",

      // 51–60
      "Make room for the fun that made you start dancing.",
      "You are allowed to celebrate yourself without waiting for likes.",
      "You don't need everyone's approval to keep enjoying what you do.",
      "Each time you show up, you give yourself another chance to grow.",
      "Your passion is worth protecting from pressure.",
      "You can pause, breathe, and decide what feels right next.",
      "You don't have to compare your beginning to someone else's highlight.",
      "Your work deserves care, and so do you.",
      "You are allowed to change, experiment, and find your style.",
      "A small audience can still be a meaningful start.",

      // 61–70
      "Keep being curious about what you can create.",
      "You can be proud of the effort even if the outcome wasn't what you hoped.",
      "You aren't behind; you're on your own path.",
      "Your joy is a good reason to keep dancing.",
      "The world doesn't need you to be a copy of anyone.",
      "Your unique spark comes from being yourself.",
      "You can learn from a quiet post without judging yourself.",
      "Your feelings are valid, and so is your hope.",
      "You deserve the same patience you give other people.",
      "You are doing better than you think, one step at a time.",

      // 71–80
      "Let your progress be personal, not a competition.",
      "You can start again whenever you're ready.",
      "There is strength in making something and sharing it.",
      "Your dreams are allowed to take time.",
      "You don't have to have it all figured out today.",
      "Give yourself credit for the work you put in.",
      "You can be nervous and brave at the same time.",
      "Even imperfect attempts help you improve.",
      "Your creativity is not measured by engagement.",
      "It's okay to ask for support when you need it.",

      // 81–90
      "You make the journey brighter just by showing up as yourself.",
      "Keep the memories and lessons from each time you try.",
      "Your self-worth stays the same on quiet days.",
      "You are allowed to feel proud and still want to improve.",
      "Small improvements deserve recognition.",
      "Your hard work is part of your story.",
      "Take things one dance, one post, and one day at a time.",
      "You don't have to prove your worth to anyone.",
      "What matters to you is worth making time for.",
      "Your future audience hasn't seen all you'll create yet.",

      // 91–100
      "A kind word from yourself can make a difference.",
      "You can let today be a tough day without making it a tough future.",
      "Your patience with yourself is part of growth.",
      "You deserve to enjoy the process, not just the results.",
      "Your courage today can inspire your confidence tomorrow.",
      "Keep your standards kind as you keep growing.",
      "You bring something only you can bring.",
      "There is room for you to improve and be amazing right now.",
      "Celebrate the fact that you tried, Varshi.",
      "Abi is cheering you on, and I hope you keep being you."
    ];

    const reminderText = document.getElementById("reminder-text");
    const reminderCount = document.getElementById("reminder-count");
    const reminderButton = document.getElementById("reminder-button");

    let currentIndex = 0;

    reminderButton.addEventListener("click", () => {
      currentIndex = (currentIndex + 1) % reminders.length;

      reminderText.classList.remove("is-changing");
      void reminderText.offsetWidth;

      reminderText.textContent = reminders[currentIndex];
      reminderText.classList.add("is-changing");
      reminderCount.textContent =
        `REMINDER ${currentIndex + 1} OF ${reminders.length}`;
    });
  </script>
</body>
</html>
```
