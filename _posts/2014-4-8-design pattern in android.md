---

layout: post
categories: [Computer Vision]
tags: [增强现实 ,AR, 机器视觉, 算法]

---

**参考链接**：

http://www.cnblogs.com/qianxudetianxia/tag/Android%E8%AE%BE%E8%AE%A1%E6%A8%A1%E5%BC%8F%E7%B3%BB%E5%88%97/

一，组合模式

View + ViewPager

二，观察者模式

AbstractCursor

三，单例模式

输入法（InputMethodManager） 状态栏等

四，模板方法模式

View中的方法 onDraw() dispatchDraw()

    public class View{
    
    protected void onDraw(Canvas canvas) {
    }
 
    protected void dispatchDraw(Canvas canvas) {
    }
 
    //算法骨架
    public void draw(Canvas canvas) {
       if (!verticalEdges && !horizontalEdges) {
            // 步骤1
            if (!dirtyOpaque) onDraw(canvas);
 
            // 步骤2
            dispatchDraw(canvas);
 
            // 步骤3
            onDrawScrollBars(canvas);
 
            return;
        }
    }
    //... ...
}


五，备忘录模式

Canvas save（） restore()方法

六，共享元模式

sqlite 请求sql，对于重复的sql的返回结果，会缓存。

客户端通过享元工厂获取享元对象，享元对象的创建则根据工厂的享元池来控制，如果有享元池中没有这个对象，则创建这个对象并保存到享元池中，如果享元池中有这个对象，则直接使用这个对象。因为享元对象在共享的同时，说明它重用属性的不变性，不然都是变化的东西，不存在共享，这些不变得属性我们称之为内部状态，独立与外部场景。

七，命令模式

封装了接受者和操作

new Thread(new Runnable(){}).start()

八，工厂模式

Asynctask中的ThreadFactory

   

     private static final ThreadFactory sThreadFactory = new ThreadFactory() { 
     private final AtomicInteger mCount = new AtomicInteger(1);
     public Thread newThread(Runnable r) { 
            return new Thread(r, "AsyncTask #" + mCount.getAndIncrement());  
       }
    }; 
   
             
九，适配器模式

adapter

十，原型模式

Cloneable接口

十一，策略模式

暂时理解为多态的内涵

十二，建造者模式
builder


