---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 647d626a0b4d59f219020d66c3c1ec8a5218355b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263176"
---
# <span data-ttu-id="87abd-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="87abd-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="87abd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87abd-102">SYNOPSIS</span></span>
<span data-ttu-id="87abd-103">Exportar a definição Blueprint especificada para o local de saída especificado como um arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="87abd-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="87abd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87abd-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87abd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="87abd-105">DESCRIPTION</span></span>
<span data-ttu-id="87abd-106">Exporte uma definição Blueprint com seus artefatos e salve em disco.</span><span class="sxs-lookup"><span data-stu-id="87abd-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="87abd-107">Esse cmdlet exporta a versão mais recente (rascunho ou publicado) da planta.</span><span class="sxs-lookup"><span data-stu-id="87abd-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="87abd-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87abd-108">EXAMPLES</span></span>

### <span data-ttu-id="87abd-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="87abd-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="87abd-110">Exporte uma definição Blueprint com seus artefatos e salve em disco.</span><span class="sxs-lookup"><span data-stu-id="87abd-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="87abd-111">OS</span><span class="sxs-lookup"><span data-stu-id="87abd-111">PARAMETERS</span></span>

### <span data-ttu-id="87abd-112">-Plano gráfico</span><span class="sxs-lookup"><span data-stu-id="87abd-112">-Blueprint</span></span>
<span data-ttu-id="87abd-113">O objeto de definição Blueprint a ser exportado.</span><span class="sxs-lookup"><span data-stu-id="87abd-113">The blueprint definition object to export.</span></span>

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

### <span data-ttu-id="87abd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87abd-114">-DefaultProfile</span></span>
<span data-ttu-id="87abd-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="87abd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87abd-116">-Force</span><span class="sxs-lookup"><span data-stu-id="87abd-116">-Force</span></span>
<span data-ttu-id="87abd-117">Quando definida como true, a execução não solicitará uma confirmação.</span><span class="sxs-lookup"><span data-stu-id="87abd-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="87abd-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="87abd-118">-OutputPath</span></span>
<span data-ttu-id="87abd-119">Caminho para um arquivo no disco onde exportar a definição Blueprint no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="87abd-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="87abd-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87abd-120">-PassThru</span></span>
<span data-ttu-id="87abd-121">Quando definido, o cmdlet retornará um objeto que representa a definição Blueprint exportada.</span><span class="sxs-lookup"><span data-stu-id="87abd-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="87abd-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="87abd-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="87abd-123">-Versão</span><span class="sxs-lookup"><span data-stu-id="87abd-123">-Version</span></span>
<span data-ttu-id="87abd-124">Versão de definição de esquema publicada.</span><span class="sxs-lookup"><span data-stu-id="87abd-124">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="87abd-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="87abd-125">-Confirm</span></span>
<span data-ttu-id="87abd-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87abd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87abd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87abd-127">-WhatIf</span></span>
<span data-ttu-id="87abd-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="87abd-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87abd-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="87abd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87abd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87abd-130">CommonParameters</span></span>
<span data-ttu-id="87abd-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87abd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87abd-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87abd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87abd-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="87abd-133">INPUTS</span></span>

### <span data-ttu-id="87abd-134">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="87abd-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="87abd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="87abd-135">System.String</span></span>

## <span data-ttu-id="87abd-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="87abd-136">OUTPUTS</span></span>

### <span data-ttu-id="87abd-137">System. String</span><span class="sxs-lookup"><span data-stu-id="87abd-137">System.String</span></span>

## <span data-ttu-id="87abd-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="87abd-138">NOTES</span></span>

## <span data-ttu-id="87abd-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87abd-139">RELATED LINKS</span></span>
