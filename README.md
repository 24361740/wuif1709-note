# wuif1709-note
28日作业提交地址：

<!doctype html>
<html lang="en">
<head>

    <meta charset="UTF-8">
    <title>lianxi</title>
</head>
<body>

</body>
</html>
<script>
    成绩的输入
    var num=prompt("请输入成绩");
        if(num >=0 && num <60){
     	  alert('不及格');
        }else if(num >=60 && num <=100){
     	  alert('及格');
     	  if (num >60 && num <=75) {
     		 alert('一般')
     	  }else if(num > 75 && num <= 85){
     		 alert('良好')
     	  }else if(num >85 && num <=100){
     		 alert('优秀')
     	  }
     	  if (num = 100) {
     		 alert('满分')
     	  }
        }else{
     	alert('输入错误');
        }
    //  星期的输出
    var date=prompt('星期');
    switch(date){
        case '1':alert('周一');
        break;
        case '2':alert('周二');
        break;
        case '3':alert('周三');
        break;
        case '4':alert('周四');
        break;
        case '5':alert('周五');
        break;
        case '6':alert('周六');
        break;
        case '7':alert('周日');
        break;
        default :alert('输入错误');
    }
    //   四次运算
    var num1 =Number (prompt('请输入第一个数字'));
    var ope =prompt('请输入运算符');
    var num3 =Number (prompt('请输入第二个数字'));
    switch(ope){
        case '+':alert(`${num1}+${num3}=${num1+num3}`);
        break;
        case '-':alert(`${num1}-${num3}=${num1-num3}`);
        break;
        case '*':alert(`${num1}*${num3}=${num1*num3}`);
        break;
        case '/':alert(`${num1}/${num3}=${num1/num3}`);
        break;
    }   
//      奇偶数
    for(var a = 1;a <=100;a++){
        if (a % 2 == 0) {
            console.log(`这是偶数 -- ${a}`)
        }else if(a % 2 ==1){
            console.log(`这是奇数 -- ${a}`)
        }
    }
    // 九九乘法表
    for(var m = 1;m <= 9;m++){
        for(var n = 1;n <= m;n++){
            if ((m==3 || m ==4) && n == 2) {
                document.write(`${n}*${m}=${m*n}&nbsp &nbsp&nbsp`);
            }else{
                document.write(`${n}*${m}=${m*n}&nbsp&nbsp`);
            }
        }
        document.write('<br>');
    }
    // 金字塔
    for(i=6;i>=1;i--){
        for(a=1;a<=i;a++){
            document.write("&nbsp");
        }
        for(q=6;q>=i;q--){
            document.write("*");
            document.write("&nbsp");
        }
        document.write("<br/>");
    }
// 水仙花数
    for(a = 100;a < 1000;a++){
        var b = a % 10;
        var c = parseInt(a / 100);
        var d = parseInt(a % 100 / 10);
        if (b**3+c**3+d**3==a) {
            console.log(a);
        }
    }
