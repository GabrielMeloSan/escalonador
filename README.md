# Simulador de Escalonamento de Tarefas

Projeto prático da disciplina de Sistemas Operacionais, do 8º semestre do curso de Engenharia de Computação, ministrada por Vinicius Borges no 2º semestre de 2026.

## Autoria
- Henrique Alves Ferreira
- Matheus da Silva Souza
- Gabriel Melo Santos
- Rafael Ruppert Barrocal

## Descrição
Simulador de escalonamento de tarefas em um processador. Implementa seis algoritmos (FCFS, SJF, SRTF, Round-Robin e prioridade cooperativa e preemptiva), trata recursos de uso exclusivo e reproduz o fenomeno da inversão de prioridades, com os mecanismos de herança e teto de prioridade.

## Como executar

### Arquivo Executável

Clique duas vezes em `Simulador.exe`.
Nao e necessario instalar nada.

### Script Python

## Estrutura do repositório

```
simulador_escalonamento/
|-- Simulador.exe       Programa pronto para executar
|-- main.py             Ponto de entrada do codigo-fonte
|-- src/                Codigo-fonte do simulador
|-- cenarios/           Conjuntos de tarefas em JSON
`-- docs/               Tutoriais e documentacao tecnica
```

## Arquivos de código

- `src/view/` - interface gráfica
- `src/model/processo.py` - estrutura da tarefa
- `src/model/prioridade.py` - modelagem da prioridade da tarefa
- `src/control/simular_escalonamento.py` - raíz de chamado do simulador
- `src/control/motor.py` - motor de simulação
- `src/control/politicas.py` - modelagem das políticas de escalonamento
- `src/control/gerador.py` - gerador de tarefas e simulação em lotes
- `src/control/persistencia.py` - importação e exportação de tarefas em json
- `src/control/algoritmos/_base.py` - funções comuns dos algoritmos
- `src/control/algoritmos/nomes.py` - enumerador de nomes dos algoritmos
- `src/control/algoritmos/recursos.py` - funções para tratativa de uso de recursos

## Funcionalidades

| O que faz | Onde |
|-----------|------|
| Os seis algoritmos | `simulador/politicas.py` |
| Metricas por tarefa | `simulador/metricas.py` |
| Recurso exclusivo | `simulador/motor.py` |
| Heranca e teto | `simulador/motor.py` |
| Sorteio de cenarios | `simulador/gerador.py` |

## Documentação

- [Tutorial de execucao](./docs/tutorial_execucao.pdf)
- [Tutorial de uso](./docs/tutorial_uso.pdf)
- [Documentacao tecnica](./docs/documentacao_projeto.pdf)

## Por onde comecar

1. Abra o programa e siga o tutorial de execução
2. Reproduza um cenario de exemplo pelo tutorial de uso
3. Consulte a documentação técnica para entender o código