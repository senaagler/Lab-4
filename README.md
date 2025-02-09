# Lab-4
Lesson
package lan8;

interface DersIsle {
 void SozluSunum(); 
 void YaziliSunum(); 
}


abstract class Ders implements DersIsle {
 protected String DersAd;
 protected String DersSinif;

 public Ders(String DersAd, String DersSinif) {
     this.DersAd = DersAd;
     this.DersSinif = DersSinif;
 }

 public String IsmiBuyut(String DersAd) {
     return DersAd.toUpperCase();
 }

 public abstract String IsimGetir();
 public abstract String SinifGetir();
}






class Matematik extends Ders {
 public Matematik(String DersAd, String DersSinif) {
     super(DersAd, DersSinif);
 }

 @Override
 public String IsimGetir() {
     return "Ders Adı: " + DersAd;
 }

 @Override
 public String SinifGetir() {
     return "Ders Sınıfı: " + DersSinif;
 }

 @Override
 public void SozluSunum() {
     System.out.println(DersAd + " dersinde sözlü sunum yapıldı.");
 }

 @Override
 public void YaziliSunum() {
     System.out.println(DersAd + " dersinde yazılı sunum yapıldı.");
 }
}






class Fizik extends Ders {
 public Fizik(String DersAd, String DersSinif) {
     super(DersAd, DersSinif);
 }

 @Override
 public String IsimGetir() {
     return "Ders Adı: " + DersAd;
 }

 @Override
 public String SinifGetir() {
     return "Ders Sınıfı: " + DersSinif;
 }

 @Override
 public void SozluSunum() {
     System.out.println(DersAd + " dersinde sözlü sunum yapıldı.");
 }

 @Override
 public void YaziliSunum() {
     System.out.println(DersAd + " dersinde yazılı sunum yapıldı.");
 }
}





class Kimya extends Ders {
 public Kimya(String DersAd, String DersSinif) {
     super(DersAd, DersSinif);
 }

 @Override
 public String IsimGetir() {
     return "Ders Adı: " + DersAd;
 }

 @Override
 public String SinifGetir() {
     return "Ders Sınıfı: " + DersSinif;
 }

 @Override
 public void SozluSunum() {
     System.out.println(DersAd + " dersinde sözlü sunum yapıldı.");
 }

 @Override
 public void YaziliSunum() {
     System.out.println(DersAd + " dersinde yazılı sunum yapıldı.");
 }
}





public class SoyutSiniflar {
 public static void main(String[] args) {
	 
     Matematik matematik = new Matematik("Matematik", "10-A");
     System.out.println(matematik.IsimGetir());
     System.out.println(matematik.SinifGetir());
     System.out.println("Büyük Harfli Ders Adı: " + matematik.IsmiBuyut(matematik.DersAd));
     matematik.SozluSunum();
     matematik.YaziliSunum();

     System.out.println();

    
     Fizik fizik = new Fizik("Fizik", "11-B");
     System.out.println(fizik.IsimGetir());
     System.out.println(fizik.SinifGetir());
     System.out.println("Büyük Harfli Ders Adı: " + fizik.IsmiBuyut(fizik.DersAd));
     fizik.SozluSunum();
     fizik.YaziliSunum();

     System.out.println();

    
     Kimya kimya = new Kimya("Kimya", "12-C");
     System.out.println(kimya.IsimGetir());
     System.out.println(kimya.SinifGetir());
     System.out.println("Büyük Harfli Ders Adı: " + kimya.IsmiBuyut(kimya.DersAd));
     kimya.SozluSunum();
     kimya.YaziliSunum();
 }
}
