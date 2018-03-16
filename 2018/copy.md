tar 文件解压缩
tar zxvf gender.gz*
zip文件解压缩
unzip file.zip


服务器获得权限
su chenwei     密码：emdata2017
sudo chmod -R 777 folder


.tar.gz文件压缩和解压
压缩：tar zcvf filename.tar.gz filename
解压缩：tar zxvf filename.tar.gz

vnc 强制关掉
vncserver -kill :3
vncserver -geometry 1024x768



# cd /data/source/user16/10.17tongxinyu
# nano 20171016.sh
# 
current_file_path="20171016" #要处理的文件夹名
new_file_path="20171016_moved" #处理后的文件夹名
max_size=3000 #每个文件夹文件数量

i=1
for shname in `ls $current_file_path`
do
    #name=`echo "$shname" | awk -F\/ '{print $0}'`
    #name=`echo "$shname" | awk -F. '{print $0}'`
    if(($i%$max_size==0))
        mkdir -p ./$new_file_path/$[$i/$max_size]
        cp  $current_file_path/$shname ./$new_file_path/$[$i/$max_size]/
    then
        echo $i
        cp  $current_file_path/$shname/ ./$new_file_path/$[$i/$max_size]/
    fi
    i=$(($i+1))
done


# ctrl + x 保存退出 
# Y
# enter
# 

# bash 20171016.sh



分带有文件夹的文件

#需要移动的文件夹
current_file_path="MegafaceIdentities_VGG"


#移动到目的文件夹
new_file_path="MegafaceIdentities_VGG_moved"


#每个文件夹最大
max_folder_size=500


# check path persent
if [ ! -d "$new_file_path" ]; then
(mkdir ${new_file_path} && chmod 777 ${new_file_path})
fi
i=1


for shname in `ls $current_file_path`
do
name=`echo "$shname" | awk -F. '{print $1}'`
if(($i%500==0))
then
mkdir -p $new_file_path/$[$i/500]
cp -rf $current_file_path/$name $new_file_path/$[$i/500]/
echo "create folder ${i/5000}"
else
cp -rf $current_file_path/$name/ $new_file_path/$[$i/500]/
echo "copy ${i}"
fi
i=$(($i+1))
done



如果文件夹加密了
sudo chenwei

sudo nano qian-fang4.sh
sudo bash qian-fang4.sh

exit


A文件夹
B文件夹 


B -》 A 