// 鸡兔同笼，头有34，脚有96，有多少只鸡与兔?

    for(var a =0;a <=34;a++){
        for(var b =0;b <=34-a;b++){
            if ((a+b==34) && (2*a+4*b==96)) {
                 document.write(`兔${a}只 鸡${b}只`);
            }
        }
    }  
    // 操场上有一百多个人，三排余一人，四排余二人，五排余三人，问一共有多少人？
    for(var a = 100;a <200;a++){
        if ((a % 3 ==1)&&(a % 4 ==2)&&(a % 5 ==3)) {
            console.log(a);
        }
    }  
    // 教材10元/本，参考书5元/本，练习本0.5元/本。100元买了100本书，各种书各有几本？
    for(var a = 0;a <=100;a++){
        for(var b = 0;b <=100-a;b++){
            for(var c = 0;c <=100-a-b;c++){
                if ((a+b+c==100) && (10*a+5*b+0.5*c==100)) {
                    console.log(`教材${a}参考书${b}练习本${c}`);
                }
            }
        }
    }
    // 十乘十表格+隔行换色+交叉换色
    var tab = '<table width="500px" height="500px" cellspacing="0">';
    for(var b = 0;b <10;b++){
        tab +='<tr>';
        for(var c =0;c <10;c++){
            if (b%2==0 && c%2==0) {
                tab +='<th bgColor="white"></th>';
            }else if (b%2==1 && c%2==1) {
                tab +='<th bgColor="white"></th>';
            }else if (b%2==1 && c%2==0) {
                tab +='<th bgColor="black"></th>';
            }else{
                tab +='<th bgColor="black"></th>';
            }
        }
        tab +='</tr>';
    }
    tab += '</table>';
    document.write(tab);
    // 数组去空
    var a = [18,24,3,,68,'ds','gf',,85];
    var b = [];
    for(var i = 0;i < a.length;i++){
        if(a[i] !== undefined){
            b[b.length] = a[i];
        }
    }
    console.log("数组去空后是：" + b);
    
    // 最大值
    var arr = [18,24,3,68,36,85];
    var max = arr[0];
    for(var i = 0;i < arr.length;i++){
        if(max < arr[i]){
            max = arr[i];
        }
    }
    console.log("数组的最大值是：" + max);
    
    // 最小值
    var arr = [18,24,3,68,36,85];
    var min = arr[0];
    for(var i = 0;i < arr.length;i++){
        if(min > arr[i]){
            min = arr[i];
        }
    }
    console.log("数组的最小值是：" + min);
    
    // 平均值
    var arr = [18,24,3,68,36,85];
    var sum = 0;
    for(var i = 0;i < arr.length;i++){
        sum += arr[i];
        }
    var ave = sum / arr.length;
    console.log("数组的平均数是：" + ave);
    
    // 数组排序：从大到小
    var arr = [18,24,3,68,36,85];
    for(var i = 0;i < arr.length-1;i++){
        for(var j = 0;j < arr.length-1-i;j++){
            if(arr[j] < arr[j+1]){
                var xu = arr[j];  
                arr[j] = arr[j+1];  
                arr[j+1] = xu;
            }
        }
    }
    console.log("从大到小的排序："+ arr);
    
    // 数组排序：从小到大
    var arr = [18,24,3,68,36,85];
    for(var i = 0;i < arr.length-1;i++){
        for(var j = 0;j < arr.length-1-i;j++){
            if(arr[j] > arr[j+1]){
                var xu = arr[j];  
                arr[j] = arr[j+1];  
                arr[j+1] = xu;
            }
        }
    }
    console.log("从小到大的排序："+ arr);
    
    var arr = [18,24,3,68,36,85];
    for(var i = 0;i < arr.length;i++){
        for(var j = i + 1;j < arr.length;j++){
            if(arr[i] > arr[j]){
                var num = arr[i];
                arr[i] = arr[j];
                arr[j] = num;
            }
        }
    }
    console.log("从小到大的排序："+ arr);
    
    // 数组筛选数据类型
    var arr = [-1,32,,56,'a',93,0,-34];
    for(var i = 0; i < arr.length; i++) {
        if(typeof arr[i] == 'number') {
        console.log("arr数组中是Number类型的有：" + arr[i]);
        }
    }
    
    // 筛选数组中大于0的数
    var arr = [-1,32,56,'a',93,0,-34];
    for(var i = 0; i < arr.length; i++) {
        if(arr[i] > 0) {
        console.log("arr数组中大于0的数有：" + arr[i]);
        }
    }
    
    // 将数组里每个元素扩大二倍
    var arr = [18,24,3,56,68,'ds','gf'];
    for(var i = 0;i < arr.length;i++){
        arr[i]*=2;
    }
    console.log("数组中每个元素扩大两倍后是："+ arr);
    
    // 反向输出数组中的各元素
    var arr = [8,24,3,56,68,1];
    var newArr = [];
    for(var i = arr.length - 1;i >= 0;i--){
        newArr[newArr.length] = arr[i];
    }
    console.log("反向输出数组元素是：" + newArr);
    
    // 数组合并
    var x = [8,24,3,56,68,1];
    var y = [18,24,3,,68,'ds','gf',,85];
    for(var i = 0;i < y.length;i++){
        x[x.length] = y[i];
    }
    console.log("数组合并后是：" + x);
