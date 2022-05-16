        /***************** CSS *****************\

I. Phần chính của CSS:
        --> Được chia làm 2 phần:
        +, Selector: sẽ trỏ đến những đối tượng(html) chịu ảnh hưởng bởi CSS
        +, declaration: các thuộc tính CSS dùng để style cho thẻ Selector.

        Vd:
                h1 {
                        background: red;
                        color: blue
                }

II. Ta viết Css ở đâu:
        --> Chúng ta có ba cách viết CSS đó là viết:
                +, inline: viết trực tiếp trên thẻ thông qua thuộc tính style
                +, external: viết riêng một thẻ có phần đuôi .css rồi sau đó import vào bằng thẻ link.
                +, internal: viết tại file html hiện tại và nằm trong thẻ style

        2.1, inline
                +, Trong thẻ HTML chúng ta tạo một thuộc tính style="code css"
                        <div style="background:red; color: blue">HỌC CSS MIỄN PHÍ TẠI FREETUTS.NET</div>
        2.2  internal
                +, Chúng ta sẽ code bên trong thẻ <style type="text/css"> code css </style>
                        <style type="text/css">
                        div{
                                background:red; 
                                color: blue;
                        }
                        </style>
                        <div>HỌC CSS MIỄN PHÍ TẠI FREETUTS.NET</div>
                --> Lúc này tất cả các thẻ div sẽ mang thuộc tính background:red và color:blue
                --> Các thẻ kahcs thẻ div ko chịu thuộc tính này.
        2.3 external
                +,chúng ta cần tạo một file style.css (có phần mở rộng là .css) và sau đó import vào file HTML thông qua thẻ link. 
                        B1, Tạo một file style.css với nội dung sau:
                                div{
                                        background:red; 
                                        color: blue;
                                }
                        B2, Bước 2: Tạo một file index.html cùng cấp với file style.css với nội dung sau:
                                <link href="style.css" rel="stylesheet"/>
                                <div>HỌC CSS MIỄN PHÍ TẠI FREETUTS.NET</div>
                                
                                -->     trong thẻ link có một thẻ href, bạn sẽ truyền đường dẫn đến file CSS của bạn
                                        rel="stylesheet" báo cho trình duyệt đây là file CSS

        
--> Ta thường sử dụng các external vì nó tách biệt phần html và css.

II. Selector:
        --> Selector được sử dụng để chọn đối tượng(là thẻ nào của html) mà sẽ áp dụng css lên nó:
        + Như ta biết trong một file HTML thì có rất nhiều thẻ giống nhau và thông thường chúng ta sẽ đặt các ID, class cho các thẻ để phân biệt.
                -->vậy thì trong CSS sẽ dựa vào các ID và class đó để truy xuất tới và cách truy xuất đó ta gọi là selector.
        +, Ví dụ: Truy xuất tới tất cả các thẻ DIV và gán background cho nó màu đỏ
                        div{
                                background: red
                        }

        2.1, Các loại Css thông dụng:
                +, Có 3 loại selector chính:
                        +, CSS Selector phân cấp
                        +, CSS Selector ID
                        +, CSS Selector Class

                2.1.1, Selector phân cấp
                        +, Phân cấp nghĩa là sẽ dựa vào cấp cha để tìm cấp con.
                                Vd: Ví dụ: thiết lập color màu đỏ cho các thẻ p nằm trong thẻ div
                                +, file HTML
                                        <div>
                                        <p>
                                                Nội dung sẽ có màu đỏ vì nó nằm trong thẻ p.
                                        </p>
                                        </div>
                                        <p>
                                        Nội dung không có màu vì nó nằm ngoài thẻ p.
                                        </p>
                                +, file CSS
                                        div p{
                                                color: red
                                        }
                        
                        --> Kể cả 3 cấp ta cũng có thể viết như thế:
                                div p strong{
                                    color: red
                                }
                2.1.2, Selector ID
                        +, Trong một trang web ID là duy nhất nhé, nghĩa là nếu ta định nghĩa hai ID giống nhau trong 1 layout thì không đúng chuẩn giao diện của W3C. 
                        +, Giả sử bạn có nhiều thẻ div và bạn muốn viết CSS cho một thẻ DIV nào đó thôi thì bạn có thể chọn giải pháp là Selector theo ID của HTML. Chúng ta sử dụng dấu thăng (#) để đại diện cho ID.
                                Vd: Cho background màu đỏ cho div có id="active". 
                                --> file HTML
                                        <div id="active">
                                                ACTIVE
                                        </div>
                                --> file Css:
                                +,Cách 1:
                                        #active{
                                                background: red
                                        }
                                +, Cách 2:
                                        div#active{
                                            background: red
                                        }
                                --> Đoạn code div#active có nghĩa tìm là thẻ div có id là active.

                2.1.3, Selector class
                        +, Với ID là duy nhất thì class ngược lại, nghĩa là bạn có thể cho nhiều thẻ HTML có cùng tên class, điều này khá tiện lợi cho CSS. 
                        --> Ví dụ ta cần style cho một số thẻ div nào đó thôi thì nếu bạn dùng ID thì không hay lắm vì phải viết nhiều lần, chính vì vậy ta sẽ chọn class. Selector cho class sẽ là dấu chấm (.).
                                Vd: Ví dụ: thiết lập background màu vàng cho các the div có class="bg-yellow"
                                --> fiel HTML:
                                        <div class="bg-yellow">
                                                Yellow
                                        </div>
                                --> file Css:
                                        .bg-yellow{
                                                background: yellow
                                        }
                        
                        --> Giả sử bạn thiết lập class="bg-yellow" thêm một thẻ p nữa nhưng ta muốn chỉ có thẻ div là có tác dụng thì làm thế nào? 
                                -->Đơn giản ta chỉ cần thêm tên thẻ div đằng trước dấu chấm là được.
                                        Vd:
                                                div.bg-yellow{
                                                        background: yellow
                                                }
                
                2.1.4, Các lưu ý trong CSS Selector:
                        +,Thứ nhất bạn phải phân biệt được hai loại là ID selector và CSS selector:
                                +,Với ID thì trong mỗi trang web nó là duy nhất nên thông thường chúng ta hay dùng nó ở những vị trí không có tính chất lặp đi lặp lại nhiều lần
                                +, Với Class thì ta có thể đặt nhiều vị trí, chính vì vậy nếu website bạn có nhiều block giống nhau thì hãy chọn class
                        +, Thứ hai ban phải hiểu dù ID hay class thì đều tuân theo quy luật phâp cấp, nghĩa là khi truy vấn selector thì sẽ ghi cấp cha rồi tới cấp con. Ví dụ giờ viết CSS cho thẻ h2 có class="title" nằm trong thẻ  div có id="main".
                                div#mian h2.title{
                                
                                }
                        +, Thứ ba hiểu được sự khác nhau giữa ghi liền và ghi có khoảng trắng giữa id hoặc class và tên thẻ. Ví dụ:
                                +, div#main: chọn thẻ div có id="main" 
                                +, div #main: Chọn thẻ có id="main" nằm trong thẻ div

III. Các thuộc tính trong CSS:
        3.1 Màu sắc và kích cỡ trong CSS:
                3.1.1, Màu sắc chung:
                --> Màu sắc trong CSS chủ yếu sử dụng 3 màu: đỏ(RED), xanh lá(GREEN) và xanh nước biển(BLUE)
                        +, Màu trong CSS được chia làm 3 loại:
                                +, RGB
                                +, HEX
                                +, HSL
                        3.1.1.1, RGB trong CSS:
                                --> RGB là tỉ lệ trộn 3 màu bên trên: RED, GREEN, and BLUE
                                        --> Tổng quát: rgb(red, green, blue)
                                        Vd:  rgb(255, 0, 0) --> là toàn bộ là màu đỏ 
                                                +, To display black, set all color parameters to 0, like this: rgb(0, 0, 0).
                                                +, To display white, set all color parameters to 255, like this: rgb(255, 255, 255).
                                -       Vd2:
                                                p {
                                                        color: rgb(238, 130, 238)
                                                }
                                --> RGBA cũng là RGB nhưng thêm tính năng thể hiện độ trong suốt của màu: 
                                                p {
                                                        color: rgb(238, 130, 238, 0.5)
                                                }
                                                --> Nếu thay 0.5 là 1 thì sẽ là màu rõ nhất, nếu là 0.5 thì là màu sẽ nửa vời.                
                        3.1.1.2, HEX trong CSS:
                                +, Một mã hex trong Css đại diện cho: #RRGGBB (red, green, blue).
                                             p {
                                                        color: #ff0000
                                               }
                                        --> Toàn bộ thẻ <p> sẽ màu đỏ.
                        
                        3.1.1.3, HSL trong CSS:
                                +, HSL stands for hue, saturation, and lightness.
                                        --> màu sắc, độ bão hòa và độ sáng.
                                Vd: hsl(0, 100%, 50%)
                                        --> các chỉ số này designer sẽ đưa cho mình hoặc ta có thể tự chọn màu bằng link: https://www.w3schools.com/css/css_colors_hsl.asp
                3.1.2, Màu sắc riêng:
                        +, Muốn chỉnh background với hình nền là 1 link ảnh:
                                htmk{
                                        background: url('https://i.pinimg.com/originals/3a/3c/ab/3a3cabd94347cf64dade52882308c780.jpg');

                                }

                3.1.3, Hiển thị chữ trong Css(font, căn lề).
                        h1 {
                                font-size: 16px;                        --> Kích cỡ
                                font-weith: 500;                        --> Độ đậm của chữ
                                font-style: italic;                     --> Làm chữ bị in nghiêng
                                font-family: 'Arial';                   --> font của chữ = Arial
                                text-align: center;                     --> Chuyển chữ ra trung tâm
                                text-transform: uppercase;              --> Viết hoa toàn bộ các chữ
                                text-decoration: underline;             --> Gạch chân chữ đó.
                        }
                
                3.1.4, Dùng Css để sắp xếp giao diện(layout).
                        --> Ba khái niệm: border, margin và padding.
                        +, Border trong Css: Border là thuộc tính CSS dùng để tạo đường viền bao quanh nội dung của phần tử HTML, nó nằm giữa padding và margin
                                --> 4 thuộc tính quan trọng của border là: border-style, border-width, border-color và border-radius.
                                +, border-style: là thuộc tính để thiết lập loại border nào sẽ được hiển thị.
                                Vd:     p {
                                                background-color: rgb(255, 214, 192); 
                                                color: rgb(88, 214, 192);
                                                border-style: dotted;
                                        }
                                        --> border-style: dotted; chọn loại viền chấm chấm,... 
                                +, Những style chính là border hổ trợ như sau:
                                        +, dotted - border sẽ hiển thị là những dấu chấm
                                        +, dashed - border sẽ hiển thị nét đứt
                                        +, solid - border sẽ hiển thị đường thẳng liền mạch
                                        +, double - border sẽ hiển thị 2 đường thẳng
                                        +, groove - border sẽ hiển thị dạng rãnh 3D.
                                        +, ridge - border sẽ hiển thị dạng viền 3D.
                                        +, inset - border sẽ hiển thị dạng viền trong 3D. 
                                        +, outset - border sẽ hiển thị dạng viền đầu 3D. 
                                        +, none - sẽ không có border
                                        +, hidden - border sẽ  bị ẩn.
                        
                        +, border-width: là thuộc tính để thiết lập độ rộng của border.
                                --> Ta có thể sử dụng CSS Unit như pt, px, em, rem ...  hoặc là có thể dùng 3 giá trị sau: thin, medium, thick.
                                +, Cú pháp : selector {
                                                border-width: giá trị;
                                             }
                        
                                Vd: p {
                                        background-color: rgb(255, 214, 192); 
                                        color: rgb(88, 214, 192);
                                        border-style: dotted;
                                        border-width: 50px;
                                    }
                        
                        +, border-color:  là thuộc tính để thiết lập màu sắc cho border.
                                +, Cú pháp:     selector {
                                                        border-color: giá trị;
                                                }
                                        
                                        Vd:     p {
                                                        background-color: rgb(255, 214, 192); 
                                                        color: rgb(88, 214, 192);
                                                        border-style: dotted;
                                                        border-width: 50px;
                                                        border-color: rgb(88, 214, 74);
                                                }

                        +, border-radius : là để thiết lập bo tròn cho border --> Kiểu viền tròn, vuông hay gì đó cho border.
                                vd: border-radius: 10px;

                        +, border Shorland: là cách viết ngắn gọn cho 3 thuộc tính border-width, border-style và border-color.
                                +, Cú pháp:     selector {
                                                      border: width style color;
                                                }

                                        Vd:     div {
                                                        border: 15px dotted rgb(88, 214, 99);
                                                }
                
                +, Margin và Padding trong Css
                        +, Margin: Dùng để tạo khoảng cách giữa hai thẻ HTML:
                                +, margin-left: 20px : khoảng cách lề trái 20px 
                                +, margin-top:20px : khoảng cách lề trên 20px
                                +, margin-right: 20px : khoảng cách lề phải 20px
                                +, margin-bottom: 20px : khoảng cách lề dưới 20px
                                +, margin : 20px : tất cả lề trên, lề dưới, lề trái, lề phải đều có khoảng cách 20px 
                        
                        +, Padding: Dùng để tạo khoảng giữa thẻ HTML và nội dung của nó
                                +, padding-left: 20px : khoảng cách lề trái so với nội dung bên trong 20px 
                                +, padding-top:20px : khoảng cách lề trên so với nội dung bên trong 20px
                                +, padding-right: 20px : khoảng cách lề so với nội dung bên trong phải 20px
                                +, padding-bottom: 20px : khoảng cách so với nội dung bên trong lề dưới 20px
                                +, padding : 20px : tất cả lề trên, lề dưới, lề trái, lề phải so với nội dung bên trong đều có khoảng cách 20px 

        3.2, Position trong Css:
                +, Có  kiểu Position trong Css: 
                        +, static              : là kiểu nguyên thủy, ko chịu tác động nào của các method left, right, bottom, top
                        +, relative            : là kiểu dữ liệu chịu tác động của các method left, right, bottom, top theo default
                                        Vd: nếu Position: relative;
                                                left: 30px ;
                                --> thì sẽ dịch trái 30px so với vị trí nguyên thủy của nó.
                        +, fixed                : là kiểu dữ liệu hiển thị sẽ vẫn ở nguyên vĩ trí đó, dù ta có kéo hay lăn lên trên, sang ngang,...
                        +, absolute
                        +, sticky





                

