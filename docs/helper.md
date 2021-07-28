> Một số hàm helper xây dựng sẵn

Class tham khảo tại: `Modules/Common/Helpers/Helper.php`

##### csvToArray
- `params`: headers file, đường dẫn file, dấu phân tách dữ liệu trong file. 
- `return`: dữ liệu của file csv dưới dạng array

Sample usage: `Helper::csvToArray(['header1','header2'], 'storage/csv/example.csv', ',');`


##### getListDayOfMonth
- `params`: date
- `return`: array dữ liệu tất cả ngày trong tháng

Sample usage: `Helper::getListDayOfMonth('2021-07-07');`

##### sortAscArrayByField
sắp xếp 1 mảng theo chiều tăng dần của 1 key
- `params`: array gốc, key cần sắp xếp
- `return`: mảng theo chiều tăng dần của key

Sample usage: `Helper::sortAscArrayByField([
  ['key' => 1, 'value' => 'XYZ'],
  ['key' => 2, 'value' => 'ABC'],
], 'key');`

##### uploadFile
- `params`: $filePath/đường dẫn file, $file/file cần upload, $includeTime/có thêm timestamp vào trước tên file không, $replaceName, $prefix
- `return`: đường dẫn file

Sample usage: `Helper::uploadFile('/images', $file, true, false);`

##### resizeImage
- `params`: $file, $fileExtension, $maxWidth, $maxHeight
- `return`: file đã resize'/images', $file, true, false);`

##### correctImageOrientation
Sử dụng để fix lỗi ảnh tự động xoay khi chụp ảnh trên 1 số thiết bị
- `params`: $file
- `return`: file đã fix rotation

##### convertYoutubeUrlToEmbedUrl
Convert url youtube thành embed url
- `params`: $url
- `return`: $url đã convert 

##### getS3FullUrlFile
Get full url gồm cả domain của 1 file lưu trên s3
- `params`: $filePath
- `return`: $fileUrl


