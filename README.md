# metashape-batch-automator

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Metashape](https://img.shields.io/badge/Agisoft-Metashape_Pro-blue?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)

## Sobre o Projeto

O **Metashape Batch Automator** é um script em Python desenvolvido para automatizar o pipeline completo de processamento fotogramétrico no Agisoft Metashape Professional. 

Processar grandes volumes de imagens de drones (seja para agricultura de precisão, topografia ou inspeção de ativos) exige tempo e diversas interações manuais com a interface do software. Este projeto elimina o tempo de ociosidade do operador, executando o alinhamento de câmeras, geração de nuvem de pontos densa, Modelo Digital de Elevação (DEM) e Ortomosaico em lote, diretamente via linha de comando (CLI).

## Principais Funcionalidades

- **Importação em Lote:** Carrega automaticamente todas as imagens de um diretório especificado.
- **Pipeline Completo 3D e 2D:** Executa `matchPhotos`, `alignCameras`, `buildDepthMaps`, `buildDenseCloud`, `buildDem` e `buildOrthomosaic` de forma sequencial.
- **Exportação Automática:** Salva os produtos finais (Ortomosaico e DEM) em formato `.tif` e o projeto `.psx` para consultas futuras.
- **Interface de Linha de Comando (CLI):** Parametrização fácil de diretórios de entrada, saída e qualidade de processamento.

## Como Usar

### Pré-requisitos
- **Agisoft Metashape Professional** (A versão Standard não possui suporte à API Python).
- **Python 3.x** configurado nas variáveis de ambiente.

### Instalação
Clone este repositório para sua máquina local:
```bash
git clone [https://github.com/SEU_USUARIO/metashape-batch-automator.git](https://github.com/SEU_USUARIO/metashape-batch-automator.git)
cd metashape-batch-automator
````

Execução via CLI
Execute o script passando os parâmetros necessários. Exemplo:

```bash
python automator.py --input "C:/imagens_voo/fazenda_alvo" --output "C:/resultados/ortomosaicos" --quality high
```

Roadmap

• [ ] Implementar leitura de logs de voo para processamento PPK (Post-Processed Kinematic) automatizado.

• [ ] Adicionar suporte para importação de coordenadas de Pontos de Controle (GCPs).

• [ ] Geração automática de relatórios de processamento em PDF.

Autor
Pedro

Sinta-se à vontade para abrir uma Issue ou enviar um Pull Request se tiver ideias para melhorar o pipeline!
