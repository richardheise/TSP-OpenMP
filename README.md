# Problema do Caixeiro Viajante (TSP) - Implementações Sequencial e Paralela

Este projeto contém implementações em C de algoritmos para resolver o Problema do Caixeiro Viajante (TSP), tanto de forma sequencial quanto paralela (usando OpenMP). O objetivo é comparar o desempenho das duas abordagens.

## Estrutura de Pastas

O repositório está organizado da seguinte forma:

- **/src**: Contém os códigos-fonte das implementações.
  - `tsp.c`: Implementação sequencial.
  - `tspp.c`: Implementação paralela com OpenMP.
  - `Makefile.sequential`: Makefile para compilar a versão sequencial.
  - `Makefile.parallel`: Makefile para compilar a versão paralela.

- **/tests**: Contém os arquivos de entrada (`.in`) para testar os algoritmos com diferentes quantidades de cidades.

- **/scripts**: Contém diversos scripts para automação de tarefas.
  - `run_sequential.sh` / `run_parallel.sh`: Executam as respectivas implementações para os testes.
  - `run_all.sh`: Script principal que executa todos os testes para ambas as versões.
  - `geratestes.py`: Script Python para gerar novos casos de teste.
  - `calc_statistics.py` / `plot_both_graphs.py`: Scripts para calcular estatísticas e gerar gráficos a partir dos resultados.

- **/results**: Armazena os arquivos de saída (`.out`) e estatísticas (`.st`) gerados pela execução dos algoritmos.
  - `sequential/`: Resultados da execução sequencial.
  - `parallel/`: Resultados da execução paralela.

## Como Compilar e Executar

### Compilação

1.  Navegue até a pasta `src`:
    ```bash
    cd src
    ```

2.  Para compilar a versão sequencial, use:
    ```bash
    make -f Makefile.sequential
    ```

3.  Para compilar a versão paralela, use:
    ```bash
    make -f Makefile.parallel
    ```
    Os executáveis (`tsp` e `tspp`) serão criados dentro da pasta `src`.

### Execução

Os scripts na pasta `scripts` foram configurados para encontrar os executáveis na pasta `src` e utilizá-los para processar os arquivos de teste da pasta `tests`.

- Para executar todos os testes e gerar os resultados, você pode usar o script principal na raiz do projeto:
  ```bash
  bash scripts/run_all.sh
  ```

## Dependências

- `gcc`
- `make`
- `OpenMP` (para a versão paralela)
- `python3` (para os scripts de análise e geração de testes)
