---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 3e4e3b2c2f90420f198d2900d5de0d519ffde81a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901519"
---
# <span data-ttu-id="9690c-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="9690c-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="9690c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9690c-102">SYNOPSIS</span></span>
<span data-ttu-id="9690c-103">Exporta um log de uma instância do servidor do Analysis Services no ambiente conectado no momento, conforme especificado no Add-AzAnalysisServicesAccount comando</span><span class="sxs-lookup"><span data-stu-id="9690c-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="9690c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9690c-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9690c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9690c-105">DESCRIPTION</span></span>
<span data-ttu-id="9690c-106">O Export-AzAnalysisServicesInstance de cmdlet exporta log de uma instância do servidor do Azure Analysis Services para o arquivo</span><span class="sxs-lookup"><span data-stu-id="9690c-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="9690c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9690c-107">EXAMPLES</span></span>

### <span data-ttu-id="9690c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9690c-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="9690c-109">Este comando exportará o log do servidor 'testserver' no ambiente especificado no comando Add-AzAnalysisServicesAccount e o salvará no arquivo especificado em OutputPath 'C:\path\to\log\testserver.log'</span><span class="sxs-lookup"><span data-stu-id="9690c-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="9690c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9690c-110">PARAMETERS</span></span>

### <span data-ttu-id="9690c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="9690c-111">-Force</span></span>
<span data-ttu-id="9690c-112">Substituir arquivo se existir sem perguntar</span><span class="sxs-lookup"><span data-stu-id="9690c-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="9690c-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="9690c-113">-Instance</span></span>
<span data-ttu-id="9690c-114">Nome da instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="9690c-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="9690c-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="9690c-115">-OutputPath</span></span>
<span data-ttu-id="9690c-116">Caminho de saída para o arquivo para exportar log</span><span class="sxs-lookup"><span data-stu-id="9690c-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="9690c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9690c-117">-PassThru</span></span>
<span data-ttu-id="9690c-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9690c-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9690c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9690c-119">-Confirm</span></span>
<span data-ttu-id="9690c-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9690c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9690c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9690c-121">-WhatIf</span></span>
<span data-ttu-id="9690c-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9690c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9690c-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9690c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9690c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9690c-124">CommonParameters</span></span>
<span data-ttu-id="9690c-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9690c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9690c-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9690c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9690c-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9690c-127">INPUTS</span></span>

### <span data-ttu-id="9690c-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9690c-128">None</span></span>

## <span data-ttu-id="9690c-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9690c-129">OUTPUTS</span></span>

### <span data-ttu-id="9690c-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="9690c-130">System.Void</span></span>

## <span data-ttu-id="9690c-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="9690c-131">NOTES</span></span>
<span data-ttu-id="9690c-132">Alias: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="9690c-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="9690c-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9690c-133">RELATED LINKS</span></span>
