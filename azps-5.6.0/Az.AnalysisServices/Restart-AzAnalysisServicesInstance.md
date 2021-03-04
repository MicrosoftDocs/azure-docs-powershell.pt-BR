---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: b0bb5d90fe304d2663671fdc8a2277d2adb18322
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888381"
---
# <span data-ttu-id="f85cf-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="f85cf-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="f85cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f85cf-102">SYNOPSIS</span></span>
<span data-ttu-id="f85cf-103">Reinicia uma instância do servidor do Analysis Services no ambiente conectado no momento, conforme especificado no Add-AzAnalysisServicesAccount comando</span><span class="sxs-lookup"><span data-stu-id="f85cf-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="f85cf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f85cf-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f85cf-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f85cf-105">DESCRIPTION</span></span>
<span data-ttu-id="f85cf-106">O Restart-AzAnalysisServicesInstance cmdlet reinicia uma instância do servidor do Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f85cf-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="f85cf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f85cf-107">EXAMPLES</span></span>

### <span data-ttu-id="f85cf-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f85cf-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="f85cf-109">Este comando reiniciará o servidor "testserver" no ambiente especificado no comando Add-AzAnalysisServicesAccount servidor</span><span class="sxs-lookup"><span data-stu-id="f85cf-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="f85cf-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f85cf-110">PARAMETERS</span></span>

### <span data-ttu-id="f85cf-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="f85cf-111">-Instance</span></span>
<span data-ttu-id="f85cf-112">Nome da instância do servidor do Analysis Services a ser reiniciada</span><span class="sxs-lookup"><span data-stu-id="f85cf-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="f85cf-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f85cf-113">-PassThru</span></span>
<span data-ttu-id="f85cf-114">Especificar isso retornará true se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f85cf-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f85cf-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f85cf-115">-Confirm</span></span>
<span data-ttu-id="f85cf-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f85cf-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f85cf-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f85cf-117">-WhatIf</span></span>
<span data-ttu-id="f85cf-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f85cf-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f85cf-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f85cf-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f85cf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f85cf-120">CommonParameters</span></span>
<span data-ttu-id="f85cf-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f85cf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f85cf-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f85cf-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f85cf-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f85cf-123">INPUTS</span></span>

### <span data-ttu-id="f85cf-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f85cf-124">None</span></span>

## <span data-ttu-id="f85cf-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f85cf-125">OUTPUTS</span></span>

### <span data-ttu-id="f85cf-126">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f85cf-126">System.Boolean</span></span>

## <span data-ttu-id="f85cf-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="f85cf-127">NOTES</span></span>
<span data-ttu-id="f85cf-128">Alias: Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="f85cf-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="f85cf-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f85cf-129">RELATED LINKS</span></span>
