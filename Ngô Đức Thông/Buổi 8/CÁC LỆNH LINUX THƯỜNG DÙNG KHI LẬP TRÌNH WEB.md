# Lệnh lưu trữ tệp của các thư mục


            tar -czf new-tar-file-name.tar.gz file-or-folder-to-archive

            tar -czf new-tar-file-name.tar.gz file1 file2 folder1 folder2


# Hủy lưu trữ:


             tar -xzf tar-file-name.tar.gz


 
# Lệnh liệt kê và sắp xếp các tệp theo kích thước:


            ls -lS


            ls -lSr

 
# Lệnh liệt kê kích thước các thư mục:


          du -sh /*


# Lệnh xem ổ đĩa còn trống bao nhiêu


            df -h
 
# Lệnh đếm tất cả các tệp và thư mục trong một thư mục:


            ls | wc -l


# Lệnh đổi tên tệp hoặc thư mục:


            mv name new_name


# Lệnh xóa toàn bộ thư mục với tất cả nội dung của nó:


            rm -rf dir_name


# Tạo một liên kết tượng trưng:


            ln -s [TARGET DIRECTORY OR FILE] ./[SHORTCUT]


Ví dụ:


            ln -s /usr/local/apache/logs ./logs



# Lệnh chuyển line-endings kiểu window sang kiểu unix cho toàn bộ dự án:


# Lệnh này sẽ bỏ qua các thư mục .git và .svn nhưng bạn có thể điều chỉnh nó theo nhu cầu của mình:


            find . -path ./.git -prune -o -path ./*.svn -prune -o -print -exec dos2unix {} ;


 
# Lệnh tìm tệp chứa văn bản:


            grep -rnw 'directory' -e "pattern"


Và đây là một ví dụ:


            grep -rnw /etc/apache2/sites-available/ -e "www"


# Lệnh tìm (sau đó xóa) các thư mục .svn tạo thành dự án của bạn:


            find . -name .svn -exec echo {} ;
            find . -name .svn -exec rm -rf {} ;
