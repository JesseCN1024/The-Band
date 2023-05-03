 EXERCISE 1: 
Build a website like this: https://www.w3schools.com/w3css/tryw3css_templates_band.htm#contact

Steps:
1. Phân tích : dựa theo mẫu, hoặc từ designer
2. Dựng base (xây móng)
3. Xây dựng từng phần theo phân tích: dựa vào bước 1
4. Hoàn thiện: review, fix, finish project  

Những thành phần thường gặp: 
1. Header (Đầu trang)
2. Navigation (Phan co cac nut dieu huong den nhung trang khac)
3. Breadcrumb (VD: Khoá học > Kiến thức chung > HTML/CSS zero to hero)
4. Sidebar: thanh ben trai/phai man hinh co cac nut dieu huong
     Front-end
         HTML,CSS
     Back-end
         NodeJS
     DevOps
5. Slider: chua noi dung truot qua lai
6. Content: nội dung chính của website
7. Footer (Chân trang): thường để logo, góp ý, email
8. Banner



------------TIEN HANH------------
BUOC 1: Phan tich
  1. Header V
  2. Slider V
  3. Content  (/Container: chua content)
      1. About
      2. Tour
        2.1 Tickets Booking modal  
            2.1.1 Container
                Header
                Body: label, input, button, Buying-Bnt
               
                Footer: close bnt, 'need help' bnt
                Exit button
      3. contact
      4. Image
  4. Footer


-----Nguyên tắc thiết kế-----
    1. Tu ngoai vao trong
    2. Tu tren xuong duoi
    3. Từ tổng quan đến chi tiết

---------- Summary ----------
82. Header CSS
    + Cach goi nhanh voi ul#nav>li*5>a
    + Kiem tra cac trang thai active, hover, ... cua tag tren web 28:43
        . Chon bieu tuong select ele    ment -> chon vao the can kiem tra
        .  Ben canh "Filter" -> :hov 
    + CSS truc tiep tren web (Styles->element.style{}) 31:50   
83. Navigation CSS    
    + Cach su dung outline de tim nhanh mot ham css
    + display: inline, inline-block, block
    + Viet hoa bang CSS: text-transform
    + Hieu ung shadow
    + Di vao the more va hien the con 24:25
84. Header search CSS
    + Download bo font/icon tren themify va setup vao project (hoac fontawesome neu can ,day du cac font)
    + Cach goi icon: <i class="<tenicon>"></i>
    + Ap dung thuoc tinh float / right
    + Thuoc tinh cursor:<value>; thay doi con hinh dang pointer
        + pointer: hinh ban tay
85. Set fixed positon for Header    
    + Cach tao thanh cuon truc tiep tren browser -> css truc tiep height tren browser
    + Xu li van de khi fixed position lam cho header bi day len tren -> su dung margin-top = height of header
86. Slider CSS
    + Cach su dung padding-top (va position: relative - positive) de set background
    + Tao title/desc roi can chinh
    + Sua loi slider tran len header bang z-index
87. About section CSS
    + Cai dat cac the div trong Content
    + Set center cho the div bang: margin-right = left = auto
    + Thuoc tinh do dam cua chua "opacity"
88. Team section CSS    
    + Duplicate dong hien tai: Shift + Alt + (Down arrow)
    + Su dung "float" de align 3 images tren 1 hang
    + Set width de align 3 images panel
    + Set img size (width) va text-align de can giua
    + clear (hoac overflow: hidden neu muon) de khac phuc cho TH su dung float
89. Tour Dates
    + Boi den background khi co phan border
    + Tao class 'chung' text-white de co j dung lai -> important
    + The span: used for colorizing a part of text 
    + Set background hinh tron: border-radius = 50%
    + Quy tac ve float:
        . Khi set float -> element display = block -> khi do moi co the tuy chinh widht/height
        . Khi do co the su dung margin -
90. Tour Places
    + Set width=100% cho img de dieu chinh anh trong the div
    + background-clip: set gioi han background trong cac box
    + set padding de tinh chinh kich thuoc cho button
91-92. Buy tickets modal
    + Khai niem:
        .giao dien modal (giao dien noi khi bam vao )
        .overlay: lop phu khi bat modal 
    + label tag
    + display: flex cho modal -> modal-containter - align center, justify
    + Icon + in inspector for add style rule
    + position: absolute cho "close button"
    + Body:
        . modal label khoang cach hop li toi input
        . Input adjusting
        . for:  of label
        . Xu li breakpoint (luc keo nho browser) (Responsive) : max-width: calc(100% - 32px)
    + Javascript
        . naming rule: "js-..."
        . adding 'open class' to modal ("modal open") -> modal opened
        . querrySelector -> function -> eventlistener: for setactive on/off when clicking buttons
        . @frame (in css file)
        . Bubble effect: when using eventlistener for an el, it also capture all that EVENTs of the CHILDREN
            -> how to fix
93-94. Contact section
    + Tư duy hàng và cột: tao class .row, .col, .col-third, ..
    + Áp dụng tư duy này vào contact section
    + form tag: used for storing input elements
    + input-submit type <input type="submit" value"<text display>">
    + css seletor nang cao: .contact-info i[class*="ti-"]
    + (*) them clear vao class row de fix 'float', su dung pseudo class
        .! su dung cho tag row, thay vi phai <div>clear<\div>
    + Them warnign sign cho input when submitting: attribute required
95. Map, footer CSS 
    + Using joint class for button: .pull-right, .btn
96. Review
    + href="#<id>" de get vao section
    + scroll-behaviour in html tag 
    + set web icon using favicon
       <link rel="icon" type"favicon.ico" href="<link here>">

---------- RESPONSIVE --------
100. Tablet Responsive
    + set maxwidth:100% cho truong hop tablet khi pc set width=800px
    + overflow: hidden: hide every elements that spill out of parent
101. Mobile Responsive
    + use overflow hidden for nav bar to hide/show 
    + **Javascript: 
        .var <variable> = document.getElementById('')
        .variable.onclick = funcion(){...}
        .console.log(<variable>) -> check in console to see if it's ok
        .alert(''): for browser to notify user  
102. Mobile Responsive fix
    + error1: nav button dont overflơw horizontally 
        -> parent tag has display: inline-block
        1. mobile Responsive: #nav display = block
    + error2: menu-btn appears on tablet, pc
    + error3: button 'Home' must not overflow -> inline-block
103. Mobile submenu fix
    + Err1: Click MORE -> hide menu
        + usig nextelementsiblings to get 'subnav'
        + <vari>.classList.contains('<>') -> check if element has class in bracket
        + event.preventDefault(); - used with onclick to stop called function from returning an event
    + Err2: overflow: hidden -> subnav disappears
        . only overflow: hidden on mobile
        . subnav position: absolute -> remove on mobile
            *button height on mobile should be 42-48px for good user experience
104. Content Responsive
    - Show member-img on each single line: 
        . width: 100%
    - edit size
    - apply class .mt-16
105. Contact form
    + using class s-col-full (make width 100%) 
    + lengthen buttons for better experience 
106. Review, fix UI/UX
    + Hold alt + up/down arrow -> changing value in inspector by .1 
    + phone to/ mail to in contact info
107. Run and fix bug on mobile
    + Ngrok Installation
    + For reseting basic settings on safari and other browsers (preventing errors)
        --webkit-appearance: none
108. Fix bugs   
    - text-shadow: h-shadow v-shadow blur-radius color|none|initial|inherit;
    - relative url address calling:
        + ./ : find the same level file
        + ../ : find file outside the folder


