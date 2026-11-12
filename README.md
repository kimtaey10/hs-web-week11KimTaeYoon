# hs-web-week11KimTaeYoon
kimweb1112week11
javascript
function circleArea(radius) {
    return Math.PI * radius ** 2;
}

let result = circleArea(5);
console.log(result.toFixed(2));

javascript
const scores = [95, 42, 88, 67, 55];

// 60점 이상인 점수만 골라 새 배열 만들기
const passed = scores.filter(score => score >= 60);

// 개수 구하기
const count = passed.length;

// 평균 구하기
const average = passed.reduce((sum, score) => sum + score, 0) / count;

console.log("새 배열:", passed);
console.log("개수:", count);
console.log("평균:", average.toFixed(2)


const students = [
    { name: "김민수", year: 1, score: 90 },
    { name: "이영희", year: 2, score: 85 },
    { name: "박철수", year: 1, score: 95 },
    { name: "최유진", year: 3, score: 80 }
];

const firstGrade = students.filter(student => student.year === 1);

const names = firstGrade.map(student => student.name);

console.log(names.join(", "))



const products = [
    { id: 1, name: "노트북", price: 1000000, stock: 5 },
    { id: 2, name: "마우스", price: 30000, stock: 0 },
    { id: 3, name: "키보드", price: 50000, stock: 10 },
    { id: 4, name: "모니터", price: 300000, stock: 0 },
    { id: 5, name: "태블릿", price: 500000, stock: 3 }
];

// ① 총 재고 금액
const total = products.reduce(
    (sum, product) => sum + product.price * product.stock, 0
);

// ② 재고가 0인 상품 이름
const soldOut = products
    .filter(product => product.stock === 0)
    .map(product => product.name);

// ③ 가장 비싼 상품
const expensive = [...products].sort(
    (a, b) => b.price - a.price
)[0];

console.log("총 재고 금액:", total);
console.log("재고가 0인 상품:", soldOut.join(", "));
console.log("가장 비싼 상품:", expensive.name)
