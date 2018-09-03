##Delimiter definition 

A delimiter is a sequence of one or more characters used to specify the boundary between separate, independent regions in plain text or other data stream

##Delimiter 사용방범
golang 에서는 strings.split 라는 함수를 통해 사용합니다 
예시) 0.0.0.0 으로 [0 0 0 0] 으로변환 할려면 string 0.0.0.0 의 이름을 str 이라고 하면 strings.split("str", ".") 하면 [0 0 0 0]으로 바뀌게 됩니다 

##Delimiter 쓰는이유 
문자열속에 많은 문자열이 존재하는데 분리를 해야하는경우에 용인하게 쓰게되죠 
