# Tic-Tac-Toe-Thao
build interactive tic-tac-toe game to React
## Building a board
> Tạo 1 nút bằng function square
> > React component chỉ trả về một phần tử duy nhất nên không thể nối nhiều button vào với nhau nên cần 1 thẻ <> </>
> > Nhóm các ô vào các div với class="board-row" (3div) để các ô chuyển từ 1 hàng thành 3 hàng như ý
> Đổi tên function square thành board
## Passing data through props
> Tạo 1 function Square mới để return một button có class="square" để tạo 1 ô vuông có value = 1
> 
> cập nhật thành phần Board để hiển thị thành phần Square đó bằng cú pháp JSX (thay các button bằng Square ở trên, lưu ý luôn phải là tag đóng       <Square>.)
> 
> Sử dụng props để chuyển giá trị từ bố mẹ là board vào ô square thay giá trị là 1 mặc định {value}, **nhớ dấu {} này nhé** vì mình cần giá trị của thành phần chứ không phải và từ value
>
> Chuyển giá trị prop cho các thành phần Square vào bảng để hiển thị (pass the value prop to each Square component it renders) 
## Making an interactive component
> Khai báo một function handleClick bên trong function Square
> 
> Thêm onClick vào props của phần tử JSX của nút được trả về từ Square **nhớ dấu {} này nhé** onClick={handlerClick}
>
> Thành phần phải Square “ghi nhớ” rằng nó đã được nhấp vào và điền vào dấu “X”. Để “ghi nhớ” mọi thứ, các thành phần sử dụng trạng thái (useState).
> > Hãy lưu trữ giá trị hiện tại của Square ở trạng thái và thay đổi nó khi nhấp vào Square.
> > > Đặt import { useState } from 'react' ở đầu file
> > > Xoá value prop khỏi Square và sau đó thêm một dòng để bắt đầu Square để gọi useState. Thay console.log("clicked!"); bằng setValue("X");
## Completing the game (alternate placing “X”s and “O”s on the board, and you need a way to determine a winner)
> **Lifting state up** phát triển trạng thái
> 
> > thay vì set trạng thái cho từng ô, ta nên set trạng thái cho thành phần cha nó là bảng, bảng sẽ truyền trạng thái cho từng con theo tình huống cụ thể, điều này giúp đồng bộ các ô con với nhau và với cha mẹ chúng là bảng
> > > Edit the Board component so that it declares a state variable named squares that defaults to an array of 9 nulls corresponding to the 9 squares
> > > chỉnh sửa thành phần Square để nhận value prop từ thành phần Board
> > > chuyển một hàm từ thành phần Board sang thành phần Square và yêu cầu Square gọi hàm đó khi nhấp vào một hình vuông
>
> Talking turns X - O 
> > Đặt X là nước đi đầu tiên
>> cập nhật hàm handClick của Board để lật giá trị của xIsNext

## Declaring a winner 
> CalculateWinner function
## Bonus
>> ...history spread syntax
>> để chuyển đổi một mảng thành một mảng khác, bạn có thể sử dụng phương thức bản đồ mảng
>> đối với danh sách động phải cần key 