export 需要是接口，不是值

// 报错
function f() {}
export f;

// 正确
export function f() {};

// 正确
function f() {}
export {f};


import的 {}  里面的值，需要和export的值一样

export default 的接口 不用加大括号
