# UNITY

## GameObject中创建子对象

```C#
var gameObject = new GameObject("New Game Object");
gameObject.transform.parent = this.gameObject.transform;
```
