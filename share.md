dajngo jwt demo  
https://blog.csdn.net/2201_75632987/article/details/142929840  


三、每条数据满足以下条件：  
1.电源档位_(12D)为ON档    
2.空调出风档位_(404)非0档    
3.左冷暖电机反馈AD_(4EB-03)非0     
4.右冷暖电机反馈AD_(4EB-03)非0       
5.(左通道目标温度_(4EB-04)-左吹面通道温度_(4EB-04)>10℃ )or (右通道目标温度_(4EB-04)-右吹面通道温度_(4EB-04))＞10℃    

四、数据处理，对于每天，每个VIN：  
    若：PTC冷却液温度_(4EB-03)＞40℃时，若 PTC冷却液温度_(4EB-03)-左吹面通道温度_(4EB-04)＞20℃    
    则将数据命名为，干烧异常  
    若：PTC冷却液温度_(4EB-03)＜40℃时，压缩机控制档位_(4EB-02) 和 PTC目标档位_(4EB-03) 均为0，持续30s  
    则将数据命名为鼓风机异常  
