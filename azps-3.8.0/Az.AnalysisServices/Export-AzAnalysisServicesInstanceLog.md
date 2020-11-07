---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 57fe2159ab53e1a822da376a07546202ac672cb2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941185"
---
# <span data-ttu-id="565d3-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="565d3-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="565d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="565d3-102">SYNOPSIS</span></span>
<span data-ttu-id="565d3-103">Exporta um log de uma instância do servidor do Analysis Services no ambiente atualmente conectado, conforme especificado no comando Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="565d3-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="565d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="565d3-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="565d3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="565d3-105">DESCRIPTION</span></span>
<span data-ttu-id="565d3-106">O cmdlet Export-AzAnalysisServicesInstance exporta o log de uma instância do servidor do Azure Analysis Services para o arquivo</span><span class="sxs-lookup"><span data-stu-id="565d3-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="565d3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="565d3-107">EXAMPLES</span></span>

### <span data-ttu-id="565d3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="565d3-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="565d3-109">Esse comando irá exportar o log do servidor ' TestServer ' no ambiente especificado no comando Add-AzAnalysisServicesAccount e salvá-lo no arquivo especificado no OutputPath ' C:\path\to\log\testserver.log '</span><span class="sxs-lookup"><span data-stu-id="565d3-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="565d3-110">OS</span><span class="sxs-lookup"><span data-stu-id="565d3-110">PARAMETERS</span></span>

### <span data-ttu-id="565d3-111">-Force</span><span class="sxs-lookup"><span data-stu-id="565d3-111">-Force</span></span>
<span data-ttu-id="565d3-112">Substituir arquivo se existir sem perguntar</span><span class="sxs-lookup"><span data-stu-id="565d3-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="565d3-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="565d3-113">-Instance</span></span>
<span data-ttu-id="565d3-114">Nome da instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="565d3-114">Name of the Analysis Services server instance</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="565d3-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="565d3-115">-OutputPath</span></span>
<span data-ttu-id="565d3-116">Caminho de saída do log de arquivo para exportação</span><span class="sxs-lookup"><span data-stu-id="565d3-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="565d3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="565d3-117">-PassThru</span></span>
<span data-ttu-id="565d3-118">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="565d3-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="565d3-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="565d3-119">-Confirm</span></span>
<span data-ttu-id="565d3-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="565d3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="565d3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="565d3-121">-WhatIf</span></span>
<span data-ttu-id="565d3-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="565d3-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="565d3-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="565d3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="565d3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="565d3-124">CommonParameters</span></span>
<span data-ttu-id="565d3-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="565d3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="565d3-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="565d3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="565d3-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="565d3-127">INPUTS</span></span>

### <span data-ttu-id="565d3-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="565d3-128">None</span></span>

## <span data-ttu-id="565d3-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="565d3-129">OUTPUTS</span></span>

### <span data-ttu-id="565d3-130">System. void</span><span class="sxs-lookup"><span data-stu-id="565d3-130">System.Void</span></span>

## <span data-ttu-id="565d3-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="565d3-131">NOTES</span></span>
<span data-ttu-id="565d3-132">Alias: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="565d3-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="565d3-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="565d3-133">RELATED LINKS</span></span>
