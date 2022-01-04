# T306-JS_intro (2020.10.12/13)
## -------INFO
```

1. Intro
2. Syntax
3. Types
4. Flow control
5. Functions
6. Objects
7. DOM

```

```
ZADT30601
Przygotuj sterowanie kwadratowym elementem z uzyciem buttonów (arrows).

```

```html
...............

        <input id="btnprev" type="button" value="<">

        <img id="myimg" src="https://images.pexels.com/photos/5725972/pexels-photo-5725972.jpeg?auto=compress&cs=tinysrgb&h=650&w=940" alt="img">

        <input id="btnnext" type="button" value=">">

        <script>
            const btnprev = document.getElementById('btnprev');
            const btnnext = document.getElementById('btnnext');
            const img = document.getElementById('myimg');

            let counter = 0;

            const obrazki = [
                'https://images.pexels.com/photos/5725972/pexels-photo-5725972.jpeg?auto=compress&cs=tinysrgb&h=650&w=940',
                'https://images.pexels.com/photos/10069506/pexels-photo-10069506.jpeg?auto=compress&cs=tinysrgb&h=650&w=940',
                'https://images.pexels.com/photos/7997389/pexels-photo-7997389.jpeg?auto=compress&cs=tinysrgb&h=650&w=940',
                'https://images.pexels.com/photos/10314318/pexels-photo-10314318.jpeg?auto=compress&cs=tinysrgb&h=650&w=940'
            ];

            //const obrazki1 = [];
            //const obrazki2 = new Array();

            btnprev.addEventListener('click',function (){zmien('prev')});
            btnnext.addEventListener('click',() => zmien('next'));

            function zmien(jak){
                if(jak == 'prev'){
                    console.log('poprzedni',counter,obrazki[counter])
                    if(counter > 0){
                        counter--;
                    } else {
                        counter = obrazki.length -1;
                    }
                    //conter = counter - 1
                } else {
                    console.log('nastepny',obrazki.length,counter,obrazki[counter])
                    if(counter < obrazki.length - 1){
                        counter++;
                    } else {
                        counter = 0;
                    }
                    //conter = counter + 1
                }                    
                img.src = obrazki[counter];
            }
        </script>
          
................
```

### --------Links
https://github.com/T3iL/T303-CSS

GOOGLE DRIVE: https://drive.google.com/drive/folders/1OqTcjwr_qAdTPO-dThxUOd3ooTTOlzgp?usp=sharing

https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css

https://www.w3.org | https://validator.w3.org | https://www.php.net/manual/en/
### --------Repositiories
https://www.w3schools.com | https://stackoverflow.com | https://css-tricks.com |
### --------On line editors
https://codepen.io/ | https://codesandbox.io/ | https://jsfiddle.net/ |
### ---------Assets
https://cdnjs.com/ | https://fontawesome.com | http://fontello.com/ | https://fonts.google.com/ | https://www.flaticon.com/
### ---------Stock Img
https://www.pexels.com/ | https://unsplash.com | https://pixabay.com
### ---------Tuts
https://www.youtube.com/watch?v=1Rs2ND1ryYc
https://www.youtube.com/watch?v=J35jug1uHzE
https://www.youtube.com/watch?v=ieTHC78giGQ
### ---------License
[MIT](https://choosealicense.com/licenses/mit/)