封装四则运算
    var num1 = Number(prompt('请输入第一个值'));
    if(isNaN(num1)){
     alert('请重新输入');
    }
    var num2 = Number(prompt('请输入第二个值'));
    if(isNaN(num2)){
     alert('请重新输入');
    }
    var symbol = prompt('请输入运算符');
    function SZ(num1,num2,symbol){
     switch(symbol){
         case '+':alert(`${num1}+${num2}=${num1+num2}`);
         break;
         case '-':alert(`${num1}-${num2}=${num1-num2}`);
         break;
         case '*':alert(`${num1}*${num2}=${num1*num2}`);
         break;
         case '/':alert(`${num1}/${num2}=${num1/num2}`);
         break;
         case '%':alert(`${num1}%${num2}=${num1%num2}`);
         break;
         default:alert('请重新输入');
     }
    }
    SZ(num1,num2,symbol);



    封装九九乘法表
    function nine(n){
        for(var a = 1; a <= n; a++){
            for(var b=1; b <= a; b++){
                if((a == 3) || (a == 4) && (b == 4)){
                   document.write(`${a}*${b}=${a*b}`);
                }else{
                     document.write(`${a}*${b}=${a*b}`);
                }
                document.write('&nbsp;'); 
            }
             document.write("<br />");
        }
    }
    nine(5);


    封装金字塔
    function JZT(num){
        for(var h = 1;h <= num;h++){
            for(var k = 1;k <= num-h;k++){
                document.write('&nbsp;');
            }
            for(var x = 1;x <= h;x++){
                document.write('*&nbsp; ');
            }
            document.write('<br />');
        }
    }
    JZT(10);



    封装表格：
    function biao(hang,lie){
        var tab = '<table width="600px" height="600px" border="1px" cellspacing="0">';
        for(var i = 0;i < hang;i++){
            tab += '<tr">';
            for(var j = 0;j < lie;j++){
                tab += '<td></td>';
            }
            tab += '</tr>';
        }
        tab += '</table>';
        document.write(tab);
    }
    biao(3,8);


    function biao1(hang,lie){
        var tab = '<table width="600px" height="600px" border="1px" cellspacing="0">';
        for(var i = 0;i < 10;i++){
            if(i % 2 == 0){
                tab += '<tr bgColor="pink">';
            }else{
                tab += '<tr bgColor="yellow">';
            }
            for(var j = 0;j < 10;j++){
                tab += '<td></td>';
            }
            tab += '</tr>';
        }
    tab += '</table>';
    document.write(tab); 
    }
    biao1(10,15);


    function TAB(hang,lie){
        hang = hang || 10;
        lie = lie || 10;
        var tab1 = '<table width="600px" height="600px" border="1px" cellspacing="0">';
            for(var i = 0;i < hang;i++){
                tab1 += '<tr>';
                for(var j = 0;j < lie;j++){
                    // tab1 += '<td bgColor="red"></td>';
                    if((i % 2 == 1) && (j % 2 == 1)){
                        tab1 += '<td bgColor="blue"></td>';
                    }else if((i % 2 == 0) && (j % 2 == 0)){
                        tab1 += '<td bgColor="red"></td>';
                    }else if((i % 2 == 1) && (j % 2 == 0)){
                        tab1 += '<td bgColor="yellow"></td>';
                    }else{
                        tab1 += '<td bgColor="green"></td>';
                    }
                }
                tab1 +='</tr>'
            }
        tab1 += '</table>';
        document.write(tab1);
    }
    TAB(5,10)


    //封装数组去空
    function QK(a){
        var b = [];
        for(var i = 0;i < a.length;i++){
            if(a[i] !== undefined){
                b[b.length] = a[i];
            }
        }
        console.log("数组去空后是：" + b);
    }
    QK([19,24,,3,432,,53])



    //封装数组求最大值
    function MAX(arr){
        var max = arr[0];
        for(var i = 0;i < arr.length;i++){
            if(max < arr[i]){
                max = arr[i];
            }
        }
        console.log("数组的最大值是：" + max);
    }
    MAX([18,24,3,68,36,152])



    // 封装数组求最小值
    function MIN(arr){
        var min = arr[0];
        for(var i = 0;i < arr.length;i++){
            if(min > arr[i]){
                min = arr[i];
            }
        }
        console.log("数组的最小值是：" + min);
    }
    MIN([18,24,3,68,36,152])



    // 封装数组求平均值
    function AVE(arr){
        var sum = 0;
        for(var i = 0;i < arr.length;i++){
            sum += arr[i];
            }
        var ave = sum / arr.length;
        console.log("数组的平均数是：" + ave);
    }
    AVE([18,24,3,68,36,152])



    // 封装数组排序：从大到小
    function BS(arr){
        for(var i = 0;i < arr.length-1;i++){
            for(var j = 0;j < arr.length-1-i;j++){
                if(arr[j] < arr[j+1]){
                    var xu = arr[j];  
                    arr[j] = arr[j+1];  
                    arr[j+1] = xu;
                }
            }
        }
    console.log("从大到小的排序："+ arr);
    }
    BS([18,24,3,68,36,152])



    // 封装数组排序：从小到大
    function SB(arr){
        for(var i = 0;i < arr.length-1;i++){
            for(var j = 0;j < arr.length-1-i;j++){
                if(arr[j] > arr[j+1]){
                    var xu = arr[j];  
                    arr[j] = arr[j+1];  
                    arr[j+1] = xu;
                }
            }
        }
    console.log("从大到小的排序："+ arr);
    }
    SB([18,24,3,68,36,152])


    // 封装数组筛选数据类型
    function SX(arr){
        for(var i = 0; i < arr.length; i++) {
            if(typeof arr[i] == 'number') {
            console.log("arr数组中是Number类型的有：" + arr[i]);
            }
        }
    }
    SX([18,,24,'a',68,36,152])



    // 封装筛选数组中大于0的数
    function SX(arr){
        for(var i = 0; i < arr.length; i++) {
            if(arr[i] > 0) {
            console.log("arr数组中大于0的数有：" + arr[i]);
            }
        }
    }
    SX([-18,,24,'a',68,-36,152])



    // 封装数组里每个元素扩大二倍
    function KD(arr){
        for(var i = 0;i < arr.length;i++){
            arr[i]*=2;
        }
        console.log("数组中每个元素扩大两倍后是："+ arr);
    }
    KD([-18,,24,'a',68,-36,152])



    // 封装反向输出数组中的各元素
    function FX(arr){
        var newArr = [];
        for(var i = arr.length - 1;i >= 0;i--){
            newArr[newArr.length] = arr[i];
        }
        console.log("反向输出数组元素是：" + newArr);
    }
    FX([-18,,24,'a',68,-36,152])



    // 封装数组合并
    function HB(x,y){
        for(var i = 0;i < y.length;i++){
            x[x.length] = y[i];
        }
        console.log("数组合并后是：" + x);
    }
    HB([-18,,24,'a',68,-36,152],[8,24,3,56,68,1])



    // 找出数组中是否包含某个元素，包含返回true，不包含返回false
    // var arr=;
    function con(arr,num){
        for(var i=0; i<arr.length; i++){
            if(arr[i] == num){
                return true;
            }
        }
        return false;
    }
    console.log(con([18,2,3,16,12,41,87],32));



    //数组查找，查找数组中是否包含a元素，包含则返回此元素的下标，不包含则返回-1
    var arr=[5,2,3,18,12,41,87];
    function Index(arr,num){
        for(var i=0; i<arr.length; i++){
            if(arr[i] == a){
                return i;
            }
        }
        return -1;
    }
    console.log(Index(arr,41));




    //将数组转换为字符串，默认用-链接
    function link(arr){
        b = "" || "-";
        var str = '';
        for(var i=0; i<arr.length; i++){
            if(i == arr.length-1){
                str = str + arr[i];
            }else{
                str = str + arr[i] + '-';
            }
        }
        return str;
    }
    console.log(link([1,2,3]));


    	// 数组的去重//
    function qc(arr){
        var newArr = [];
        for(var i = 0; i < arr.length; i++){
            var flag = true; 
            for(var j = i+1; j < arr.length; j++){
                if(arr[i] == arr[j]){
                    flag = false;
                }
            }
            if(flag == true){
                newArr[newArr.length] = arr[i];
            }
        }
       return newArr;
   }
   console.log(qc([1,23,1,1,1,3,23,5,6,7,9,9,8,5]));

</script>