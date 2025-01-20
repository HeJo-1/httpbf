
# HTTP Brute Force Aracı

Bu Python tabanlı araç, bir hedef URL'ye ve belirtilen bir wordlist dosyasındaki şifreleri deneyerek formu doldurur.

---

## Kullanım

**Komut:**
```bash
python main.py -u <URL> -w <WORDLIST_PATH> -i <INPUT_ID>
```

### Parametreler:

- **`-u` / `--url`**: Hedef URL. 
  - Örnek: `https://example.com/login`

- **`-w` / `--wordlist`**: Şifrelerin bulunduğu `.txt` dosyasının yolu. 
  - Örnek: `wordlist.txt`

- **`-i` / `--input-id`**: Formda yer alan şifre alanının `id` değeri. 
  - Örnek: `password`

---

### Örnek Kullanım:

```bash
python main.py -u https://dosya.co/login -w passwords.txt -i pass_input
```

- **URL**: `https://dosya.co/login` hedef URL'si.
- **Wordlist Dosyası**: `passwords.txt`.
- **Şifre Input ID**: `pass_input`.

---

### Çıktı:

Araç çalıştırıldığında, şifreler tek tek denenir ve aşağıdaki formatta çıktı üretir:

- **Başarısız Deneme:**
  ```
  Şifre: password123 | Sonuç: Şifre yanlış
  ```

- **Başarılı Deneme:**
  ```
  Şifre: admin123 | Yanıt: 
  ...
  Doğru şifre bulundu: admin123
  ```

---

### Dikkat

- Bu araç yalnızca izinli sistemler üzerinde test amaçlı kullanılmalıdır. İlgili kanunlara aykırı olarak kullanımı ciddi hukuki sonuçlar doğurabilir.
- Sorumluluk tamamen kullanıcıya aittir.
