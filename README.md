# code
<--The front end code for the project--/>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>price comparisonar</title>
</head>
<body>
  <style>
        *{
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins',sans-serif;
        } 
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background: url('shoppipng.jpg') no-repeat;
            background-size: cover;
            background-position: center;
        }
        header{
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            padding: 20px 100px;
            background: rgb(255, 0, 187);
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 99;
        }  
        .logo{
            font-size: 2em;
            color: #fff;
            user-select: none;
        }
        .navigation a{
            position: relative;
            font-size: 1.1em;
            color: #fff;
            text-decoration: none;
            font-weight: 500;
            margin-left: 40px;
        }
        .navigation a::after{
           content: '';
           position: absolute;
           left: 0;
           bottom: -6px;
           width: 100%;
           height: 3px;
           background: #fff;
           border-radius: 5px;
           transform-origin: top;
           transform: scaleX(0);
           transition: transform .5s;
           
        }
        .navigation a:hover::after{
            transform-origin: top;
            transform: scaleX(1)
        }
        .navigation .btnLogin-popup{
            width: 130px;
            height: 50px;
            background: transparent;
            border: 2px solid #fff;
            outline: none;
            border-radius: 6px;
            cursor: pointer;
            font-size: 1.1em;
            color: #fff;
            font-weight: 500;
            margin-left: 40px;
            transition: .5s;
        }
        .navigation .btnLogin-popup:hover {
            background: #fff;
            color: #162938;
        } 
        .wrapper{
            position: relative;
            width: 400px;
            height: 440px;
            background: transparent;
            border: 2px solid rgba(255, 255, 255, .5);
            border-radius: 20px;
            backdrop-filter: blur(30px);
            box-shadow: 0 0 30px rgba(0, 0, 0, .5);
            display: flex;
            justify-content: center;
            align-items: center;

        }  
        .wrapper .form-box{
            width: 100%;
            padding: 40px;

        }
        .form-box h2{
            font-size: 2em;
            color: #162938;
            text-align: center;
        }
        .input-box{
            position: relative;
            width: 100%;
            height: 50px;
            border-bottom: 2px  solid #162938;
            margin: 30px 0;
        }
        .input-box label{
            position: absolute;
            top: 50%;
            left: 5px;
            transform: translateY(-50%);
            font-size: 1em;
            color: #162938;
            font-weight: 500;
            pointer-events: none;
            transition: .5s;
        }
        .input-box input:focus~label,
        .input-box input:valid~label{
            top: -5px;
        }
        
        .input-box input{
            width: 100%;
            height: 100%;
            background: transparent;
            border: none;
            outline: none;  
            font-size: 1em;
            color: #162938;
            font-weight: 600;    
            padding: 0 35px 0 5px;     
        }
        .remember-forget{
          font-size: .9em;
          color: #162938;
          font-weight: 500;
          margin: -15px 0 15px;
          display: flex;
          justify-content: space-between;  
        }
        
        .btn{
            width: 100%;
            height: 45px;
            cursor: pointer;
        }
        .login-register {
            font-size: .9em;
          color: #162938;
          text-align: center;
          font-weight: 500;
          margin: 25px 0 10px;
        }
        .login-register p a:hover{
            text-decoration:underline ;
            
        }


    </style> 
    <header>
        <h2 class="logo">Logo</h2>
        <nav class="navigation">
            <a href="#">Home</a>
            <a href="#">About</a>
            <a href="#">Services</a>
            <a href="#">Contact</a>
            <button class="btnLogin-popup">Login</button>

        </nav>
    </header>
    <div class="wrapper">
        <div class="form-box login"> 
            <h2>Login</h2>
            <form action="#">
                <div class="input-box">
                    <span class="icon">
                    </span>
                    <input type="email" required>
                    <label>Email</label>
                </div>
                <div class="input-box">
                    <span class="icon">
                    </span>
                    <input type="password" required>
                    <label>Password</label>  
                </div>
                <div class="remember-forget">
                    <label><input type="checkbox">Remember me</label>
                    <a href="#">Forget Password</a>

                </div>
                <button type="submit" class="btn">Login</button>
                <div class="login-register">
                    <p>Don't have an account?
                        <a href="#" class="register-link">Register</a>
                    </p>
                </div>
            </form>
        </div>
    </div>
</body>
</html>