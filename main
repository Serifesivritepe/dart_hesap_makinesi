import 'dart:io';

void main() {
  while (true) {
    print("Hangi işlemi yapmak istiyorsunuz?");
    print("1- Toplama");
    print("2- Çıkarma");
    print("3- Çarpma");
    print("4- Bölme");
    print("0- Bitir");

    int choice = int.parse(stdin.readLineSync() ?? "0");

    if (choice == 0) {
      print("Program sonlandırılıyor.");
      break;
    } else if (choice >= 1 && choice <= 4) {
      print("İlk sayıyı girin:");
      double num1 = double.parse(stdin.readLineSync() ?? "0.0");

     
      double? num2;

      if (choice != 1) {
       
        print("İkinci sayıyı girin:");
        num2 = double.parse(stdin.readLineSync() ?? "0.0");
      }

      double result = 0.0;

      switch (choice) {
        case 1:
          result = toplama(num1, num2 ?? 0.0);
          break;
        case 2:
          result = cikarma(num1, num2 ?? 0.0);
          break;
        case 3:
          result = carpma(num1, num2 ?? 1.0);
          break;
        case 4:
          if (num2 != null && num2 != 0) {
            result = bolme(num1, num2);
          } else {
            print("Hata: Sayılar sıfıra bolunemez!");
            continue;
          }
          break;
      }

      print("Sonuç: $result");
    } else {
      print("Geçersiz işlem! Lütfen tekrar deneyiniz.");
    }
  }
}

double toplama(double a, [double? b]) {
  return a + (b ?? 0.0);
}

double cikarma(double a, double b) {
  return a - b;
}

double carpma(double a, [double? b]) {
  return a * (b ?? 1.0);
}

double bolme(double a, double b) {
  if (b == 0) {
    throw Exception("Sayılar sıfıra bolunemez!");
  }
  return a / b;
}
