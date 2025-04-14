# card-profile<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Card Profile</title>
  <style>
    .card {
      width: 300px;
      background-color: #fff;
      border-radius: 20px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.6);
      padding: 20px;
      animation: fadein 0.5s ease-in-out;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    .avatar {
      width: 100px;
      height: 100px;
      border-radius: 50%;
      margin-bottom: 20px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
    }

    .info {
      text-align: center;
    }

    .name {
      font-size: 24px;
      color: #000;
      margin-bottom: 10px;
    }

    .description {
      font-size: 16px;
      color: #000;
      margin-bottom: 20px;
    }

    .follow-btn {
      background-color: #4CAF50;
      color: #fff;
      border: none;
      padding: 10px 20px;
      font-size: 16px;
      cursor: pointer;
      border-radius: 5px;
      transition: background-color 0.3s ease-in-out;
    }

    .follow-btn:hover {
      background-color: #3e8e41;
    }

    .follow-btn:focus {
      outline: none;
    }

    @keyframes fadein {
      0% {
        opacity: 0;
        transform: scale(0.5);
      }
      100% {
        opacity: 1;
        transform: scale(1);
      }
    }

    @media only screen and (max-width: 768px) {
      .card {
        width: 90%;
        margin: 20px auto;
      }
    }
  </style>
</head>
<body>
  <div class="card">
    <img src="https://i.imgur.com/iQrEWsx.jpeg" alt="Avatar" class="avatar">
    <div class="info">
      <h2 class="name">Dusk Soldier</h2>
      <p class="description">Dusk Soldier adalah seorang prajurit yang beroperasi di bawah naungan senja, membawa misi dan tugas yang memerlukan keahlian dan keberanian.</p>
      <button class="follow-btn">Follow</button>
    </div>
  </div>

  <script>
    const followBtn = document.querySelector('.follow-btn');

    followBtn.addEventListener('click', () => {
      if (followBtn.textContent === "Follow") {
        followBtn.textContent = "Following";
        followBtn.style.backgroundColor = "#2ecc71";
      } else {
        followBtn.textContent = "Follow";
        followBtn.style.backgroundColor = "#4CAF50";
      }
    });
  </script>
</body>
</html>
