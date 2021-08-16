<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>🌅Miracle-morning!</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.0/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-KyZXEAg3QhqLMpG8r+8fhAXLRk2vvoC2f3B09zVXn8CA5QIVfZOJ3BCsw2P0p/We" crossorigin="anonymous">
  <link rel="stylesheet" href="main.css">
</head>
<body>

  <nav class="navbar navbar-light" style="background-color: #5D5CC4;">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">🌅Miracle-morning</a>
    </div>
  </nav>

  <nav class="navbar navbar-expand-lg navbar-light" style="background-color: #5D5CC4;" >
    <div class="container-fluid">
      <span class="navbar-text">
        당신의 미라클 모닝 다이어리🤭
      </span>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="#">전체보기👀</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">공부👩‍💻</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">다이어트💪</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">운동🏃‍♀️</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">독서📚</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">기타🎸</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  안녕하세요! 당신의 아침을 깨우는 미라클모닝입니다! :)

  <div class="container mt-3">
    <!-- <div class="product">
      <div class="thumbnail" style="background-image: url('https://via.placeholder.com/350')"></div>
      <div class="flex-grow-1 p-4">
        <h5 class="title">아기다스 신발</h5>
        <p class="date">2030년 1월 8일</p>
        <p class="price">20000원</p>
        <p class="float-end">🤍0</p>
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
  db.collection('diary').get().then((결과)=>{
    결과.forEach((doc)=>{
      console.log(doc.data());
      var 템플릿 = `<div class="product">
      <div class="thumbnail" style="background-image: url('https://via.placeholder.com/350')"></div>
      <div class="flex-grow-1 p-4">
        <h5 class="name">${doc.data().닉네임}</h5>
        <p class="date">${doc.data().기록시간}</p>
        <p class="category">${doc.data().카테고리}</p>
        <p class="float-end">🤍0</p>
      </div>
      </div>`;
      $('.container').append(템플릿)
    })
  })

</script>

</body>
</html>
