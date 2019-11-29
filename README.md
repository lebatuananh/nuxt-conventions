# Tổng hợp kinh nghiệm sử dụng nuxtjs hay cũng như vuejs
### 1.Cài đặt project trên môi trường phát triển của vscode
* Khi chạy vuejs trên vscode bạn đươc đề xuất cài đặt tiện ích vetur. vetur có rất nhiều chức năng như format code định dạng .vue , bắt các lỗi cơ bản, thêm vào snippet để gõ code nhanh hơn. Tuy nhiên project nuxt thường cài đặt thêm eslint để bắt lỗi. eslint và  vetur nó không cùng rule với nhau. Project của bạn chỉ chạy được khi phải pass rule của eslint. Vì vậy mà ta cần config vscode tắt một số chức năng của vetur đi và bật eslint nó bắt lỗi. 
* Các cài đặt eslint rất đơn giản đầu tiên là cài đặt tiện ích eslint của vscode sau đó thêm các dòng sau vào file .vscode/settings.json. (xem trong file .vscode/settings.json) nếu chưa có file này thì tạo thêm. vscode sẽ tự nhận diện nó
* `    
     "eslint.validate": [
        "javascript",
        "javascriptreact",
        {
            "language": "vue",
            "autoFix": true
        }
    ],
    "eslint.autoFixOnSave": true,
    "vetur.validation.script": false,
    "vetur.validation.template": true
`
* Đoạn mã trên bật tính năng auto fix lỗi của eslint khi bạn save code nó tắt validate script của vetur thay vào đó sẽ dùng eslint. Việc sử dụng eslint trong project nuxt là quan trọng. Nếu bạn không cài đặt eslint thì bạn sẽ gặp phải trường hợp là khi chạy app sẽ gặp lỗi và bạn sẽ tìm cách tắt hết rule của eslint đi và làm project không còn tuân theo quy tắc nữa.
* Eslint và prettier có quan hệ với nhau. Eslint thường tích hợp luôn prettier để format code luôn. hãy mở file eslintrc.js để xem config.
* Lưu ý quan trọng: Không mở project dưới dạng workspace của vscode vì nó làm ảnh hưởng tới việc các tiện ích của vscode hoạt động.

### 2. 
