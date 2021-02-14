---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 647d626a0b4d59f219020d66c3c1ec8a5218355b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111189"
---
# <span data-ttu-id="2f7d2-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="2f7d2-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="2f7d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f7d2-102">SYNOPSIS</span></span>
<span data-ttu-id="2f7d2-103">Exportar a definição de planta especificada para o local de saída especificado como um arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="2f7d2-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="2f7d2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f7d2-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f7d2-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f7d2-105">DESCRIPTION</span></span>
<span data-ttu-id="2f7d2-106">Exporte uma definição de planta com seus artefatos e salve em disco.</span><span class="sxs-lookup"><span data-stu-id="2f7d2-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="2f7d2-107">Este cmdlet exporta a versão(rascunho ou publicação) mais recente do diagrama.</span><span class="sxs-lookup"><span data-stu-id="2f7d2-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="2f7d2-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2f7d2-108">EXAMPLES</span></span>

### <span data-ttu-id="2f7d2-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2f7d2-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="2f7d2-110">Exporte uma definição de planta com seus artefatos e salve em disco.</span><span class="sxs-lookup"><span data-stu-id="2f7d2-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="2f7d2-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f7d2-111">PARAMETERS</span></span>

### <span data-ttu-id="2f7d2-112">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="2f7d2-112">-Blueprint</span></span>
<span data-ttu-id="2f7d2-113">O objeto de definição de planta a ser exportado.</span><span class="sxs-lookup"><span data-stu-id="2f7d2-113">The blueprint definition object to export.</span></span>

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

### <span data-ttu-id="2f7d2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f7d2-114">-DefaultProfile</span></span>
<span data-ttu-id="2f7d2-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f7d2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f7d2-116">-Forçar</span><span class="sxs-lookup"><span data-stu-id="2f7d2-116">-Force</span></span>
<span data-ttu-id="2f7d2-117">Quando definida como verdadeira, a execução não solicitará uma confirmação.</span><span class="sxs-lookup"><span data-stu-id="2f7d2-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="2f7d2-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="2f7d2-118">-OutputPath</span></span>
<span data-ttu-id="2f7d2-119">Caminho para um arquivo no disco onde exportar a definição de diagrama no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="2f7d2-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="2f7d2-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f7d2-120">-PassThru</span></span>
<span data-ttu-id="2f7d2-121">Quando definido, o cmdlet retornará um objeto que representa a definição de diagrama exportado.</span><span class="sxs-lookup"><span data-stu-id="2f7d2-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="2f7d2-122">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="2f7d2-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2f7d2-123">-Versão</span><span class="sxs-lookup"><span data-stu-id="2f7d2-123">-Version</span></span>
<span data-ttu-id="2f7d2-124">Versão de definição de planta publicada.</span><span class="sxs-lookup"><span data-stu-id="2f7d2-124">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="2f7d2-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2f7d2-125">-Confirm</span></span>
<span data-ttu-id="2f7d2-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f7d2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f7d2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f7d2-127">-WhatIf</span></span>
<span data-ttu-id="2f7d2-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2f7d2-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f7d2-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2f7d2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f7d2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f7d2-130">CommonParameters</span></span>
<span data-ttu-id="2f7d2-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f7d2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f7d2-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f7d2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f7d2-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="2f7d2-133">INPUTS</span></span>

### <span data-ttu-id="2f7d2-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="2f7d2-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="2f7d2-135">System.String</span><span class="sxs-lookup"><span data-stu-id="2f7d2-135">System.String</span></span>

## <span data-ttu-id="2f7d2-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="2f7d2-136">OUTPUTS</span></span>

### <span data-ttu-id="2f7d2-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2f7d2-137">System.String</span></span>

## <span data-ttu-id="2f7d2-138">Notas</span><span class="sxs-lookup"><span data-stu-id="2f7d2-138">NOTES</span></span>

## <span data-ttu-id="2f7d2-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f7d2-139">RELATED LINKS</span></span>
