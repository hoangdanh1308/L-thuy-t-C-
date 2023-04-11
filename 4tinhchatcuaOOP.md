	Encapsulation (Tính đóng gói): 
•	Trong lập trình hướng đối tượng có ý nghĩa không cho phép người sử dụng các đối tượng thay đổi trạng thái nội tại của một đối tượng, mà chỉ có phương thức nội tại của đối tượng có thể thay đổi chính nó. Điều đó có nghĩa, dữ liệu và thông tin sẽ được đóng gói lại, giúp các tác động bên ngoài một đối tượng không thể làm thay đổi đối tượng đó, nên sẽ đảm bảo tính toàn vẹn của đối tượng, cũng như giúp dấu đi các dữ liệu thông tin cần được che giấu.
•	Ví dụ ta thấy một viên thuốc chữa cảm. Chúng ta chỉ biết nó chữa cảm sổ mũi nhức đầu và một số thành phần chính, còn cụ thể bên trong nó có những hoạt chất gì thì hoàn toàn không biết nhà sản xuất mới có thể biết.
	Abstraction (Tính trừu tượng) 
•	Trong lập trình hướng đối tượng là một khả năng mà chương trình có thể bỏ qua sự phức tạp bằng cách tập trung vào cốt lõi của thông tin cần xử lý.Điều đó có nghĩa, bạn có thể xử lý một đối tượng bằng cách gọi tên một phương thức và thu về kết quả xử lý, mà không cần biết làm cách nào đối tượng đó được các thao tác trong class.
•	Ví dụ đơn giản chạy xe tay ga thì có hành động là tăng ga để tăng tốc, thì chức năng tăng ga là đại diện cho trừu tượng (abstraction). Người dùng chỉ cần biết là tăng ga thì xe tăng tốc, không cần biết bên trong nó làm thế nào..
•	class footballClub
•	    {
•	    private:
•	        char nameClub[9];
•	        int members;
•	        int rank;
•	    public:
•	        footballClub(){
•	            this->members = 0;
•	            this->rank = 0;
•	        };
•	        ~footballClub(){
•	            this->members = 0;
•	            this->rank = 0;
•	        };
•	        void set();
•	        void get();
•	    };
•	    
•	    void footballClub::set()
•	    {
•	        cout<<"so thanh vien"<<endl;
•	        cin>>footballClub::members;
•	    }
•	    
•	    void footballClub::get()
•	    {
•	        cout<<footballClub::members;
•	    }
•	
•	    class fanClub : public footballClub {
•	        private:
•	        int membersFan;
•	        char namefanClub[10];
•	        public:
•	        void set(){
•	            footballClub::set();
•	            cout<<"nhap vao so fan"<<endl;
•	            cin >>this->membersFan;
•	        };
•	        void get(){
•	            footballClub::get();
•	            cout<<"so luong Fan"<<this->membersFan<<endl;
•	        };
•	    };
•	

Ví dụ về tính trừu tượng:
int main(int argc, char const *argv[])
{
    fanClub realMadrid;

    realMadrid.set();
    realMadrid.get();
    
    return 0;
}
-	Ở đây ta tạo  1 Object là realMadrid thuộc lớp fanClub. Lớp fanClub được kế thừa từ lớp cha là footballClub.
-	Ta gọi Object thực hiện chức năng của nó là gán giá trị và xuất ra màn hình thông tin của đội bóng.
-	Ta chỉ cần gọi tên phương thức set() và get() là ta có thể nhận về kết quả như bên dưới: mà không cần quan tâm đến đối tượng đó  làm gì, biến đổi ra sao để ra kết quả mong muốn.
-	 

Ví dụ về tính đóng gói:
-	- Các phương thức nội tại bên trong của Class footballClub như là Contructor và discontructor và phương thức Set() có thể thay đổi giá trị của các Property.
-	-  

Ta không thể truy cập từ bên ngoài thông Object.membersFan để thay đổi giá trị. Ta chỉ có thể thực hiện thông qua các phương thức bên trong Class đó.
•	Vì thế nó được gói gọn trong  Class và thông tin sẽ được đóng gói lại, giúp các tác động bên ngoài một đối tượng không thể làm thay đổi đối tượng đó, nên sẽ đảm bảo tính toàn vẹn của đối tượng, cũng như giúp dấu đi các dữ liệu thông tin cần được che giấu.
