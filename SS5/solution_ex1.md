Trường hợp kiểm thử          |  Dữ liệu đầu vào  |Kết quả sai thực tế         |Kết quả đúng mong đợi
TC01 - Mã có khoảng trắng    |  " med-nhi-1024 " |Kiểm tra "MED-" trên chuỗi  |Sau trim() và toUpperCase(), mã hợp lệ, trả về true
và chữ thường                |                   |chữ thường nên trả về false |
-----------------------------|------------------------------------------------|-----------------------------
TC02 - Cắt số thứ tự tiếp đón|  "med-nhi-1024"   | Cắt sai vị trí có thể      |  Lấy đầy đủ 1024
                             |                   | làm thiếu/sai số thứ tự    |

1. startsWith("MED-") đang kiểm tra chữ hoa trong khi mã sau trim() vẫn là med-nhi-1024 -> sai
2. slice(8, 12) lấy vị trí chưa đúng nên cần xác định lại index của chuỗi