---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 1e4184b847b260d84d8b3609ade5403367046dd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901504"
---
# <span data-ttu-id="e00ed-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="e00ed-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="e00ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e00ed-102">SYNOPSIS</span></span>
<span data-ttu-id="e00ed-103">Exportar a definição de projeto especificada para o local de saída especificado como um arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="e00ed-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="e00ed-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e00ed-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e00ed-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e00ed-105">DESCRIPTION</span></span>
<span data-ttu-id="e00ed-106">Exporte uma definição de projeto com seus artefatos e salve em disco.</span><span class="sxs-lookup"><span data-stu-id="e00ed-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="e00ed-107">Este cmdlet exporta a versão mais recente(rascunho ou publicado) do projeto.</span><span class="sxs-lookup"><span data-stu-id="e00ed-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="e00ed-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e00ed-108">EXAMPLES</span></span>

### <span data-ttu-id="e00ed-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e00ed-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="e00ed-110">Exporte uma definição de projeto com seus artefatos e salve em disco.</span><span class="sxs-lookup"><span data-stu-id="e00ed-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="e00ed-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e00ed-111">PARAMETERS</span></span>

### <span data-ttu-id="e00ed-112">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="e00ed-112">-Blueprint</span></span>
<span data-ttu-id="e00ed-113">O objeto de definição de projeto a ser exportado.</span><span class="sxs-lookup"><span data-stu-id="e00ed-113">The blueprint definition object to export.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e00ed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e00ed-114">-DefaultProfile</span></span>
<span data-ttu-id="e00ed-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e00ed-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e00ed-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e00ed-116">-Force</span></span>
<span data-ttu-id="e00ed-117">Quando definido como true, a execução não solicitará uma confirmação.</span><span class="sxs-lookup"><span data-stu-id="e00ed-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="e00ed-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="e00ed-118">-OutputPath</span></span>
<span data-ttu-id="e00ed-119">Caminho para um arquivo no disco onde exportar a definição de blueprint no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="e00ed-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e00ed-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e00ed-120">-PassThru</span></span>
<span data-ttu-id="e00ed-121">Quando definido, o cmdlet retornará um objeto que representa a definição de projeto exportada.</span><span class="sxs-lookup"><span data-stu-id="e00ed-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="e00ed-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e00ed-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e00ed-123">-Version</span><span class="sxs-lookup"><span data-stu-id="e00ed-123">-Version</span></span>
<span data-ttu-id="e00ed-124">Versão de definição de projeto publicada.</span><span class="sxs-lookup"><span data-stu-id="e00ed-124">Published blueprint definition version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e00ed-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e00ed-125">-Confirm</span></span>
<span data-ttu-id="e00ed-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e00ed-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e00ed-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e00ed-127">-WhatIf</span></span>
<span data-ttu-id="e00ed-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e00ed-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e00ed-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e00ed-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e00ed-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e00ed-130">CommonParameters</span></span>
<span data-ttu-id="e00ed-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e00ed-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e00ed-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e00ed-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e00ed-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e00ed-133">INPUTS</span></span>

### <span data-ttu-id="e00ed-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="e00ed-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="e00ed-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e00ed-135">System.String</span></span>

## <span data-ttu-id="e00ed-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e00ed-136">OUTPUTS</span></span>

### <span data-ttu-id="e00ed-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e00ed-137">System.String</span></span>

## <span data-ttu-id="e00ed-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="e00ed-138">NOTES</span></span>

## <span data-ttu-id="e00ed-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e00ed-139">RELATED LINKS</span></span>
