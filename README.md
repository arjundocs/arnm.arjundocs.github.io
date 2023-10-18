<html>
    <head>
        <title>Revoto Admin | Revoto.in</title>
        <link rel="stylesheet" href="style.css">
    </head>
    <body>
        <div class="box">
            <div class="form">
                <h2>Login Form</h2>
                <form>
                    <div class="inputbox">
                        <input type="text" value="" id="username" required>
                        <span>username</span>
                    </div>
                    <div class="inputbox">
                        <input type="email" value="" id="email" required>
                        <span>E-mail</span>
                    </div>
                    <div class="inputbox">
                        <input type="text" value="" id="phone" required>
                        <span>Phone Number</span>
                    </div>
                    <input type="submit" value="submit" class="sub" id="submit">
                </form>
            </div>
        </div>
        <script type="module">
               // Import the functions you need from the SDKs you need
               import { initializeApp } from "https://www.gstatic.com/firebasejs/10.5.0/firebase-app.js";
            import { getDatabase, ref, set, get, child } from "https://www.gstatic.com/firebasejs/10.5.0/firebase-app.js";
  
//   // Your web app's Firebase configuration
//             const firebaseConfig = {
//               apiKey: "AIzaSyAkPgAR0Hs6v5oNlmxYxI2OGh-S8YA2OWU",
//               authDomain: "creativetutorial-43ba7.firebaseapp.com",
//               projectId: "creativetutorial-43ba7",
//               storageBucket: "creativetutorial-43ba7.appspot.com",
//               messagingSenderId: "52869654198",
//               appId: "1:52869654198:web:0a19740d1f26ade1066817"
//             };

//   // Initialize Firebase
//             const app = initializeApp(firebaseConfig);

            // import { initializeApp } from "https://www.gstatic.com/firebasejs/10.5.0/firebase-app.js";
  // TODO: Add SDKs for Firebase products that you want to use
  // https://firebase.google.com/docs/web/setup#available-libraries

  // Your web app's Firebase configuration
  const firebaseConfig = {
    apiKey: "AIzaSyBc9xwyccwWaGjWsI7F_TYChsSvqf_ocCg",
    authDomain: "rewardsq-3cef2.firebaseapp.com",
    projectId: "rewardsq-3cef2",
    storageBucket: "rewardsq-3cef2.appspot.com",
    messagingSenderId: "317576263316",
    appId: "1:317576263316:web:52222689e35b794efaa681"
  };

  // Initialize Firebase
  const app = initializeApp(firebaseConfig);

   //get ref to database services
             const db = getDatabase(app);

             document.getElementById("submit").addEventListener('click', function(e){
              e.preventDefault();
              set(ref(db, 'user/' + document.getElementById("username").value),
              {
   
                username: document.getElementById("username").value,
                email: document.getElementById("email").value,
                PhoneNumber: document.getElementById("phone").value

              });
                alert("Login Sucessfull  !");
             })
        </script>
    </body>
</html>
