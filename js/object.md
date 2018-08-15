# 构造函数的方法
Object.create(obj)
可以把obj当做__proto__

Object.defineProperty()
Object.defineProperties()

Object.freeze()

Object.getOwnPropertyDescriptor()

Object.getOwnPropertyNames()

Object.getPrototypeOf()   prototype

Object.isExtensible()

Object.isFrozen()

Object.isSealed()

Object.keys(obj)

Object.preventExtensions()

Object.seal(obj)

Object.setPrototypeOf(obj, prototype)

# ie不支持
Object.assign()

Object.entries()

Object.is()

Object.values(obj)


# 实例方法
所有对象都会从它的原型上继承一个 constructor 属性：

使用prototype继承的时候，可以重新把constructor指向正确的构造函数，保证构建的正确性

hasOwnProperty和in的区别是可以去掉从原型链继承的属性

isPrototypeOf 方法用于测试一个对象是否存在于另一个对象的原型链上。

isPrototypeOf() 与 instanceof 运算符不同。在表达式 "object instanceof AFunction"中，object 的原型链是针对 AFunction.prototype 进行检查的，而不是针对 AFunction 本身。
