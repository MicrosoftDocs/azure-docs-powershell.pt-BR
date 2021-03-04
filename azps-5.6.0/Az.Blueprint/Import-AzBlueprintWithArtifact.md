---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: eb0fddc34a83d5a23aeb990c920f36d7a3e03ff2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888745"
---
# <span data-ttu-id="d3ec5-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="d3ec5-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="d3ec5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="d3ec5-103">Importe um arquivo de projeto no formato JSON para um objeto blueprint e salve-o dentro da assinatura ou grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="d3ec5-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="d3ec5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d3ec5-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-IncludeSubFolders] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3ec5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d3ec5-105">DESCRIPTION</span></span>
<span data-ttu-id="d3ec5-106">Importar uma definição de projeto com seus artefatos.</span><span class="sxs-lookup"><span data-stu-id="d3ec5-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="d3ec5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3ec5-107">EXAMPLES</span></span>

### <span data-ttu-id="d3ec5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d3ec5-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="d3ec5-109">Importe uma definição de projeto com seus artefatos e salve em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="d3ec5-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="d3ec5-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d3ec5-110">PARAMETERS</span></span>

### <span data-ttu-id="d3ec5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3ec5-111">-DefaultProfile</span></span>
<span data-ttu-id="d3ec5-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3ec5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3ec5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d3ec5-113">-Force</span></span>
<span data-ttu-id="d3ec5-114">Quando definido como true, a execução não solicitará uma confirmação.</span><span class="sxs-lookup"><span data-stu-id="d3ec5-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="d3ec5-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="d3ec5-115">-IncludeSubFolders</span></span>
<span data-ttu-id="d3ec5-116">Quando definido como true, o artefato nas subpastas será incluído.</span><span class="sxs-lookup"><span data-stu-id="d3ec5-116">When set to true, artifact in the subfolders will be included.</span></span>

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

### <span data-ttu-id="d3ec5-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="d3ec5-117">-InputPath</span></span>
<span data-ttu-id="d3ec5-118">Caminho para um arquivo JSON de esquema no disco.</span><span class="sxs-lookup"><span data-stu-id="d3ec5-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="d3ec5-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="d3ec5-119">-ManagementGroupId</span></span>
<span data-ttu-id="d3ec5-120">ID do Grupo de Gerenciamento onde a definição de projeto é ou será salva.</span><span class="sxs-lookup"><span data-stu-id="d3ec5-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="d3ec5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d3ec5-121">-Name</span></span>
<span data-ttu-id="d3ec5-122">Nome da definição de projeto.</span><span class="sxs-lookup"><span data-stu-id="d3ec5-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="d3ec5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3ec5-123">-PassThru</span></span>
<span data-ttu-id="d3ec5-124">Quando definido, o cmdlet retornará um objeto que representa a definição de projeto importada.</span><span class="sxs-lookup"><span data-stu-id="d3ec5-124">When set, the cmdlet will return an object representing the imported blueprint definition.</span></span> <span data-ttu-id="d3ec5-125">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="d3ec5-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d3ec5-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d3ec5-126">-SubscriptionId</span></span>
<span data-ttu-id="d3ec5-127">ID da assinatura onde a definição de projeto é ou será salva.</span><span class="sxs-lookup"><span data-stu-id="d3ec5-127">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="d3ec5-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3ec5-128">-Confirm</span></span>
<span data-ttu-id="d3ec5-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3ec5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3ec5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3ec5-130">-WhatIf</span></span>
<span data-ttu-id="d3ec5-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d3ec5-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3ec5-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d3ec5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3ec5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3ec5-133">CommonParameters</span></span>
<span data-ttu-id="d3ec5-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3ec5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3ec5-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3ec5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3ec5-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3ec5-136">INPUTS</span></span>

### <span data-ttu-id="d3ec5-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d3ec5-137">System.String</span></span>

## <span data-ttu-id="d3ec5-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d3ec5-138">OUTPUTS</span></span>

### <span data-ttu-id="d3ec5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d3ec5-139">System.String</span></span>

## <span data-ttu-id="d3ec5-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="d3ec5-140">NOTES</span></span>

## <span data-ttu-id="d3ec5-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3ec5-141">RELATED LINKS</span></span>
