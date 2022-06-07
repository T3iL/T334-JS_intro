# T334-JS_intro

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
LIVE SHARE LINK:
https://prod.liveshare.vsengsaas.visualstudio.com/join?00AFCDF6BC999F8CD2656224FD65B319395F

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

```javascript
        const container = document.createElement('div')
        document.body.appendChild(container);

        function dodaj(){
            const newDiv = document.createElement('div')
            newDiv.id = "nowyDiv";
            newDiv.classList.add('czerwony')
            newDiv.style.border = '1px solid'
            newDiv.innerHTML = content;

            container.appendChild(newDiv);
        }
```

```
ZADT30601
T33401 - Przygotuj sterowanie kwadratowym elementem z uzyciem buttonów (arrows).

T33402 - Przygotuj skrypt wstawiający po kliknięciu cegłę do kontenera. Cegły buduja mur. 
Mur buduje się od dolnej krawędzi strony i może być wyższy niz strona.
- dodaj teksturę do cegieł (gradient/pattern)
- upewnij się że cegły budują się prawidłowo (na zakładkę)
- losuj odcień cegieł (każda ma inny odcień)
- zanimuj spadanie cegieł z góry podczas budowania

T33403 - (do 2022.05.31) - Przygotuj stronę html wyświetlającą karty profilowe z danymi pobranymi z tablicy. 
(Zastosuj css do sformatowania zgodnie z rysunkiem - Rys 1.)
- dane użytkowników pobierz z https://gist.github.com/rubenCodeforges/ef1f0ce6a055bbb985c0848d8b0c04d5
- zastąp placeholdery obrazów zdjęciami stockowymi (np: https://randomuser.me/api/portraits/women/24.jpg)
- kolory : colors = ["#74fed6","#9fc1fe","#acc0e9","#9bd9ff","#a4d0e8","#ffc7e3","#fed8ae","#ffd7ae","#ff97a4"]
- opis wypełnij lorem ipsum

DODATKOWA FUNKCJONALNOSĆ:
- odwrócenie kolejności
- filttrowanie (K/M)
- usuwanie
- dodawanie
- drag and drop


T334004 - Przygotuj zegar z obręczami zamiast wskazówek wskazujący rzeczywisty czas. (Canvas)
 Zastosuj Koła o odpowiednio pbliczonym zakresie zgodnie z rys 2)

T334004 - Sprawdzian z podstaw Java script (zmienne, instr. warunkowe, pętle, tablice) DATA: 10.05.2022
```

![Rys 1](./Cards.PNG)

![Rys 2](./Clock.PNG)

Kartkówka ZAD5 - Przygotuj stronę pokazaną na poniższej ilustracji pamiętając o traktowaniu łańcuchów znaków jak tablicy.
- treść generowana jest dynamicznie (przy pomocy Javascript) i pobierana z tablicy imiona
```code
        const imiona = ['Eliasz','Ildefons','Chwalibóg','Adalbert','Łazarz','Genowefa','Zbysław','Serafin','Ulryk','Wawrzyniec','Kilian','Telimena','Hawier','Barnaba','Oktawiusz','Vanesa','Regina','Nicefor','Ścibor','Pantaleon','Marcjanna','Laurencja','Jakobina','Felicyta','Demetria'];
```
- W szarych kółkach o rozmiarze 150px X 150px, z czerwoną obwódką o grubości 10px, wyświetlają się pierwsze litery imion z tablicy.
- Kolor tekstu: biały, font: Verdana, rozmiar tekstu: 4em, rozmiar indeksu: 1rem
- obok liter w indeksie (w nawiasie) umieszczona jest długość imienia (ilość znaków) obliczona automatycznie
- contener z kółkami wycentrowany w obu kierunkach
- kółka "przepływają" do nowej lini gdy sięnie mieszczą (wrap) tak jak na ilustracji

```code
        const imiona = ['Eliasz','Ildefons','Chwalibóg','Adalbert','Łazarz','Genowefa','Zbysław','Serafin','Ulryk','Wawrzyniec','Kilian','Telimena','Hawier','Barnaba','Oktawiusz','Vanesa','Regina','Nicefor','Ścibor','Pantaleon','Marcjanna','Laurencja','Jakobina','Felicyta','Demetria'];
```


![Spr](./Initials3.JPG)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id="container"></div>
    <script>
        const container = document.getElementById('container')
        //IF
        let a = 10;
        let b = '10';

        if (a > 5 || a < 10) { // && || AND OR
            console.log('jest między 5 a 10')
        } else {
            console.log('nie jest równe')
        }

        // switch

    switch(a){
        case 5:
            console.log('jest równe 5')
        break;
        case 10:
            console.log('jest równe 10')
        break;
        case 15:
            console.log('jest równe 15')
        break;
        default:
            console.log('inne')
        break;
    }

    //PĘTLE

    let i = 0;

    while(i < 10){
        // console.log('I-',i);
        i++;
    }

    let j = 0;

    do {
        // console.log('J-',j);
        j++;
    } while (j < 10)

    let k = 0;

    for(k; k < 10; k++){
        // console.log('K-',k);
    }

    const imiona = ['Eliasz','Ildefons','Chwalibóg','Adalbert','Łazarz','Genowefa','Zbysław','Serafin','Ulryk','Wawrzyniec','Kilian','Telimena','Hawier','Barnaba','Oktawiusz','Vanesa','Regina','Nicefor','Ścibor','Pantaleon','Marcjanna','Laurencja','Jakobina','Felicyta','Demetria'];
    
    let tekst = '';

    for(let l = 0; l < imiona.length; l++){
        console.log(imiona[l])
    }   

    imiona.forEach(imie => {
        tekst += imie + ' ,';
    })

    container.innerHTML = tekst
    </script>
</body>
</html>
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
https://www.youtube.com/watch?v=OcwON22ctYc
https://www.youtube.com/watch?v=udxqsJXJM5Q
https://www.youtube.com/c/helloroman
### ---------License
[MIT](https://choosealicense.com/licenses/mit/)
