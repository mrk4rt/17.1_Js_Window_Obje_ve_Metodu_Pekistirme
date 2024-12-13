# JavaScript Uygulama Soruları ve Çözümleri

## Soru 1: Sayfa Başlığını Güncelleme
**Soru:** Kullanıcıdan bir metin isteyin ve bunu `document.title` kullanarak sayfa başlığına atayın. Eğer kullanıcı bir şey girmezse, ekrana bir uyarı gösterin.

**Çözüm:**
```javascript
let userInput = window.prompt("Lütfen yeni sayfa başlığını girin:");
if (userInput) {
    document.title = userInput;
} else {
    window.alert("Başlık boş bırakılamaz!");
}
```

---

## Soru 2: Ekran Boyutunu Gösterme
**Soru:** Tarayıcı penceresinin genişliğini ve yüksekliğini konsola yazdırın. Daha sonra, pencere boyutlandırıldığında yeni genişlik ve yükseklik değerlerini de gösterin.

**Çözüm:**
```javascript
console.log(`Başlangıç genişlik: ${window.innerWidth}, yükseklik: ${window.innerHeight}`);

window.addEventListener("resize", () => {
    console.log(`Genişlik: ${window.innerWidth}, Yükseklik: ${window.innerHeight}`);
});
```

---

## Soru 3: Sayfa Yönlendirme
**Soru:** Kullanıcıdan bir URL alın ve `window.location.href` kullanarak onu bu URL'ye yönlendirin. Kullanıcı bir şey girmezse ekrana "Lütfen bir URL girin" şeklinde bir uyarı gösterin.

**Çözüm:**
```javascript
let url = window.prompt("Gitmek istediğiniz URL'yi girin:");
if (url) {
    window.location.href = url;
} else {
    window.alert("Lütfen bir URL girin!");
}
```

---

## Soru 4: Zamanlayıcı Mesaj Gösterimi
**Soru:** Bir `setTimeout` kullanarak 5 saniye sonra ekrana bir mesaj (`window.alert`) gösteren bir uygulama yazın. Gösterimden önce zamanlayıcıyı iptal etme seçeneği ekleyin.

**Çözüm:**
```javascript
let timer = setTimeout(() => {
    window.alert("5 saniye geçti!");
}, 5000);

let cancel = window.confirm("Zamanlayıcıyı iptal etmek istiyor musunuz?");
if (cancel) {
    clearTimeout(timer);
    console.log("Zamanlayıcı iptal edildi.");
}
