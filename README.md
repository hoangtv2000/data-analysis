# Thực hành Khai phá Dữ liệu với một số Dataset
## Mục lục
- [Dữ liệu về giá vé tàu cao tốc ở Tây Ban Nha](#d--li-u-v--gi--v--t-u-cao-t-c---t-y-ban-nha)
  * [Giới thiệu](#gi-i-thi-u)
  * [Các phân tích & minh họa](#c-c-ph-n-t-ch---minh-h-a)
    + [1. Thống kê những ngày có nhiều lượt khởi hành nhất](#1-th-ng-k--nh-ng-ng-y-c--nhi-u-l--t-kh-i-h-nh-nh-t)
    + [2. Thống kê các chuyến tàu khởi hành và kết thúc cùng ngày và khác ngày](#2-th-ng-k--c-c-chuy-n-t-u-kh-i-h-nh-v--k-t-th-c-c-ng-ng-y-v--kh-c-ng-y)
    + [3. Thống kê giờ khởi hành của các chuyến tàu](#3-th-ng-k--gi--kh-i-h-nh-c-a-c-c-chuy-n-t-u)
    + [4. Thống kê giờ kết thúc của các chuyến tàu](#4-th-ng-k--gi--k-t-th-c-c-a-c-c-chuy-n-t-u)
    + [5. Thống kê số chuyến tàu của các tháng](#5-th-ng-k--s--chuy-n-t-u-c-a-c-c-th-ng)
    + [6. Thống kê thời gian di chuyển của các chuyến tàu](#6-th-ng-k--th-i-gian-di-chuy-n-c-a-c-c-chuy-n-t-u)
    + [7. Thống kê lượt tàu chạy của các ngày trong tuần](#7-th-ng-k--l--t-t-u-ch-y-c-a-c-c-ng-y-trong-tu-n)
    + [8. Lộ trình](#8-l--tr-nh)
    + [9. Phân tích các loại tàu cao tốc](#9-ph-n-t-ch-c-c-lo-i-t-u-cao-t-c)
    + [10. Phân tích các hạng vé](#10-ph-n-t-ch-c-c-h-ng-v-)
    + [11. Phân tích loại vé](#11-ph-n-t-ch-lo-i-v-)
    + [12. Phân tích Lộ trình với các yếu tố khác](#12-ph-n-t-ch-l--tr-nh-v-i-c-c-y-u-t--kh-c)
      - [Phân tích Lộ trình với Loại tàu cao tốc](#ph-n-t-ch-l--tr-nh-v-i-lo-i-t-u-cao-t-c)
      - [Phân tích Lộ trình với Hạng vé](#ph-n-t-ch-l--tr-nh-v-i-h-ng-v-)
    + [13. Phân tích giá vé trung bình dựa trên Hạng vé, Loại tàu cao tốc, Lộ trình và Loại vé](#13-ph-n-t-ch-gi--v--trung-b-nh-d-a-tr-n-h-ng-v---lo-i-t-u-cao-t-c--l--tr-nh-v--lo-i-v-)
      - [Biểu đồ trung bình giá vé theo Hạng vé](#bi-u----trung-b-nh-gi--v--theo-h-ng-v-)
      - [Biểu đồ trung bình giá vé theo Loại tàu cao tốc](#bi-u----trung-b-nh-gi--v--theo-lo-i-t-u-cao-t-c)
      - [Biểu đồ trung bình giá vé theo Lộ trình](#bi-u----trung-b-nh-gi--v--theo-l--tr-nh)
      - [Biểu đồ trung bình giá vé theo Loại vé](#bi-u----trung-b-nh-gi--v--theo-lo-i-v-)
    + [14. Phân tích thời gian di chuyển trung bình dựa theo Lộ trình](#14-ph-n-t-ch-th-i-gian-di-chuy-n-trung-b-nh-d-a-theo-l--tr-nh)
    + [15. Phân tích thời gian di chuyển trung bình dựa theo Loại tàu cao tốc](#15-ph-n-t-ch-th-i-gian-di-chuy-n-trung-b-nh-d-a-theo-lo-i-t-u-cao-t-c)


**Lưu ý**: để thuận tiện cho việc xem biểu đồ, hãy để github ở chế độ light mode.

# Dữ liệu về giá vé tàu cao tốc ở Tây Ban Nha

## Giới thiệu
Đây là bộ dữ liệu về các chuyến đi của Hệ thống tàu cao tốc Tây Ban Nha của công ty Renfe. Trong bộ dữ liệu này gồm các thông tin di chuyển của hành khách từ ngày 11/04/2019 đến ngày 7/10/2020. Các thông tin của mỗi chuyến đi gồm nơi khởi hành, nơi đến, hạng vé, chỗ ngồi, số ghế trống... Chúng ta hãy cùng phân tích một cách trực quan bộ dữ liệu này bằng EDA(Exploratory data analysis) để tìm hiểu hành vi tiêu dùng của họ. 

Dataset: [Spanish Rail Tickets Pricing - Renfe](https://www.kaggle.com/thegurusteam/spanish-high-speed-rail-system-ticket-pricing)

## Các phân tích & minh họa 

### 1. Thống kê những ngày có nhiều lượt khởi hành nhất 
Các ngày từ ngày 13 đến 17 tháng 4 có lượt khởi hành nhiều nhất, do những ngày này là ngày lễ thứ 5 thánh và thứ 6 tuần thánh của người Tây Ban Nha.

<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/50%20ng%C3%A0y%20c%C3%B3%20nhi%E1%BB%81u%20l%C6%B0%E1%BB%A3t%20kh%E1%BB%9Fi%20h%C3%A0nh%20nh%E1%BA%A5t.png'>

### 2. Thống kê các chuyến tàu khởi hành và kết thúc cùng ngày và khác ngày
Hầu hết các chuyến tàu bắt đầu và kết thúc trong ngày, chỉ có hơn 1% chuyến tàu là khác ngày.

<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/%25%20c%C3%A1c%20chuy%E1%BA%BFn%20t%C3%A0u%20kh%E1%BB%9Fi%20h%C3%A0nh%20v%C3%A0%20k%E1%BA%BFt%20th%C3%BAc%20c%C3%B9ng%20ng%C3%A0y.png'>

### 3. Thống kê giờ khởi hành của các chuyến tàu
Hầu hết các chuyến tàu khởi hành từ 6AM đến 9AM hoặc từ 2PM đến 7PM. Tầm giờ đó là giờ cao điểm.

**Biểu đồ cột**

<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/Gi%E1%BB%9D%20kh%E1%BB%9Fi%20h%C3%A0nh%20c%E1%BB%A7a%20c%C3%A1c%20chuy%E1%BA%BFn%20t%C3%A0u.png'>


**Biểu đồ sao**

<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/S%E1%BB%91%20l%C6%B0%E1%BB%A3ng%20c%C3%A1c%20chuy%E1%BA%BFn%20t%C3%A0u%20kh%E1%BB%9Fi%20h%C3%A0nh%20theo%20gi%E1%BB%9D.png'>


### 4. Thống kê giờ kết thúc của các chuyến tàu
Hầu hết các chuyến tàu kết thúc từ 9AM đến 11AM hoặc từ 17PM đến 22PM.

**Biểu đồ cột**

<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/Th%E1%BB%91ng%20k%C3%AA%20gi%E1%BB%9D%20k%E1%BA%BFt%20th%C3%BAc%20c%E1%BB%A7a%20c%C3%A1c%20chuy%E1%BA%BFn%20t%C3%A0u.png'>


**Biểu đồ sao**

<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/S%E1%BB%91%20l%C6%B0%E1%BB%A3ng%20c%C3%A1c%20chuy%E1%BA%BFn%20t%C3%A0u%20k%E1%BA%BFt%20th%C3%BAc%20theo%20gi%E1%BB%9D.png'>


### 5. Thống kê số chuyến tàu của các tháng
Hầu hết các chuyến tàu nằm ở tháng 3

<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/Th%E1%BB%91ng%20k%C3%AA%20s%E1%BB%91%20chuy%E1%BA%BFn%20t%C3%A0u%20c%E1%BB%A7a%20c%C3%A1c%20th%C3%A1ng.png'>


### 6. Thống kê thời gian di chuyển của các chuyến tàu
Đa số các chuyến tàu có thời gian di chuyển ở khoảng 150 - 170 phút, đây là thời gian trung bình để đi từ Madrid tới Barcelona hoặc từ Madrid tới Seville.

<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/Th%E1%BB%91ng%20k%C3%AA%20th%E1%BB%9Di%20gian%20c%C3%A1c%20chuy%E1%BA%BFn%20t%C3%A0u%20(d%E1%BB%B1a%20tr%C3%AAn%2040k%20quan%20s%C3%A1t).png'>


### 7. Thống kê lượt tàu chạy của các ngày trong tuần
Ngày thứ 6 và thứ 7 cuối tuần có lượt tàu chạy nhiều hơn những ngày còn lại. 

<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/Th%E1%BB%91ng%20k%C3%AA%20l%C6%B0%E1%BB%A3t%20t%C3%A0u%20c%E1%BB%A7a%20c%C3%A1c%20ng%C3%A0y%20trong%20tu%E1%BA%A7n.png'>


### 8. Lộ trình
Trong dataset có tất cả 62 lộ trình. Hầu hết các lộ trình đều xuất phát từ Madrid và chọn Madrid làm điểm đến. Tiếp đến là hai thành phố Barcelona, Vanlencia và Seville. 

**Biểu đồ tròn thống kê top 20 lộ trình được lựa chọn nhiều nhất theo tỉ lệ phần trăm**

<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/Bi%E1%BB%83u%20%C4%91%E1%BB%93%20top%2020%20l%E1%BB%99%20tr%C3%ACnh%20%C4%91%C6%B0%E1%BB%A3c%20ch%E1%BB%8Dn%20nhi%E1%BB%81u%20nh%E1%BA%A5t.png'>


**Đồ thị cây thống kê top 20 lộ trình được lựa chọn nhiều nhất**

<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/Ph%C3%A2n%20t%C3%ADch%20l%E1%BB%99%20tr%C3%ACnh%20b%E1%BA%B1ng%20%C4%91%E1%BB%93%20th%E1%BB%8B%20c%C3%A2y.png'>


### 9. Phân tích các loại tàu cao tốc

+ **Tàu AVE**: Tàu AVE hoạt động trên hệ thống đường ray 3100 km, là đường ray tốc độ cao dài nhất ở Châu Âu. Tàu AVE có thể chạy với tốc độ lên đến 310 km/h trên mạng lưới đường ray rộng lớn này, cho phép di chuyển một cách nhanh chóng giữa các thành phố ở Tây Ban Nha. Nó có thể đi từ Madrid đến Barcelona trong vòng chưa đầy 3 giờ! Hệ thống xe lửa hiện đại này kết nối nhiều thành phố trên khắp Tây Ban Nha từ Madrid và Barcelona, đến Córdoba, Seville, Málaga và Valencia.
+ **ALVIA**: Các chuyến tàu Alvia của Tây Ban Nha kết hợp cả tuyến đường dài và dịch vụ tốc độ cao để kết nối các thành phố lớn trên khắp Tây Ban Nha. Alvia cung cấp nhiều tuyến đường như kết nối từ Madrid đến Gijón, Alicante và Castellón và từ Barcelona đến Bilbao, A Coruña và Vigo. Với các toa máy lạnh và check-in control trước khi lên tàu, Alvia là một sự lựa chọn thoải mái và thư giãn để đi qua một trong những quốc gia lớn nhất châu Âu.
+ **NỘI TỈNH**: Các chuyến tàu nội địa tỉnh và liên tỉnh ở Tây Ban Nha. Các chuyến tàu nội tỉnh hoạt động ở phía bắc của Tây Ban Nha, kết nối các thành phố như Bilbao, Gijón, León và Santander. Đây là một mạng lưới các chuyến tàu hoạt động trong và xung quanh các thành phố lớn của Tây Ban Nha bao gồm Barcelona và Valencia.
+ **LIÊN TỈNH**: Các chuyến tàu liên tỉnh truyền thống chạy với tốc độ từ 160 đến 250 km / h cho phép bạn đến gần như mọi ngóc ngách của Tây Ban Nha. Bạn có thể chọn đi hạng 2 (du lịch) hoặc hạng 1 (ưu tiên). Độ thoải mái của toa gần bằng với tàu cao tốc AVE. Tất cả các chuyến tàu đều có máy lạnh.
+ **AV City**: Các chuyến tàu của thành phố AV là tàu cao tốc bổ sung cho AVE, cung cấp giá thấp hơn và được bán trên thị trường ở hạng phổ thông và hạng phổ thông plus (p +).
+ **TRENHOTEL**: Trenhotel là các chuyến tàu đêm chạy ở Tây Ban Nha và từ Tây Ban Nha đến Bồ Đào Nha. Có nhiều loại tàu khác nhau được sử dụng, cung cấp các loại dịch vụ khác nhau. Các chuyến tàu cũ có ghế hạng 2, 4 giường, 2 giường và 2 giường với vòi sen tắm riêng và nhà vệ sinh. Các chuyến tàu mới hơn có ghế ngả hạng 1 và 2 giường nằm với vòi sen và nhà vệ sinh riêng. Tất cả các chuyến tàu đều có toa hàng nhỏ.
+ **LD,AVE-MD,AVE-LD,LD-MD,MD-AVE,MD,LD-AVE** là các chuyến tàu LD-MD là Long Distance/ Medium Distance

**Phân tích các loại tàu cao tốc bằng biểu đồ tròn**
Đa số người dân sử dụng loại tàu AVE. Đây là loại tàu hoạt động trên hệ thống đường ray nối các thành phố lớn (Madrid, Barcelona, Vallencia,...) 

<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/Ph%C3%A2n%20t%C3%ADch%20c%C3%A1c%20lo%E1%BA%A1i%20t%C3%A0u%20cao%20t%E1%BB%91c%20b%E1%BA%B1ng%20bi%E1%BB%83u%20%C4%91%E1%BB%93%20tr%C3%B2n.png'>


### 10. Phân tích các hạng vé

Các chuyến tàu ở Tây Ban Nha thường được chia làm 2 hạng vé:
+ **Turista**: bình dân
+ **Preferente**: hạng sang

**Phân tích các hạng vé bằng biểu đồ tròn**
Hơn 80% hành khách chọn vé hạng bình dân, và chỉ 5% chọn vé hạng sang.

<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/Ph%C3%A2n%20t%C3%ADch%20c%C3%A1c%20h%E1%BA%A1ng%20v%C3%A9%20b%E1%BA%B1ng%20bi%E1%BB%83u%20%C4%91%E1%BB%93%20tr%C3%B2n.png'>


### 11. Phân tích loại vé

+ **Promo**: Các chương trình khuyến mại này dựa trên hệ thống giá vé động với chiết khấu lớn với các chuyến tàu AVE và Larga Distancia (Đường dài) trên các hành trình nội địa, được thiết lập tùy thuộc vào chuyến tàu, ngày đi và lượt mua trước.
+ **Flexible**: là chương trình ưu đãi thương mại chỉ dành cho các dịch vụ AVE và Larga Distancia (Đường dài) trên tất cả các hạng ghế và chỗ ngồi (chỗ ngồi và bến). Đây là mức giá tương tự như bình thường, không có bất kỳ chiết khấu nào, nhưng đi kèm với các ưu đãi bổ sung giúp hành khách có điều kiện tốt hơn để thay đổi, hủy chuyến hoặc nếu họ lỡ chuyến tàu của mình.
+ **Promo +**: Các chương trình khuyến mại này dựa trên hệ thống giá vé động với chiết khấu lớn với các chuyến tàu AVE và Larga Distancia (Đường dài) trên các hành trình nội địa, được thiết lập tùy thuộc vào chuyến tàu, ngày đi và lượt mua trước. Nhưng không hạ thấp bất kỳ tiêu chuẩn chất lượng nào.

**Phân tích các loại vé bằng biểu đồ tròn**
Hơn 50% hành khách chọn vé loại Promo, 22% chọn Flexible.

<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/Ph%C3%A2n%20t%C3%ADch%20c%C3%A1c%20lo%E1%BA%A1i%20v%C3%A9%20b%E1%BA%B1ng%20bi%E1%BB%83u%20%C4%91%E1%BB%93%20tr%C3%B2n.png'>


### 12. Phân tích Lộ trình với các yếu tố khác

#### Phân tích Lộ trình với Loại tàu cao tốc
Biểu đồ thống kê các chuyến đi với Loại tàu cao tốc dựa trên Lộ trình:

<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/Bi%E1%BB%83u%20%C4%91%E1%BB%93%20th%E1%BB%91ng%20k%C3%AA%20c%C3%A1c%20chuy%E1%BA%BFn%20%C4%91i%20v%E1%BB%9Bi%20Lo%E1%BA%A1i%20t%C3%A0u%20cao%20t%E1%BB%91c%20d%E1%BB%B1a%20tr%C3%AAn%20L%E1%BB%99%20tr%C3%ACnh.png'>

#### Phân tích Lộ trình với Hạng vé
Biểu đồ thống kê các chuyến đi với Hạng vé dựa trên Lộ trình

<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/Bi%E1%BB%83u%20%C4%91%E1%BB%93%20th%E1%BB%91ng%20k%C3%AA%20c%C3%A1c%20chuy%E1%BA%BFn%20%C4%91i%20v%E1%BB%9Bi%20H%E1%BA%A1ng%20v%C3%A9%20d%E1%BB%B1a%20tr%C3%AAn%20L%E1%BB%99%20tr%C3%ACnh.png'>


### 13. Phân tích giá vé trung bình dựa trên Hạng vé, Loại tàu cao tốc, Lộ trình và Loại vé

#### Biểu đồ trung bình giá vé theo Hạng vé
<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/scatter0.png'>

#### Biểu đồ trung bình giá vé theo Loại tàu cao tốc
<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/scatter1.png'>

#### Biểu đồ trung bình giá vé theo Lộ trình
<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/scatter2.png'>

#### Biểu đồ trung bình giá vé theo Loại vé
<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/scatter3.png'>

### 14. Phân tích thời gian di chuyển trung bình dựa theo Lộ trình
Biểu đồ thời gian di chuyển trung bình dựa theo Lộ trình

<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/scatter4.png'>

### 15. Phân tích thời gian di chuyển trung bình dựa theo Loại tàu cao tốc
Biểu đồ thời gian di chuyển trung bình dựa theo Loại tàu cao tốc

<img src = 'https://github.com/hoangtv2000/data-mining/blob/main/images-spanish-high-speed-rail/scatter5.png'>
