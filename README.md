# Sayisal_Analiz_Ödev1


""" cosx fonksiyonunun Taylor serisini hesaplayarak, π/5 noktasındaki değerini;
 Taylor serisinin tek ve iki terimini kullanarak hesaplayınız.
 Her iki durumdaki kesme hatalarını hesaplayınız.



 <---TAYLOR SERİ AÇILIMI--->
  f(a)=f(a0)+f'(a0)*(a-a0)+f''(a0)*((a-a0)^2)/2!)+ f'''(a0)*((a-a0)^3)/3!)+ .....
 
"""
import math
a=math.pi/5   # a=π/5 noktası
a0=0          # a0=0 (MACLAURİN Serisinde aldığımız sabit değer)

fon1=math.cos(a0)   #Taylor serimizdeki ilk terim olan f(a0) değerini buluyoruz
fon_ilk_türev=-math.sin(a)  #Taylor serimizdeki f'(a0) ı buluyoruz(  f(x)=cos(x) => f'(x)=-sin(x)  )

bulunan_sonuc1=fon1+fon_ilk_türev * (a-a0) #Taylorda ilk terim ve ikinci terimler toplamı
bulunan_sonuc2=bulunan_sonuc1+(math.cos(a0)*(a**2)/2)  #Taylorda ilk,ikinci ve üçüncü terimler toplamı
gerçek_sonuc=math.cos(a) # Taylorun olmazsa olmazı gerçek değer (gerçek değer bize kesme hatasını bulmada fazlasıyla gereken değer)

print("  ")
print("Serinin Gerçek Değeri: ",gerçek_sonuc)
print("  ")

print("Serinin İlk Terim Değeri: ",bulunan_sonuc1) #ilk terimden kastımız seride bir defa türev alınmış terim bulunmakta
print("tekterimli_kesmehata={}".format(gerçek_sonuc-bulunan_sonuc1)) #Tek terimli serinin kesme hatası

print("  ")

print("Serinin İkili Terim Değeri: ",bulunan_sonuc2) #Aynı şekilde seride iki defa türev alınmış terim bulunmakta
print("ikiterimli_kesmehata={}".format(gerçek_sonuc-bulunan_sonuc2))  #iki terimli serinin kesme hatası







