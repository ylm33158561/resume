
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        div{
            display: flex;
            position: relative;
            border: 1px solid red;
            height:40px;
            width:400px;
        }
        div>input[type='file']{
         cursor:pointer;
            height: 30px;
            width: 165px;
            position: absolute;
            right:0;
            cursor:pointer;
           opacity: 0;
        }
        div>input[type='text']{
            height: 25px;
            z-index: -1;
            width: 300px;
        }
        div>p{
            height: 30px;
            width: 90px;
            margin:0;
            background: blue;
            color: white;
            z-index: -1;
            text-align: center;
            line-height: 30px;
        }
    </style>
    <script src='./js/jquery-1.11.3.js'></script>
</head>
<body>

  <div id='main'>
      <input type="file"/>
      <input type='text'/><p>Brower</p>
  </div>
  <script>
      $('#main>input[type="file"]').on('change',()=>{
          var filepath = $('#main>input[type="file"]').val()
          var arr=filepath.split("\\")
          console.log(arr)
          $('#main>input[type="text"]').val(arr[arr.length-1])
      })
      
  </script>
</body>
</html>
