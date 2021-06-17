# demo.github.io<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Document</title>

  <style>
    body{
      /*给body添加透视景深，以便整体观察section的变化*/
      perspective: 1000px;
    }

    section {
      width: 346px;
      height: 250px;
      margin: 100px auto;
      background: url(images3/img-1.jpg);
      position: relative;
      /*让子元素在3d空间内呈现*/
      transform-style: preserve-3d;
      /* transform: rotate3d(1,1,0,45deg); */
      
      transition: transform 10s ease;
    }

    section:hover{
      transform: rotateY(360deg)
    }

    section div{
      position: absolute;
      width: 100%;
      height: 100%;
      left: 0px;
      top: 0px;
      background: url(images3/dog.gif) no-repeat;
      background-size: cover;
    }

    section div:first-child{
      transform: rotateY(0deg) translateZ(-400px);;
    }

    section div:nth-child(2){
      transform: rotateY(60deg) translateZ(-400px);;
    }

    section div:nth-child(3){
      transform: rotateY(120deg) translateZ(-400px);;
    }

    section div:nth-child(4){
      transform: rotateY(180deg) translateZ(-400px); ;
    }

    section div:nth-child(5){
      transform: rotateY(240deg) translateZ(-400px);;
    }

    section div:nth-child(6){
      transform: rotateY(300deg) translateZ(-400px);;
    }
  </style>
</head>

<body>
  <section>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
  </section>
</body>

</html>
