---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/export-azureanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: dad0e14b72c256706456ed3c923b966323fd7dad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428669"
---
# <span data-ttu-id="2842d-101">Export-AzureAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="2842d-101">Export-AzureAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="2842d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2842d-102">SYNOPSIS</span></span>
<span data-ttu-id="2842d-103">Exporta um log de uma instância do servidor do Analysis Services no ambiente atualmente conectado, conforme especificado no comando Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2842d-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2842d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2842d-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog -Instance <String> -OutputPath <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2842d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2842d-105">DESCRIPTION</span></span>
<span data-ttu-id="2842d-106">O cmdlet Export-AzureAnalysisServicesInstance exporta o log de uma instância do servidor do Azure Analysis Services para o arquivo</span><span class="sxs-lookup"><span data-stu-id="2842d-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="2842d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2842d-107">EXAMPLES</span></span>

### <span data-ttu-id="2842d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2842d-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="2842d-109">Esse comando irá exportar o log do servidor ' TestServer ' no ambiente especificado no comando Add-AzureAnalysisServicesAccount e salvá-lo no arquivo especificado no OutputPath ' C:\path\to\log\testserver.log '</span><span class="sxs-lookup"><span data-stu-id="2842d-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="2842d-110">OS</span><span class="sxs-lookup"><span data-stu-id="2842d-110">PARAMETERS</span></span>

### <span data-ttu-id="2842d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2842d-111">-Force</span></span>
<span data-ttu-id="2842d-112">Substituir arquivo se existir sem perguntar</span><span class="sxs-lookup"><span data-stu-id="2842d-112">Overwrite file if exists without asking</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2842d-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="2842d-113">-Instance</span></span>
<span data-ttu-id="2842d-114">Nome da instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2842d-114">Name of the Analysis Services server instance</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2842d-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="2842d-115">-OutputPath</span></span>
<span data-ttu-id="2842d-116">Caminho de saída do log de arquivo para exportação</span><span class="sxs-lookup"><span data-stu-id="2842d-116">Output path to file to export log</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2842d-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2842d-117">-Confirm</span></span>
<span data-ttu-id="2842d-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2842d-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2842d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2842d-119">-WhatIf</span></span>
<span data-ttu-id="2842d-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2842d-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2842d-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2842d-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2842d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2842d-122">CommonParameters</span></span>
<span data-ttu-id="2842d-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2842d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2842d-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2842d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2842d-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2842d-125">INPUTS</span></span>

### <span data-ttu-id="2842d-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2842d-126">None</span></span>

## <span data-ttu-id="2842d-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2842d-127">OUTPUTS</span></span>

### <span data-ttu-id="2842d-128">System. void</span><span class="sxs-lookup"><span data-stu-id="2842d-128">System.Void</span></span>

## <span data-ttu-id="2842d-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2842d-129">NOTES</span></span>
<span data-ttu-id="2842d-130">Alias: Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="2842d-130">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="2842d-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2842d-131">RELATED LINKS</span></span>
