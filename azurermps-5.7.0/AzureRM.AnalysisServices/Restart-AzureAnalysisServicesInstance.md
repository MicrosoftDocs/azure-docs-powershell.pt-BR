---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/restart-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 0a89ee592e6f6f6d4d9e56df6d7e4df32b010524
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430546"
---
# <span data-ttu-id="26409-101">Restart-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="26409-101">Restart-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="26409-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26409-102">SYNOPSIS</span></span>
<span data-ttu-id="26409-103">Reinicia uma instância do servidor do Analysis Services no ambiente atualmente conectado, conforme especificado no comando Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="26409-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26409-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26409-104">SYNTAX</span></span>

```
Restart-AzureAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="26409-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="26409-105">DESCRIPTION</span></span>
<span data-ttu-id="26409-106">O cmdlet Restart-AzureAnalysisServicesInstance reinicia uma instância do servidor do Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="26409-106">The Restart-AzureAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="26409-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26409-107">EXAMPLES</span></span>

### <span data-ttu-id="26409-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="26409-108">Example 1</span></span>
```
PS C:\>Restart-AzureAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="26409-109">Esse comando irá reiniciar o servidor ' TestServer ' no ambiente especificado no comando Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="26409-109">This command will restart the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="26409-110">OS</span><span class="sxs-lookup"><span data-stu-id="26409-110">PARAMETERS</span></span>

### <span data-ttu-id="26409-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="26409-111">-Instance</span></span>
<span data-ttu-id="26409-112">Nome da instância do servidor do Analysis Services para reiniciar</span><span class="sxs-lookup"><span data-stu-id="26409-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="26409-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26409-113">-PassThru</span></span>
<span data-ttu-id="26409-114">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="26409-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="26409-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="26409-115">-Confirm</span></span>
<span data-ttu-id="26409-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26409-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26409-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26409-117">-WhatIf</span></span>
<span data-ttu-id="26409-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="26409-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26409-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="26409-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="26409-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="26409-120">INPUTS</span></span>

### <span data-ttu-id="26409-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="26409-121">None</span></span>
<span data-ttu-id="26409-122">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="26409-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="26409-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="26409-123">OUTPUTS</span></span>

### <span data-ttu-id="26409-124">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26409-124">System.Boolean</span></span>

## <span data-ttu-id="26409-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="26409-125">NOTES</span></span>
<span data-ttu-id="26409-126">Alias: Restart-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="26409-126">Alias: Restart-AzureAsInstance</span></span>

## <span data-ttu-id="26409-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26409-127">RELATED LINKS</span></span>

