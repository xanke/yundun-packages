### 插入数据的三种方法

```javascript
await this.Model.create(create).then(result => {
  this.ctx.body = result
})
```

```javascript
const result = await this.Model.create(create)
this.ctx.body = result
```

```javascript
try {
  await this.Model.create(create)
} catch (e) {
  this.ctx.body = e
  return
}
this.ctx.body = create
```
