---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 57fe2159ab53e1a822da376a07546202ac672cb2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116659"
---
# <span data-ttu-id="d0c66-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="d0c66-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="d0c66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0c66-102">SYNOPSIS</span></span>
<span data-ttu-id="d0c66-103">Exporta um log de uma instância do servidor do Analysis Services no Ambiente atualmente conectado, conforme especificado no Add-AzAnalysisServicesAccount comando</span><span class="sxs-lookup"><span data-stu-id="d0c66-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="d0c66-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0c66-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0c66-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0c66-105">DESCRIPTION</span></span>
<span data-ttu-id="d0c66-106">O Export-AzAnalysisServicesInstance cmdlet exporta log de uma instância do servidor do Azure Analysis Services para arquivo</span><span class="sxs-lookup"><span data-stu-id="d0c66-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="d0c66-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d0c66-107">EXAMPLES</span></span>

### <span data-ttu-id="d0c66-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d0c66-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="d0c66-109">Esse comando exportará o log do servidor "testserver" no ambiente especificado no comando Add-AzAnalysisServicesAccount e o salvará no arquivo especificado no OutputPath 'C:\path\to\log\testserver.log'</span><span class="sxs-lookup"><span data-stu-id="d0c66-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="d0c66-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0c66-110">PARAMETERS</span></span>

### <span data-ttu-id="d0c66-111">-Forçar</span><span class="sxs-lookup"><span data-stu-id="d0c66-111">-Force</span></span>
<span data-ttu-id="d0c66-112">Substituir arquivo se existir sem perguntar</span><span class="sxs-lookup"><span data-stu-id="d0c66-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="d0c66-113">-Instância</span><span class="sxs-lookup"><span data-stu-id="d0c66-113">-Instance</span></span>
<span data-ttu-id="d0c66-114">Nome da instância do servidor analysis services</span><span class="sxs-lookup"><span data-stu-id="d0c66-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="d0c66-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="d0c66-115">-OutputPath</span></span>
<span data-ttu-id="d0c66-116">Caminho de saída para o arquivo para exportar o log</span><span class="sxs-lookup"><span data-stu-id="d0c66-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="d0c66-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0c66-117">-PassThru</span></span>
<span data-ttu-id="d0c66-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d0c66-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d0c66-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d0c66-119">-Confirm</span></span>
<span data-ttu-id="d0c66-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0c66-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0c66-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0c66-121">-WhatIf</span></span>
<span data-ttu-id="d0c66-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d0c66-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0c66-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d0c66-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0c66-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0c66-124">CommonParameters</span></span>
<span data-ttu-id="d0c66-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0c66-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0c66-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0c66-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0c66-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="d0c66-127">INPUTS</span></span>

### <span data-ttu-id="d0c66-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d0c66-128">None</span></span>

## <span data-ttu-id="d0c66-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="d0c66-129">OUTPUTS</span></span>

### <span data-ttu-id="d0c66-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="d0c66-130">System.Void</span></span>

## <span data-ttu-id="d0c66-131">Notas</span><span class="sxs-lookup"><span data-stu-id="d0c66-131">NOTES</span></span>
<span data-ttu-id="d0c66-132">Alias: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="d0c66-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="d0c66-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0c66-133">RELATED LINKS</span></span>
