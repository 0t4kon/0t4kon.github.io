---
title: "Code Synax Test"
date: 2025-05-09T15:00:00+08:00
author: "guts"
tags: ["Hugo", "Markdown", "Code"]
categories: ["Introduction"]
draft: false
---

# 代码测试
## CPP
```cpp
    int main(void)
    {
    
      GPIO_InitTypeDef  GPIO_InitStructure;
      RCC_AHB1PeriphClockCmd(RCC_AHB1Periph_GPIOF, ENABLE);
    
      GPIO_InitStructure.GPIO_Pin = GPIO_Pin_9 | GPIO_Pin_10;
      GPIO_InitStructure.GPIO_Mode = GPIO_Mode_OUT;
      GPIO_InitStructure.GPIO_OType = GPIO_OType_PP;
      GPIO_InitStructure.GPIO_Speed = GPIO_Speed_100MHz;
      GPIO_InitStructure.GPIO_PuPd = GPIO_PuPd_UP;
      GPIO_Init(GPIOF, &GPIO_InitStructure);
    
      while(1){
    		GPIO_SetBits(GPIOF,GPIO_Pin_9|GPIO_Pin_10);
    		Delay(0x7FFFFF);
    		GPIO_ResetBits(GPIOF,GPIO_Pin_9|GPIO_Pin_10);
    		Delay(0x7FFFFF);
      
    	}
    }
    
```