cp B/* A/



0605



cp  /home/user5/6.05/json/*  /home/user1/6.05/json/

cp  /home/user4/6.05/json/*  /home/user1/6.05/json/

cp  /home/user2/6.05/json/*  /home/user1/6.05/json/


0606
cp  /home/user5/6.05/json/*  /home/user1/6.05/json/

cp  /home/user4/6.05/json/*  /home/user1/6.05/json/

cp  /home/user2/6.05/json/*  /home/user1/6.05/json/



cp /data/source/user1/0927tele/tele/*  /data/suanfa/gaokaijun/down/2017.09.27chepai_dianhua_mingmin/tele/
cp /data/source/user2/0927tele/tele/*  /data/suanfa/gaokaijun/down/2017.09.27chepai_dianhua_mingmin/tele/
cp /data/source/user3/0927tele/tele/*  /data/suanfa/gaokaijun/down/2017.09.27chepai_dianhua_mingmin/tele/
cp /data/source/user4/0927tele/tele/*  /data/suanfa/gaokaijun/down/2017.09.27chepai_dianhua_mingmin/tele/

cp /data/source/user3/0927/8/*  /data/suanfa/tongxinyu/down/2017.09.27chepai_dianhua_mingmin/
cp /data/source/user4/0927/8/*  /data/suanfa/tongxinyu/down/2017.09.27xsz_riqi/

cp /data/source/user1/0927gaokaijun/dayin/*  /data/suanfa/gaokaijun/down/2017.09.27shenqingbiaodazi/dayin/
cp /data/source/user2/0927gaokaijun/dayin/*  /data/suanfa/gaokaijun/down/2017.09.27shenqingbiaodazi/dayin/
cp /data/source/user3/0927gaokaijun/dayin/*  /data/suanfa/gaokaijun/down/2017.09.27shenqingbiaodazi/dayin/
cp /data/source/user4/0927gaokaijun/dayin/*  /data/suanfa/gaokaijun/down/2017.09.27shenqingbiaodazi/dayin/
# 周一周二
sudo cp /data/source/user1/0312/json/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/json/
sudo cp /data/source/user1/0312/mark/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark/
sudo cp /data/source/user1/0312/mark1/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark1/
sudo cp /data/source/user1/0312/xml/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/xml/
sudo cp /data/source/user2/0312/json/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/json/
sudo cp /data/source/user2/0312/mark/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark/
sudo cp /data/source/user2/0312/mark1/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark1/
sudo cp /data/source/user2/0312/xml/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/xml/
sudo cp /data/source/user3/0312/json/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/json/
sudo cp /data/source/user3/0312/mark/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark/
sudo cp /data/source/user3/0312/mark1/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark1/
sudo cp /data/source/user3/0312/xml/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/xml/
sudo cp /data/source/user6/0313/json/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/json/
sudo cp /data/source/user6/0313/mark/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark/
sudo cp /data/source/user6/0313/mark1/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark1/
sudo cp /data/source/user6/0313/xml/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/xml/
sudo cp /data/source/user7/0313/json/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/json/
sudo cp /data/source/user7/0313/mark/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark/
sudo cp /data/source/user7/0313/mark1/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark1/
sudo cp /data/source/user7/0313/xml/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/xml/
sudo cp /data/source/user8/0313/json/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/json/
sudo cp /data/source/user8/0313/mark/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark/
sudo cp /data/source/user8/0313/mark1/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark1/
sudo cp /data/source/user8/0313/xml/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/xml/
sudo cp /data/source/user10/0313/json/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/json/
sudo cp /data/source/user10/0313/mark/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark/
sudo cp /data/source/user10/0313/mark1/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark1/
sudo cp /data/source/user10/0313/xml/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/xml/


#周三周四周五

sudo cp /data/source/user1/0314/json/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/json/
sudo cp /data/source/user1/0314/mark/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark/
sudo cp /data/source/user1/0314/mark1/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark1/
sudo cp /data/source/user1/0314/xml/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/xml/
sudo cp /data/source/user2/0314/json/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/json/
sudo cp /data/source/user2/0314/mark/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark/
sudo cp /data/source/user2/0314/mark1/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark1/
sudo cp /data/source/user2/0314/xml/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/xml/
sudo cp /data/source/user3/0314/json/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/json/
sudo cp /data/source/user3/0314/mark/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark/
sudo cp /data/source/user3/0314/mark1/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark1/
sudo cp /data/source/user3/0314/xml/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/xml/
sudo cp /data/source/user4/0314/json/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/json/
sudo cp /data/source/user4/0314/mark/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark/
sudo cp /data/source/user4/0314/mark1/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark1/
sudo cp /data/source/user4/0314/xml/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/xml/
sudo cp /data/source/user5/0314/json/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/json/
sudo cp /data/source/user5/0314/mark/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark/
sudo cp /data/source/user5/0314/mark1/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark1/
sudo cp /data/source/user5/0314/xml/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/xml/
sudo cp /data/source/user6/0314/json/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/json/
sudo cp /data/source/user6/0314/mark/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark/
sudo cp /data/source/user6/0314/mark1/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark1/
sudo cp /data/source/user6/0314/xml/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/xml/
sudo cp /data/source/user7/0314/json/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/json/
sudo cp /data/source/user7/0314/mark/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark/
sudo cp /data/source/user7/0314/mark1/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark1/
sudo cp /data/source/user7/0314/xml/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/xml/
sudo cp /data/source/user8/0314/json/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/json/
sudo cp /data/source/user8/0314/mark/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark/
sudo cp /data/source/user8/0314/mark1/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark1/
sudo cp /data/source/user8/0314/xml/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/xml/
sudo cp /data/source/user10/0314/json/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/json/
sudo cp /data/source/user10/0314/mark/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark/
sudo cp /data/source/user10/0314/mark1/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark1/
sudo cp /data/source/user10/0314/xml/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/xml/
sudo cp /data/source/user11/0314/json/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/json/
sudo cp /data/source/user11/0314/mark/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark/
sudo cp /data/source/user11/0314/mark1/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark1/
sudo cp /data/source/user11/0314/xml/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/xml/
sudo cp /data/source/user12/0314/json/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/json/
sudo cp /data/source/user12/0314/mark/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark/
sudo cp /data/source/user12/0314/mark1/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark1/
sudo cp /data/source/user12/0314/xml/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/xml/



sudo cp /data/source/user12/0313/json/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/json/
sudo cp /data/source/user12/0313/mark/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark/
sudo cp /data/source/user12/0313/mark1/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark1/
cp /data/source/user12/0313/1/xml/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/xml/
cp /data/source/user13/0313/1/json/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/json/
cp /data/source/user13/0313/1/mark/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark/
cp /data/source/user13/0313/1/mark1/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/mark1/
cp /data/source/user13/0906/1/xml/*  /data/suanfa/xiaobo/down/2018.03.13changjingfenge/xml/

cp /data/source/user4/0616baoxiandan_chepai/mark/*  /data/suanfa/xuchen/down/2017.06.16_baoxiandan_chepai/mark/
cp /data/source/user4/0616baoxiandan_chepai/xml/*  /data/suanfa/xuchen/down/2017.06.16_baoxiandan_chepai/xml/
cp /data/source/user5/0616baoxiandan_chepai/json/*  /data/suanfa/xuchen/down/2017.06.16_baoxiandan_chepai/json/
cp /data/source/user5/0616baoxiandan_chepai/mark/*  /data/suanfa/xuchen/down/2017.06.16_baoxiandan_chepai/mark/
cp /data/source/user5/0616baoxiandan_chepai/xml/*  /data/suanfa/xuchen/down/2017.06.16_baoxiandan_chepai/xml/
cp /data/source/user6/0616baoxiandan_chepai/json/*  /data/suanfa/xuchen/down/2017.06.16_baoxiandan_chepai/json/
cp /data/source/user6/0616baoxiandan_chepai/mark/*  /data/suanfa/xuchen/down/2017.06.16_baoxiandan_chepai/mark/
cp /data/source/user6/0616baoxiandan_chepai/xml/*  /data/suanfa/xuchen/down/2017.06.16_baoxiandan_chepai/xml/
cp /data/source/user7/0616baoxiandan_chepai/json/*  /data/suanfa/xuchen/down/2017.06.16_baoxiandan_chepai/json/
cp /data/source/user7/0616baoxiandan_chepai/mark/*  /data/suanfa/xuchen/down/2017.06.16_baoxiandan_chepai/mark/
cp /data/source/user7/0616baoxiandan_chepai/xml/*  /data/suanfa/xuchen/down/2017.06.16_baoxiandan_chepai/xml/

cp /data/source/user8/0616chetou/json/*  /data/suanfa/xuchen/down/2017.06.16_chetou/json/
cp /data/source/user8/0616chetou/mark/*  /data/suanfa/xuchen/down/2017.06.16_chetou/mark/
cp /data/source/user8/0616chetou/xml/*  /data/suanfa/xuchen/down/2017.06.16_chetou/xml/
cp /data/source/user9/0616chewei/json/*  /data/suanfa/xuchen/down/2017.0616_chewei/json/
cp /data/source/user9/0616chewei/mark/*  /data/suanfa/xuchen/down/2017.0616_chewei/mark/
cp /data/source/user9/0616chewei/xml/*  /data/suanfa/xuchen/down/2017.0616_chewei/xml/

cp /data/source/user3/0616baoxiandan_chepai/json/*  /data/suanfa/xuchen/down/2017.06.16_baoxiandan_chepai/json/
cp /data/source/user3/0616baoxiandan_chepai/mark/*  /data/suanfa/xuchen/down/2017.06.16_baoxiandan_chepai/mark/
cp /data/source/user3/0616baoxiandan_chepai/xml/*  /data/suanfa/xuchen/down/2017.06.16_baoxiandan_chepai/xml/
cp /data/source/user3/0616baoxiandan_chepai/json/*  /data/suanfa/xuchen/down/2017.06.16_baoxiandan_chepai/json/
cp /data/source/user3/0616baoxiandan_chepai/mark/*  /data/suanfa/xuchen/down/2017.06.16_baoxiandan_chepai/mark/
cp /data/source/user3/0616baoxiandan_chepai/xml/*  /data/suanfa/xuchen/down/2017.06.16_baoxiandan_chepai/xml/
cp /data/source/user6/0616baoxiandan_chejiahao/json/*  /data/suanfa/xuchen/down/2017.06.16baoxiandan_chejiahao/json/
cp /data/source/user6/0616baoxiandan_chejiahao/mark/*  /data/suanfa/xuchen/down/2017.06.16baoxiandan_chejiahao/mark/
cp /data/source/user6/0616baoxiandan_chejiahao/xml/*  /data/suanfa/xuchen/down/2017.06.16baoxiandan_chejiahao/xml
cp /data/source/user7/2017.06.16_baoxiandan_chepai/json/*  /data/suanfa/xuchen/down/2017.06.16baoxiandan_chejiahao/json/
cp /data/source/user7/0615baoxiandan_chejiahao/mark/*  /data/suanfa/xuchen/down/2017.06.16baoxiandan_chejiahao/mark/
cp /data/source/user7/0615baoxiandan_chejiahao/xml/*  /data/suanfa/xuchen/down/2017.06.16baoxiandan_chejiahao/xml
cp /data/source/user8/0615baoxiandan_chejiahao/json/*  /data/suanfa/xuchen/down/2017.06.16baoxiandan_chejiahao/json/
cp /data/source/user8/0615baoxiandan_chejiahao/mark/*  /data/suanfa/xuchen/down/2017.06.16baoxiandan_chejiahao/mark/
cp /data/source/user8/0615baoxiandan_chejiahao/xml/*  /data/suanfa/xuchen/down/2017.06.16baoxiandan_chejiahao/xml
cp /data/source/user9/0615baoxiandan_chejiahao/json/*  /data/suanfa/xuchen/down/2017.06.16baoxiandan_chejiahao/json/
cp /data/source/user9/0615baoxiandan_chejiahao/mark/*  /data/suanfa/xuchen/down/2017.06.16baoxiandan_chejiahao/mark/
cp /data/source/user9/0615baoxiandan_chejiahao/xml/*  /data/suanfa/xuchen/down/2017.06.16baoxiandan_chejiahao/xml
cp /data/source/user11/0615baoxiandan_chejiahao/json/*  /data/suanfa/xuchen/down/2017.06.16baoxiandan_chejiahao/json/
cp /data/source/user11/0615baoxiandan_chejiahao/mark/*  /data/suanfa/xuchen/down/2017.06.16baoxiandan_chejiahao/mark/
cp /data/source/user11/0615baoxiandan_chejiahao/xml/*  /data/suanfa/xuchen/down/2017.06.16baoxiandan_chejiahao/xml
cp /data/source/user11/0615baoxiandan_chejiahao/json/*  /data/suanfa/xuchen/down/2017.06.16baoxiandan_chejiahao/json/
cp /data/source/user11/0615baoxiandan_chejiahao/mark/*  /data/suanfa/xuchen/down/2017.06.16baoxiandan_chejiahao/mark/
cp /data/source/user11/0615baoxiandan_chejiahao/xml/*  /data/suanfa/xuchen/down/2017.06.16baoxiandan_chejiahao/xml
cp /data/source/user12/0615baoxiandan_chejiahao/json/*  /data/suanfa/xuchen/down/2017.06.16baoxiandan_chejiahao/json/
cp /data/source/user12/0615baoxiandan_chejiahao/mark/*  /data/suanfa/xuchen/down/2017.06.16baoxiandan_chejiahao/mark/
cp /data/source/user12/0615baoxiandan_chejiahao/xml/*  /data/suanfa/xuchen/down/2017.06.16baoxiandan_chejiahao/xml





cp /data/source/user12/0703/0703z/json/*  /data/suanfa/xubenxiang/down/20170705/z/json/
cp /data/source/user12/0703/0703z/mark/*  /data/suanfa/xubenxiang/down/20170705/z/mark/
cp /data/source/user12/0703/0703z/xml/*  /data/suanfa/xubenxiang/down/20170705/z/xml/



cp /data/source/user11/0703/0703k/json/*  /data/suanfa/xubenxiang/down/20170705/k/json/
cp /data/source/user11/0703/0703k/mark/*  /data/suanfa/xubenxiang/down/20170705/k/mark/
cp /data/source/user11/0703/0703k/xml/*  /data/suanfa/xubenxiang/down/20170705/k/xml/
cp /data/source/user5/0615wuhan_xsz/json/*  /data/suanfa/xiaobo/down/2017.06.16wuhan_xsz/json/
cp /data/source/user5/0615wuhan_xsz/mark/*  /data/suanfa/xiaobo/down/2017.06.16wuhan_xsz/mark/
cp /data/source/user5/0615wuhan_xsz/xml/*  /data/suanfa/xiaobo/down/2017.06.16wuhan_xsz/xml/
cp /data/source/user7/0615wuhan_xsz/json/*  /data/suanfa/xiaobo/down/2017.06.16wuhan_xsz/json/
cp /data/source/user7/0615wuhan_xsz/mark/*  /data/suanfa/xiaobo/down/2017.06.16wuhan_xsz/mark/
cp /data/source/user7/0615wuhan_xsz/xml/*  /data/suanfa/xiaobo/down/2017.06.16wuhan_xsz/xml/







cp /data/source/user5/0111/json/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/json/
cp /data/source/user5/0111/mark/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/mark/
cp /data/source/user5/0111/xml/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/xml/
cp /data/source/user6/0111/json/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/json/
cp /data/source/user6/0111/mark/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/mark/
cp /data/source/user6/0111/xml/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/xml/
cp /data/source/user7/0111/json/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/json/
cp /data/source/user7/0111/mark/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/mark/
cp /data/source/user7/0111/xml/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/xml/
cp /data/source/user8/0111/json/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/json/
cp /data/source/user8/0111/mark/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/mark/
cp /data/source/user8/0111/xml/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/xml/
cp /data/source/user11/0111/json/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/json/
cp /data/source/user10/0111/mark/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/mark/
cp /data/source/user10/0111/xml/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/xml/
cp /data/source/user11/0111/json/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/json/
cp /data/source/user11/0111/mark/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/mark/
cp /data/source/user11/0111/xml/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/xml/
cp /data/source/user12/0111/json/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/json/
cp /data/source/user12/0111/mark/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/mark/
cp /data/source/user12/0111/xml/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/xml/
cp /data/source/user13/0111/json/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/json/
cp /data/source/user13/0111/mark/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/mark/
cp /data/source/user13/0111/xml/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/xml/
cp /data/source/user15/0111/json/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/json/
cp /data/source/user15/0111/mark/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/mark/
cp /data/source/user15/0111/xml/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/xml/
cp /data/source/user16/0111/json/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/json/
cp /data/source/user16/0111/mark/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/mark/
cp /data/source/user16/0111/xml/*  /data/suanfa/xubenxiang/down/2018.01.04xiangxiang/2018.01.11renlian_biaoding/xml/






cp /data/source/user17/2017.06.13xsz_chejiahao_char/mark/*  /data/suanfa/xuchen/down/2017.06.14_jianyanbaogao_roi/mark/
cp /data/source/user17/2017.06.13xsz_chejiahao_char/xml/*  /data/suanfa/xuchen/down/2017.06.14_jianyanbaogao_roi/xml/

cp /data/suanfa/xiaobo/down/2017.06.16baoxiandan_chejiahao/json/*  /data/suanfa/xuchen/down/2017.06.16_baoxiandan_chejiahao/json/
cp /data/suanfa/xiaobo/down/2017.06.16baoxiandan_chejiahao/mark/*  /data/suanfa/xuchen/down/2017.06.16_baoxiandan_chejiahao/mark/
cp /data/suanfa/xiaobo/down/2017.06.16baoxiandan_chejiahao/xml/*  /data/suanfa/xuchen/down/2017.06.16_baoxiandan_chejiahao/xml/

cp /data/source/user3//json/*  /data/suanfa/tongxinyu/down/chewei0607/user5/json/
cp /data/source/user3/chewei6.05/mark/*  /data/suanfa/tongxinyu/down/chewei0607/user5/mark/
cp /data/source/user3/chewei6.05/xml/*  /data/suanfa/tongxinyu/down/chewei0607/user5/xml/

cp /data/source/user2/dipan_chelian0606/json/*  /data/suanfa/tongxinyu/down/dipan_chelian0606/json/
cp /data/source/user2/dipan_chelian0606/mark/*  /data/suanfa/gaokaijun/down/dipan_chelian0606/mark/
cp /data/source/user2/dipan_chelian0606/xml/*  /data/suanfa/gaokaijun/down/dipan_chelian0606/xml/


cp /data/suanfa/tongxinyu/up/2017.0614_wuhan_xingshizheng/xsz_0614/*  /data/source/user9/0604wuhan_xsz/
cp /data/suanfa/tongxinyu/up/2017.0614_wuhan_xingshizheng/xsz_0613/*  /data/source/user5/2017.0614_wuhan_xingshizheng/
cp /data/suanfa/yuezhenya/up/xiaoche_tupian/chetou/7/*  /data/source/user12/0614chetou/7/

cp /data/suanfa/tongxinyu/up/xiaoche_tupian/chetou/8/*  /data/source/user6/0614chetou/8/
cp /data/suanfa/yuezhenya/up/xiaoche_tupian/chetou/9/*  /data/source/user12/0614chetou/9/

cp /data/suanfa/yuezhenya/up/xiaoche_tupian/chetou/4/*  /data/source/user12/0614chetou/4/

cp /data/source/user7/ret0603/bxd/*  /home/data/7.dachefenlei/
cp /data/source/user7/ret0603/bxd/*  /data/source/user1/0612bxd/bxd/
cp /data/source/user15/ret0603/bxd/*  /data/source/user1/0612bxd/bxd/



cp D:\360安全浏览器下载\*  D:\项目\





 











current_file_path="qian-fang1"
new_file_path="qian-fang1_moved"

i=1
for shname in `ls $current_file_path`
do
    #name=`echo "$shname" | awk -F\/ '{print $0}'`
    #name=`echo "$shname" | awk -F. '{print $0}'`
    if(($i%1000==0))
        mkdir -p ./$new_file_path/$[$i/1000]
        cp  $current_file_path/$shname ./$new_file_path/$[$i/1000]/
    then
        echo $i
        cp  $current_file_path/$shname/ ./$new_file_path/$[$i/1000]/
    fi
    i=$(($i+1))
done





分带有文件夹的文件

#需要移动的文件夹
current_file_path="MegafaceIdentities_VGG"


#移动到目的文件夹
new_file_path="MegafaceIdentities_VGG_moved"


#每个文件夹最大
max_folder_size=500


# check path persent
if [ ! -d "$new_file_path" ]; then
(mkdir ${new_file_path} && chmod 777 ${new_file_path})
fi
i=1


for shname in `ls $current_file_path`
do
name=`echo "$shname" | awk -F. '{print $1}'`
if(($i%500==0))
then
mkdir -p $new_file_path/$[$i/500]
cp -rf $current_file_path/$name $new_file_path/$[$i/500]/
echo "create folder ${i/5000}"
else
cp -rf $current_file_path/$name/ $new_file_path/$[$i/500]/
echo "copy ${i}"
fi
i=$(($i+1))
done




服务器获得权限
su chenwei 
 sudo chmod -R 777 folder

 cp /data/source/user7/10.11.1/result/0/json/*  /home/data/marked-data/OCR/qita/2017.10.11cheliangmingpai_gaokaijun/json/
 cp /data/source/user7/10.11.1/result/0/mark/*  /home/data/marked-data/OCR/qita/2017.10.11cheliangmingpai_gaokaijun/mark/
 cp /data/source/user7/10.11.1/result/0/xml/*  /home/data/marked-data/OCR/qita/2017.10.11cheliangmingpai_gaokaijun/xml/
 cp /data/source/user8/10.11.1/result/1/json/*  /home/data/marked-data/OCR/qita/2017.10.11cheliangmingpai_gaokaijun/json/
 cp /data/source/user8/10.11.1/result/1/mark/*  /home/data/marked-data/OCR/qita/2017.10.11cheliangmingpai_gaokaijun/mark/
 cp /data/source/user8/10.11.1/result/1/xml/*  /home/data/marked-data/OCR/qita/2017.10.11cheliangmingpai_gaokaijun/xml/
 cp /data/source/user10/10.11.1/result/2/json/*  /home/data/marked-data/OCR/qita/2017.10.11cheliangmingpai_gaokaijun/json/
 cp /data/source/user10/10.11.1/result/2/mark/*  /home/data/marked-data/OCR/qita/2017.10.11cheliangmingpai_gaokaijun/mark/
 cp /data/source/user10/10.11.1/result/2/xml/*  /home/data/marked-data/OCR/qita/2017.10.11cheliangmingpai_gaokaijun/xml/
 cp /data/source/user11/10.11.1/result/3/json/*  /home/data/marked-data/OCR/qita/2017.10.11cheliangmingpai_gaokaijun/json/
 cp /data/source/user11/10.11.1/result/3/mark/*  /home/data/marked-data/OCR/qita/2017.10.11cheliangmingpai_gaokaijun/mark/
 cp /data/source/user11/10.11.1/result/3/xml/*  /home/data/marked-data/OCR/qita/2017.10.11cheliangmingpai_gaokaijun/xml/
 cp /data/source/user12/10.11.1/result/4/json/*  /home/data/marked-data/OCR/qita/2017.10.11cheliangmingpai_gaokaijun/json/
 cp /data/source/user12/10.11.1/result/4/mark/*  /home/data/marked-data/OCR/qita/2017.10.11cheliangmingpai_gaokaijun/mark/
 cp /data/source/user12/10.11.1/result/4/xml/*  /home/data/marked-data/OCR/qita/2017.10.11cheliangmingpai_gaokaijun/xml/
 cp /data/source/user12/10.11.1/result/5/json/*  /home/data/marked-data/OCR/qita/2017.10.11cheliangmingpai_gaokaijun/json/
 cp /data/source/user12/10.11.1/result/5/mark/*  /home/data/marked-data/OCR/qita/2017.10.11cheliangmingpai_gaokaijun/mark/
 cp /data/source/user12/10.11.1/result/5/xml/*  /home/data/marked-data/OCR/qita/2017.10.11cheliangmingpai_gaokaijun/xml/

 cp /data/source/user1/10.11/json/*  /home/data/marked-data/OCR/qita/2017.10.11huanbaodan_yanghailin/json/
 cp /data/source/user1/10.11/mark/*  /home/data/marked-data/OCR/qita/2017.10.11huanbaodan_yanghailin/mark/
 cp /data/source/user1/10.11/xml/*  /home/data/marked-data/OCR/qita/2017.10.11huanbaodan_yanghailin/xml/
 cp /data/source/user2/10.11/json/*  /home/data/marked-data/OCR/qita/2017.10.11huanbaodan_yanghailin/json/
 cp /data/source/user2/10.11/mark/*  /home/data/marked-data/OCR/qita/2017.10.11huanbaodan_yanghailin/mark/
 cp /data/source/user2/10.11/xml/*  /home/data/marked-data/OCR/qita/2017.10.11huanbaodan_yanghailin/xml/

 cp /data/source/user16/10.12/json/*  /home/data/marked-data/OCR/qita/2017.10.12huanbaodan_gaokaijun/json/
 cp /data/source/user16/10.12/mark/*  /home/data/marked-data/OCR/qita/2017.10.12huanbaodan_gaokaijun/mark/
 cp /data/source/user16/10.12/xml/*  /home/data/marked-data/OCR/qita/2017.10.12huanbaodan_gaokaijun/xml/


 cp /data/source/user1/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/json/
 cp /data/source/user1/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/mark/
 cp /data/source/user1/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/xml/
 cp /data/source/user2/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/json/
 cp /data/source/user2/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/mark/
 cp /data/source/user2/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/xml/
 cp /data/source/user3/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/json/
 cp /data/source/user3/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/mark/
 cp /data/source/user3/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/xml/
 cp /data/source/user4/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/json/
 cp /data/source/user4/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/mark/
 cp /data/source/user4/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/xml/
 cp /data/source/user5/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/json/
 cp /data/source/user5/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/mark/
 cp /data/source/user5/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/xml/
 cp /data/source/user6/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/json/
 cp /data/source/user6/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/mark/
 cp /data/source/user6/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/xml/ 
 cp /data/source/user7/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/json/
 cp /data/source/user7/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/mark/
 cp /data/source/user7/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/xml/
 cp /data/source/user8/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/json/
 cp /data/source/user8/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/mark/
 cp /data/source/user8/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/xml/
 cp /data/source/user10/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/json/
 cp /data/source/user10/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/mark/
 cp /data/source/user10/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/xml/
 cp /data/source/user11/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/json/
 cp /data/source/user11/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/mark/
 cp /data/source/user11/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/xml/
 cp /data/source/user12/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/json/
 cp /data/source/user12/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/mark/
 cp /data/source/user12/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/xml/   
 cp /data/source/user13/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/json/
 cp /data/source/user13/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/mark/
 cp /data/source/user13/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/xml/ 
 cp /data/source/user14/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/json/
 cp /data/source/user14/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/mark/
 cp /data/source/user14/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.13chejiahao/xml/          


 cp /data/source/user1/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/json/
 cp /data/source/user1/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/mark/
 cp /data/source/user1/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/xml/
 cp /data/source/user2/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/json/
 cp /data/source/user2/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/mark/
 cp /data/source/user2/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/xml/
 cp /data/source/user3/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/json/
 cp /data/source/user3/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/mark/
 cp /data/source/user3/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/xml/
 cp /data/source/user4/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/json/
 cp /data/source/user4/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/mark/
 cp /data/source/user4/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/xml/
 cp /data/source/user5/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/json/
 cp /data/source/user5/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/mark/
 cp /data/source/user5/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/xml/
 cp /data/source/user6/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/json/
 cp /data/source/user6/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/mark/
 cp /data/source/user6/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/xml/ 
 cp /data/source/user7/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/json/
 cp /data/source/user7/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/mark/
 cp /data/source/user7/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/xml/
 cp /data/source/user8/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/json/
 cp /data/source/user8/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/mark/
 cp /data/source/user8/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/xml/
 cp /data/source/user10/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/json/
 cp /data/source/user10/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/mark/
 cp /data/source/user10/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/xml/
 cp /data/source/user11/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/json/
 cp /data/source/user11/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/mark/
 cp /data/source/user11/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/xml/
 cp /data/source/user12/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/json/
 cp /data/source/user12/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/mark/
 cp /data/source/user12/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/xml/   
 cp /data/source/user13/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/json/
 cp /data/source/user13/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/mark/
 cp /data/source/user13/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/xml/ 
 cp /data/source/user14/10.13/json/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/json/
 cp /data/source/user14/10.13/mark/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/mark/
 cp /data/source/user14/10.13/xml/*  /home/data/marked-data/OCR/2.chejiahao/chejian/2017.10.12bolixiachejiahao_gaokaijun/10.14chejiahao/xml/          