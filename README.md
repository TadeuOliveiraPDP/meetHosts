# About

Projeto proposto no WeLearn com finalidade de implementar um algoritmo para selecionar hosts para apresentações.

# Enunciado (v1)

Implemente um algoritmo que receba uma lista de colaboradores e retorne uma estrutura que indique quem irá apresentar cada tema e em que data.

Restrições:

- Numa reunião com apenas um host, um colaborador não pode ser host se ele tiver menos de 1 mês de contribuição
- Numa reunião com dois hosts, pelo menos um deles deve ter mais de 3 meses de contribuição
- Um mesmo colaborador pode ser host/co-host de apenas uma apresentação por sprint
- Um colaborador não pode ser host no mesmo tipo de reunião duas semanas seguidas
  
(Extra) organize as apresentações de forma a haver o maior intervalo possível entre apresentações de cada colaborador.

Exemplo de input:
```
[
    {nome: 'Maria', entrada: '2022-02-01'},
    {nome: 'João', entrada: '2021-01-01'},
    {nome: 'Pedro', entrada: '2022-10-06'},
    {nome: 'Ana', entrada: '2022-10-03'}
]
```

Exemplo de output:
```
{
    sprintI: {
        refinamento: {
            data: '2022-10-13',
            host: 'Maria'
        },
        retro: {
            data: '2022-10-17',
            hosts: ['João', 'Pedro']
        }
    },
    sprintII: {
        refinamento: {
            data: '2022-10-27',
            host: 'João'
        },
        retro: {
            data: '2022-10-31',
            hosts: ['Maria', 'Ana']
        }
    },
}
```