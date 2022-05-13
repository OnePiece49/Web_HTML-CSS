                /***************** HTML *****************\

I. HTML chia 2 phần.
    +, Header
    +, Body

1.1, Header
    --> Chủ yếu lấy thông tin tiêu đề.
    --> Phần title "Hiển thị tên trang web"".

1.2, Body   
    --> Gồm các tags:
        --> Các tags gồm tên tag và thuộc tính 
            Vd: <html lang="en">
                --> Ở đây "lang" là tên thuộc tính và ="en" là thông tin bổ sung cho thuộc tính.
        +, Các tags có nhiệm vụ:
            +, Hiển thị thông tin cho người dùng.
            +, Lấy thông tin từ người dùng.
    
    1.2.1, Hiển thị thông tin cho người dùng
        +, Các task cơ bản:
            +, Các tags từ <h1> đến <h5>
                --> Các tags này như là các đề mục với h1 đề mục lớn nhất và bến dần đế h5
                --> Các tags này có nhiệm vụ như là các đề mục, được bôi đậm và làm tăng kích cỡ chữ.
                Vd:       <h1> Huy ngu vkl </h1>
            
            +, Tags <p> và <br/>
                --> <p> Là tags hiển thị đoạn văn
                --> <br/> là tag để xuống dòng ==> Tương tự như "\n""
                        --> Tag này chỉ có thẻ đóng và ko có thẻ mở.
            
                Vd:       <p> hello huy ngu, ngu vkl <br/> vkl </p>


        +, Thẻ <ul> và <ol>
                --> Các tags này để tạo danh sách, và đi kèm với các tags cơ bản như <li>
                --> Tags <ul> để tạo danh sách với dấu chấm tròn như trong slide :))
                    Vd:     <ul>
                                <li>hello</li>
                                <li>ae </li>
                                <li>wibu</li>
                            </ul>

                --> Tag <ol> để tạo danh sách với các số ở đầu danh sách.
        
        +, Thẻ <div>:
                --> Có tác dụng để tạo dòng riêng rẽ, nghĩa là nó được xuống dòng ý
                    Vd:       <div> Hello Viet </div>

        +, Thẻ <span>:
                --> Có tác dụng tạo thành 1 câu ko xuống dòng:
                Vd:     <div>Hello Viet</div>
                        <span>hihi</span>
                        <span>hihi</span>
                        <div>Hello Viet</div>

                --> Kết quả :
                    Hello Viet
                    hihi hihi
                    Hello Viet

        +, Thẻ <a>:
                --> Sử dụng để chèn link vào web của bạn.
                Vd: <a href = "https://github.com/OnePiece49/Web_HTML-CSS">link github viet</a>
                        --> Lúc này ở trang html hiện "link github viet", và tích vào dòng chữ đó sẽ tới trang github của OnePiece49.

        +, Thẻ <img>:
                --> Sử dụng để chèn ảnh vào trang web.
                Vd: <img src= "https://thuthuatnhanh.com/wp-content/uploads/2020/10/hinh-anh-one-piece-luffy-cuoi-de-thuong.jpg"/>
                --> tag này chỉ gồm thẻ đóng và thuộc tính src.

    1.2.2. Lấy thông tin từ người dùng.
        +, Thẻ <form>:
            --> Đi kèm với thể label và thẻ input.
                    Vd1:     <form>
                                <label>Điền tên bạn vào đây</label>
                                <input type="text" placeholder ="Ten minh la"/>
                            </form>
                        --> Tạo 1 ô hình vuông để người dùng nhập text.

                    Vd2:
                            <input type="radio" name = "huy ngu"> qq
                            <input type="radio" name = "huy ngu"> cc
                        --> Tạo ra ô tròn tròn với thông tin hiển thị "qq" và "cc" cho người dùng tích
        
        +, Thẻ <select>
            --> Dùng để hiển thị các option để cho người dùng chọn.
            --> Đi kèm với thẻ <option>
                    Vd:
                                <label>huy có ngu ko?</label>
                                <select>
                                    <option>huy ngu</option>
                                    <option>huy rất ngu</option>
                                </select>
        
        


                            