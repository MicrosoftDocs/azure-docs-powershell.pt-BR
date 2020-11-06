---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: 5354737602f168245d6c4c8dca560698fa6cfac2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611013"
---
# <span data-ttu-id="e9602-101">Export-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="e9602-101">Export-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="e9602-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9602-102">SYNOPSIS</span></span>
<span data-ttu-id="e9602-103">Exporta um log de uma instância do servidor do Analysis Services no ambiente atualmente conectado, conforme especificado no comando Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e9602-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9602-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9602-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog [-Instance] <String> [-OutputPath] <String> [-WhatIf] [-Force]
```

## <span data-ttu-id="e9602-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e9602-105">DESCRIPTION</span></span>
<span data-ttu-id="e9602-106">O cmdlet Export-AzureAnalysisServicesInstance exporta o log de uma instância do servidor do Azure Analysis Services para o arquivo</span><span class="sxs-lookup"><span data-stu-id="e9602-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="e9602-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9602-107">EXAMPLES</span></span>

### <span data-ttu-id="e9602-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e9602-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="e9602-109">Esse comando irá exportar o log do servidor ' TestServer ' no ambiente especificado no comando Add-AzureAnalysisServicesAccount e salvá-lo no arquivo especificado no OutputPath ' C:\path\to\log\testserver.log '</span><span class="sxs-lookup"><span data-stu-id="e9602-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="e9602-110">OS</span><span class="sxs-lookup"><span data-stu-id="e9602-110">PARAMETERS</span></span>

### <span data-ttu-id="e9602-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="e9602-111">-Instance</span></span>
<span data-ttu-id="e9602-112">Nome da instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="e9602-112">Name of the Analysis Services server instance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9602-113">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="e9602-113">-OutputPath</span></span>
<span data-ttu-id="e9602-114">Caminho de saída do log de arquivo para exportação</span><span class="sxs-lookup"><span data-stu-id="e9602-114">Output path to file to export log</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9602-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e9602-115">-Force</span></span>
<span data-ttu-id="e9602-116">Substituir arquivo se existir sem perguntar</span><span class="sxs-lookup"><span data-stu-id="e9602-116">Overwrite file if exists without asking</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="e9602-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e9602-117">INPUTS</span></span>

## <span data-ttu-id="e9602-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e9602-118">OUTPUTS</span></span>

## <span data-ttu-id="e9602-119">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e9602-119">NOTES</span></span>
<span data-ttu-id="e9602-120">Alias: Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="e9602-120">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="e9602-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9602-121">RELATED LINKS</span></span>

