---
title: Como usar o Azure PowerShell no Docker
description: Como usar o Azure PowerShell que é pré-instalado em uma imagem do Docker.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 48935f15241ec965adf4c34d2c17aa670110585a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "97893493"
---
# <a name="using-azure-powershell-in-docker"></a>Como usar o Azure PowerShell no Docker

Estamos publicando imagens do Docker com o Azure PowerShell pré-instalado. Este artigo mostra como começar a usar o Azure PowerShell no contêiner do Docker.

## <a name="finding-available-images"></a>Localizar imagens disponíveis

As imagens liberadas exigem o Docker 17.05 ou mais recente. Também é esperado que você possa executar o Docker sem `sudo` ou direitos administrativos locais. Siga as [instruções][install] oficiais do Docker para instalar o `docker` corretamente.

A imagem de contêiner mais recente contém a versão mais recente do PowerShell e os módulos do Azure PowerShell mais recentes compatíveis com o módulo Az.

Para cada nova versão do módulo Az, estamos lançando uma imagem para os seguintes sistemas operacionais:

- Ubuntu 18.04 (padrão)
- Debian 9
- CentOs 7

Uma lista completa de imagens disponíveis pode ser encontrada em nossa página de [imagem do Docker][az image].

## <a name="using-azure-powershell-in-a-container"></a>Usar o Azure PowerShell em um contêiner

As etapas a seguir mostram os comandos do Docker necessários para baixar a imagem e iniciar uma sessão interativa do PowerShell.

1. Baixe a imagem do azure-powershell mais recente.

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. Execute o contêiner do azure-powershell no modo interativo:

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

Para hosts do Windows Docker, é preciso habilitar o compartilhamento de arquivos do Docker para permitir que unidades locais no Windows sejam compartilhadas com contêineres do Linux. Para saber mais, confira [Introdução ao Docker for Windows][file-sharing].

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a>Executar o contêiner do azure-powershell interativamente usando a autenticação de host

Se já tiver o Azure PowerShell instalado no sistema que hospeda o Docker, você poderá ter credenciais do Azure em cache. Essas credenciais podem ser usadas na sessão do PowerShell em execução no contêiner do Docker.

Por padrão, as credenciais armazenadas em cache ficam no diretório `$HOME/.Azure` no host. O serviço do Docker deve ter acesso a esse local para acessar as credenciais. O comando a seguir inicia o contêiner com o cache de credenciais montado e inicia uma sessão interativa do PowerShell.

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a>Remover a imagem quando não for mais necessária

O comando a seguir é usado para excluir o contêiner do Docker quando você não precisar mais dele.

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a>Próximas etapas

Para saber mais sobre os módulos do Azure PowerShell e seus recursos, confira [Introdução ao Azure PowerShell](get-started-azureps.md).

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
