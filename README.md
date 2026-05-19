# STM32F4-Ethernet-CAN-Hardware-Design
Bu proje, yüksek hızlı haberleşme arayüzlerine, elektriksel izolasyona ve kararlı güç yönetimine ihtiyaç duyan endüstriyel otomasyon ve savunma sanayii uygulamaları için tasarlanmış çok katmanlı bir donanım altyapısıdır. Tasarım süreci Altium Designer kullanılarak hiyerarşik şema yapısında gerçekleştirilmiştir.
Donanım Mimarisi ve Kritik Bileşenler
Kart tasarımı, sistemin modülerliğini ve hata ayıklama (debug) süreçlerini kolaylaştırmak amacıyla hiyerarşik bloklar halinde kurgulanmıştır:

MCU: STM32F4 Serisi (STM32F417VGT6) - Yüksek performanslı ARM Cortex-M4 çekirdeği.

Ağ ve Haberleşme Katmanı:

Ethernet: RMII arayüzü ile sürülen DP83848 PHY entegresi kullanılarak 10/100 Mb/s ağ bağlantısı.

CAN Bus: Endüstriyel gürültülere karşı ISO1050 izolatörlü CAN Transceiver donanımı.

Seri Haberleşme: Uzun mesafe veri aktarımı için SN65HVD30DR tabanlı RS-422 ve standart RS-232 arayüzleri.

USB-UART: Sistem hata ayıklama süreçleri için FT230XQ çipiyle donanımlandırılmış Type-C / USB arayüzü.

Güç Yönetimi:

Sistem beslemesi için yüksek verimli dual step-down mimarisi kullanılmıştır.

5V Hattı: RT2862GSP (3A, 30V) senkron buck converter.

3.3V Hattı: AP3441 (3A, 2MHz) yüksek hızlı buck converter.

Görsel Arayüz: Harici ekran yönetimi için 128x64 Grafik LCD (GLCD) ve standart Karakter LCD portları.
