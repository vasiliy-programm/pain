# pain
const s1 = 1;
let s2 = 2;

const summ = (a, b) => a + b;

console.log('итого:' + summ(5, 6));
console.log('итого:' + summ(10058673.2834, -8583950.939394));

const hello = person => {
  console.log(`Здравствуйте, ${person.name}!`);
};

const vasia = { name: 'Василий Осицкий' };
const ania = { name: 'Анна Осицкая' };
const serega = { name: 'Сергей Осицкий' };

hello(vasia)
hello(ania)
hello(serega)

const vasiliy = 'Василий Осицкий';
const sergey = 'Сергей Осицкий';

const colors = [
  'чёрный',
  'красный',
  'зелёный',
  'жёлтый',
  'синий',
  'фиолетовый',
  'коричневый',
  'белый'
];
  
const colorer = (s, color) => `\x1b[3${color}m${s}\x1b[om`;

const pokras = name => {
  let res = '';
  const letters = name.split('');
  let color = 1;
  for (const letter of letters) {
    res += colorer(letter, color++);
    if (color > colors.length) color = 1;
  }
  return res;
};

const welcome = name => (
  name.includes('Василий') ?
  `Здравствуйте, ${pokras(name)}!` :
  `Здравствуйте, ${name}!`
);
  
console.log(welcome(vasiliy));
console.log(welcome(sergey));

const счёт1 = (а, б, в) => (а + б + в);
const счёт2 = (а, в) => счёт1(а, 10, в);
console.log(счёт2(2,3));
