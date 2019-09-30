# 交叉类型

交叉类型（Intersection Types）表示同时具备多种类型。交叉类型，只可能发生在非基本类型中。

交叉类型使用 `&` 链接每个类型。

```ts
interface Stu{
    school:string,
    class:string,
    grade:string
}
interface Person{
    weight:string,
    height:string,
    name:string
    age:number,
}
export type Student = Stu & Person;

```

上例中，stu具有Person,Stu 两个类型的所有属性, 访问共有属性是没问题的：

```ts
function getStudentInfo(stu:Student):string{
    return `name:${stu.name} age:${stu.age} school:${stu.school} grade:${stu.grade}`;
}
```

## 参考

- [Advanced Types # Intersection Types](http://www.typescriptlang.org/docs/handbook/advanced-types.html#intersection-types)（[中文版](https://zhongsp.gitbooks.io/typescript-handbook/content/doc/handbook/Advanced%20Types.html#联合类型)）

---

- [上一章：类型推论](type-inference.md)
- [下一章：对象的类型——接口](type-of-object-interfaces.md)
