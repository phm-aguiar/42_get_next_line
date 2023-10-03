# 42_get_next_line

## Descrição
O projeto 42_get_next_line é uma implementação da função `get_next_line`, que lê uma linha de um arquivo de texto ou descritor de arquivo e a retorna. O objetivo principal deste projeto é aprimorar suas habilidades de programação em C, especialmente em relação ao uso de listas ligadas, enquanto enfrenta restrições específicas de código.

## Funcionalidades
- Leitura de linhas de arquivos ou descritores de arquivo.
- Manipulação de múltiplas chamadas da função `get_next_line` em um mesmo arquivo.

## Como usar
Para usar a função `get_next_line`, inclua o arquivo header fornecido em seu código e chame a função conforme mostrado no exemplo abaixo:

```c
#include "get_next_line.h"

int main()
{
    int fd;
    char *line;

    fd = open("exemplo.txt", O_RDONLY);
    while (get_next_line(fd, &line) > 0)
    {
        // Faça algo com a linha lida
        printf("%s\n", line);
        free(line);
    }
    close(fd);
    return (0);
}
```
Certifique-se de que o arquivo header get_next_line.h esteja no mesmo diretório do seu código fonte.

Desafios
Limitação de apenas 2 arquivos de código com 5 funções limitadas a 25 linhas cada.
Gerenciamento de vazamentos de memória (leaks) e erros de segmentação (segfaults).

## Autor
Este projeto foi criado por phenriq2 cadet at 42.



## Licença
Este projeto é licenciado sob os termos da [Licença MIT](LICENSE). Consulte o arquivo [LICENSE](LICENSE) para obter detalhes sobre os direitos e limitações da licença.

---

**Nota:** Este projeto foi criado por phm-aguiar como parte do curso software engineer na 42sp. Sinta-se à vontade para contribuir, relatar problemas ou fornecer feedback para melhorias. Estou ansioso para colaborar com a comunidade de desenvolvedores.


