---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 57fe2159ab53e1a822da376a07546202ac672cb2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948023"
---
# <span data-ttu-id="5fd1a-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="5fd1a-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="5fd1a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5fd1a-102">SYNOPSIS</span></span>
<span data-ttu-id="5fd1a-103">Exporta um log de uma instância do servidor do Analysis Services no ambiente atualmente conectado, conforme especificado no comando Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="5fd1a-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="5fd1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5fd1a-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fd1a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5fd1a-105">DESCRIPTION</span></span>
<span data-ttu-id="5fd1a-106">O cmdlet Export-AzAnalysisServicesInstance exporta o log de uma instância do servidor do Azure Analysis Services para o arquivo</span><span class="sxs-lookup"><span data-stu-id="5fd1a-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="5fd1a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5fd1a-107">EXAMPLES</span></span>

### <span data-ttu-id="5fd1a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5fd1a-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="5fd1a-109">Esse comando irá exportar o log do servidor ' TestServer ' no ambiente especificado no comando Add-AzAnalysisServicesAccount e salvá-lo no arquivo especificado no OutputPath ' C:\path\to\log\testserver.log '</span><span class="sxs-lookup"><span data-stu-id="5fd1a-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="5fd1a-110">OS</span><span class="sxs-lookup"><span data-stu-id="5fd1a-110">PARAMETERS</span></span>

### <span data-ttu-id="5fd1a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="5fd1a-111">-Force</span></span>
<span data-ttu-id="5fd1a-112">Substituir arquivo se existir sem perguntar</span><span class="sxs-lookup"><span data-stu-id="5fd1a-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="5fd1a-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="5fd1a-113">-Instance</span></span>
<span data-ttu-id="5fd1a-114">Nome da instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="5fd1a-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="5fd1a-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="5fd1a-115">-OutputPath</span></span>
<span data-ttu-id="5fd1a-116">Caminho de saída do log de arquivo para exportação</span><span class="sxs-lookup"><span data-stu-id="5fd1a-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="5fd1a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5fd1a-117">-PassThru</span></span>
<span data-ttu-id="5fd1a-118">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="5fd1a-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5fd1a-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5fd1a-119">-Confirm</span></span>
<span data-ttu-id="5fd1a-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fd1a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fd1a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fd1a-121">-WhatIf</span></span>
<span data-ttu-id="5fd1a-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5fd1a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5fd1a-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5fd1a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fd1a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fd1a-124">CommonParameters</span></span>
<span data-ttu-id="5fd1a-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fd1a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fd1a-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fd1a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fd1a-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5fd1a-127">INPUTS</span></span>

### <span data-ttu-id="5fd1a-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5fd1a-128">None</span></span>

## <span data-ttu-id="5fd1a-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5fd1a-129">OUTPUTS</span></span>

### <span data-ttu-id="5fd1a-130">System. void</span><span class="sxs-lookup"><span data-stu-id="5fd1a-130">System.Void</span></span>

## <span data-ttu-id="5fd1a-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5fd1a-131">NOTES</span></span>
<span data-ttu-id="5fd1a-132">Alias: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="5fd1a-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="5fd1a-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5fd1a-133">RELATED LINKS</span></span>
