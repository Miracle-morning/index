<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>๐Miracle-morning!</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.0/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-KyZXEAg3QhqLMpG8r+8fhAXLRk2vvoC2f3B09zVXn8CA5QIVfZOJ3BCsw2P0p/We" crossorigin="anonymous">
  <link rel="stylesheet" href="main.css">
</head>
<body>

  <nav class="navbar navbar-light" style="background-color: #5D5CC4;">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">๐Miracle-morning</a>
    </div>
  </nav>

  <nav class="navbar navbar-expand-lg navbar-light" style="background-color: #5D5CC4;" >
    <div class="container-fluid">
      <span class="navbar-text">
        ๋น์ ์ ๋ฏธ๋ผํด ๋ชจ๋ ๋ค์ด์ด๋ฆฌ๐คญ
      </span>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="#">์ ์ฒด๋ณด๊ธฐ๐</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">๊ณต๋ถ๐ฉโ๐ป</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">๋ค์ด์ดํธ๐ช</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">์ด๋๐โโ๏ธ</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">๋์๐</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">๊ธฐํ๐ธ</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  ์๋ํ์ธ์! ๋น์ ์ ์์นจ์ ๊นจ์ฐ๋ ๋ฏธ๋ผํด๋ชจ๋์๋๋ค! :)

  <div class="container mt-3">
    <!-- <div class="product">
      <div class="thumbnail" style="background-image: url('https://via.placeholder.com/350')"></div>
      <div class="flex-grow-1 p-4">
        <h5 class="title">์๊ธฐ๋ค์ค ์ ๋ฐ</h5>
        <p class="date">2030๋ 1์ 8์ผ</p>
        <p class="price">20000์</p>
        <p class="float-end">๐ค0</p>
      </div>
    </div> -->
  </div>



  <script src="https://www.gstatic.com/firebasejs/8.6.5/firebase-app.js"></script>
  <script src="https://www.gstatic.com/firebasejs/8.6.5/firebase-auth.js"></script>
  <script src="https://www.gstatic.com/firebasejs/8.6.5/firebase-firestore.js"></script>
  <script src="https://www.gstatic.com/firebasejs/8.6.5/firebase-storage.js"></script>

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.0/dist/js/bootstrap.bundle.min.js" integrity="sha384-U1DAWAznBHeqEIlVSCgzq+c9gqGAJn5c/t99JyeKa9xxaYpSvHU5awsuZVVFIhvj" crossorigin="anonymous"></script>

  <script src="https://code.jquery.com/jquery-3.6.0.min.js" integrity="sha256-/xUj+3OJU5yExlq6GSYGSHk7tPXikynS7ogEvDej/m4=" crossorigin="anonymous"></script>

  <script>
    var firebaseConfig = {
      apiKey: "AIzaSyArH0sl2K_wiipS0i4RxJJOBeZrxmUZ03M",
      authDomain: "miracle-morning-8bb63.firebaseapp.com",
      projectId: "miracle-morning-8bb63",
      storageBucket: "miracle-morning-8bb63.appspot.com",
      messagingSenderId: "184112856198",
      appId: "1:184112856198:web:1ca11a25055ab9cb462507",
      measurementId: "G-MMMYYY5H2Q"
    };
    // Initialize Firebase
    firebase.initializeApp(firebaseConfig);
  </script>

<script>
  const db = firebase.firestore();
  db.collection('diary').get().then((๊ฒฐ๊ณผ)=>{
    ๊ฒฐ๊ณผ.forEach((doc)=>{
      console.log(doc.data());
      var ํํ๋ฆฟ = `<div class="product">
      <div class="thumbnail" style="background-image: url('https://via.placeholder.com/350')"></div>
      <div class="flex-grow-1 p-4">
        <h5 class="name">${doc.data().๋๋ค์}</h5>
        <p class="date">${doc.data().๊ธฐ๋ก์๊ฐ}</p>
        <p class="category">${doc.data().์นดํ๊ณ ๋ฆฌ}</p>
        <p class="float-end">๐ค0</p>
      </div>
      </div>`;
      $('.container').append(ํํ๋ฆฟ)
    })
  })

</script>

</body>
</html>
