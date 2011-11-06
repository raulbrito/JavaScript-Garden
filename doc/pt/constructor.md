## O  constructor do `Array`

Visto que o constructor do `Array` é ambíguo na forma como age com os seus parâmetros,
é altamente recomendado utilizar a notação literal do Array - `[]` - 
na criação de novos vectores.

    [1, 2, 3]; // Resultado: [1, 2, 3]
    new Array(1, 2, 3); // Resultado: [1, 2, 3]

    [3]; // Resultado: [3]
    new Array(3); // Resultado: []
    new Array('3') // Resultado: ['3']

No caso de haver só um parâmetro passado ao constructor do `Array`, e
esse argumento ser um `Number`, o constructor retorna um novo
vector *esparço* com a propriedade `length` com o valor do argumento.
Além disso, *só* a propriedade `length` do novo vector é definida desta
maneira; os indices do vector não são inicializados.

    var arr = new Array(3);
    arr[1]; // indefinido
    1 in arr; // falso, o índice nao foi definido

O facto de ser possivel definir o tamanho do vector inicialmente só
é util nalguns casos, tal como na repetição de um objecto de tipo
`String´, visto que evita a utilização de um ciclo `for`.

    new Array(count + 1).join(stringToRepeat);

### Em conclusão

O uso do constructor do `Array` deve ser evitado tanto como possivel. Os
literais são definitivamente preferidos. Sao mais curtos e tem uma
sintaxe mais clara; o que aumenta a legibilidade do código.
