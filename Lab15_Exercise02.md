# Lab 15 Exercise 2

## Delegate on instance and static method

1.สร้าง console application project

```cmd
dotnet new console --name Lab15_Ex02
```

2.เปลี่ยน code ให้เป็นดังต่อไปนี้

```cs
var im = new InstanceMethod();
MyDelegate del = im.MethodA;
del("Hello World");
del = StaticMethod.MethodB;
del("Hello Moon");

class InstanceMethod
{
     public void MethodA(string message)
     {
        System.Console.WriteLine($"You are calling instance MethodA() with message {message}");
     }
}
static class StaticMethod
{
     public static void MethodB(string message)
     {
        System.Console.WriteLine($"You are calling static MethodB() with message {message}");
     }
}

public delegate void MyDelegate(string message);
```

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab15_Ex02
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab15_Ex02
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5

7.อธิบายสิ่งที่พบในการทดลอง
