# UNITY

## GameObject中创建子对象

```cs
var gameObject = new GameObject("New Game Object");
gameObject.transform.parent = this.gameObject.transform;
```
