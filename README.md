Şilan EKİN 
silanekinceng@gmail.com
# Veri Seti ve Yapılan İşlemler

Bu proje, bir sağlık veri seti üzerinde **keşifsel veri analizi (EDA)** ve görselleştirme çalışmaları içerir. Veri seti, toplam 2235 hasta kaydından oluşmaktadır ve aşağıdaki bilgileri içerir:  

## Veri Seti Kolonları
- **HastaNo**: Hasta numarası  
- **Yas**: Hastanın yaşı  
- **Cinsiyet**: Kadın/Erkek/Bilinmiyor  
- **KanGrubu**: A, B, AB, 0 veya bilinmiyor  
- **Uyruk**: Hastanın uyruk bilgisi  
- **KronikHastalik**: Kronik hastalık bilgisi (var/yok)  
- **Bolum**: Hastanın tedavi olduğu bölüm  
- **Alerji**: Alerji durumu  
- **Tanilar**: Tanı bilgileri  
- **TedaviAdi**: Uygulanan tedavinin adı  
- **TedaviSuresi**: Tedavi süresi  
- **UygulamaYerleri**: Tedavinin uygulandığı yer  
- **UygulamaSuresi**: Tedavi uygulama süresi  

## Yapılan İşlemler

1. **Eksik veri analizi**  
   - Hangi kolonlarda eksik veri var, yüzdelik dağılımı hesaplandı.  
   - Eksik değerler uygun şekilde dolduruldu veya “Yok/Bilinmiyor” olarak işaretlendi.

2. **Yaş aralıkları oluşturma**  
   - Yaş sayısal olduğu için gruplara ayrıldı:
     - 2–37  
     - 38–56  
     - 56–92  
   - Bu sayede görselleştirmelerde daha anlamlı karşılaştırmalar yapıldı.

3. **Kronik hastalık bilgisi binary hale getirildi**  
   - `Var` / `Yok` olarak etiketlendi.  

4. **Popüler kategorilerin seçimi**  
   - Çok sayıda kategoriye sahip kolonlarda (ör. Tedavi, UygulamaYerleri) **Top N + Diğer** yaklaşımı kullanıldı.  
   - Böylece görselleştirmeler daha okunabilir oldu.

5. **Görselleştirmeler**  
   - **Heatmap**: Yaş aralığı, cinsiyet ve kronik hastalık ilişkileri  
   - **Countplot / barplot**: Kategorik kolonların dağılımları  
   - **Yüzdelik heatmap**: Oranları görmek için  
   - Örnek analizler:
     - Cinsiyet × Kronik Hastalık  
     - Yaş Aralığı × Cinsiyet × Kronik Hastalık  
     - Kan Grubu × Uygulama Yerleri  
