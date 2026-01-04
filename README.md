# Selector-de-cor
Um pequeno programa feito com HTML, CSS e JavaScript. Que altera a cor de fundo de acordo com a cor selecionada pelo usuário. 

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Document</title>
  <style>
  body{
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: Times New Roman;
  }
    #para{
      text-align: center;
      color: red;
    }
    button{
      padding: 20px;
      margin-left: 10px;
      width: 150px;
      font-family: Times New Roman;
      border-radius: 20px;
    }
    .meudiv{
      width: 500px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      
      border-radius: 20px;
      box-shadow: 4px 4px 4px 8px rgb(198,198,198);
    }
    input{
      border: 1px solid black;
      border-radius: 20px;
      font-family: Times New Roman;
    }
    input:focus{
      border:1px solid black;
      outline: none;
    }
  </style>
</head>
<body>
  <div class="meudiv">
    <h1>Selector de cor</h1>
  <input style="padding: 20px; margin:10px;" type="text" id="cor" placeholder="digite uma cor"><br>
  <button onclick="cique()">Clica aqui</button>
  <p id="para"></p>
  </div>
</body>
<script>
  function cique(){
  let alterar=document.getElementById("cor").value;
  alterar=alterar.toLowerCase();
  switch(alterar){
    case "azul":
      document.body.style.backgroundColor="blue"
      button=document.querySelector('button');
      button.style.borderColor="white"
      button.style.backgroundColor="blue";
      break;
      case "vermelho":
        document.body.style.backgroundColor="red"
        button=document.querySelector('button');
        button.style.borderColor="white"
      button.style.backgroundColor="red";
        break;
        case "verde":
          document.body.style.backgroundColor="green"
          button=document.querySelector('button');
          button.style.borderColor="white"
      button.style.backgroundColor="green";
          break;
          case"rosa":
            document.body.style.backgroundColor="pink"
            button=document.querySelector('button');
            button.style.borderColor="white"
      button.style.backgroundColor="pink";
            break;
            case"castanho":
              document.body.style.backgroundColor="brown"
              button=document
              .querySelector('button');
              button.style.borderColor="white"
      button.style.backgroundColor="brown";
         break;
         case"preto":
           document.body.style.backgroundColor="black"
              button=document
              .querySelector('button');
              button.style.borderColor="white"
      button.style.backgroundColor="black";
      button.style.color="white";
          break; 
          case"branco":
            
            document.body.style.backgroundColor="white"
              button=document
              .querySelector('button');
              button.style.borderColor="black"
      button.style.backgroundColor="white";
      button.style.color="black";
            break;
          default:
          document.getElementById("para").innerHTML="Cor não encontrado!"
  }
  }
</script>
</html>