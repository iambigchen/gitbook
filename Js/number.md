parseInt

会忽略字符串前面的空格，如果第一个字符不是数字字符或者负号，会返回NaN。会继续解析第二个字符，直到遇到非数字的字符



parseInt(Num, 基数) 基数表示Num为几进制的

parseInt(0x15, 8) 先将0x15转为10进制，后该数以8进制去转化10进制

parseInt(Num, 8)

parseInt(Num, 16)



parseFloat

会忽略字符串前面的空格，如果第一个字符不是数字字符或者负号，会返回NaN。会继续解析第二个字符，直到遇到非数字的字符（第一个小数点不会结束）