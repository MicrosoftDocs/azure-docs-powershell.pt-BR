---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: 30e3e7f7b6ace383a2c492f4dcc088f65dfea08b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891630"
---
# <span data-ttu-id="566a1-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="566a1-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="566a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="566a1-102">SYNOPSIS</span></span>
<span data-ttu-id="566a1-103">Cria um aplicativo gerenciado do Azure.</span><span class="sxs-lookup"><span data-stu-id="566a1-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="566a1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="566a1-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="566a1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="566a1-105">DESCRIPTION</span></span>
<span data-ttu-id="566a1-106">O cmdlet **New-AzManagedApplication** cria um Aplicativo Gerenciado do Azure.</span><span class="sxs-lookup"><span data-stu-id="566a1-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="566a1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="566a1-107">EXAMPLES</span></span>

### <span data-ttu-id="566a1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="566a1-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="566a1-109">Este comando cria um aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="566a1-109">This command creates a managed application</span></span>

## <span data-ttu-id="566a1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="566a1-110">PARAMETERS</span></span>

### <span data-ttu-id="566a1-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="566a1-111">-ApiVersion</span></span>
<span data-ttu-id="566a1-112">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="566a1-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="566a1-113">Se não for especificada, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="566a1-113">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="566a1-114">-DefaultProfile</span></span>
<span data-ttu-id="566a1-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="566a1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="566a1-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="566a1-116">-Kind</span></span>
<span data-ttu-id="566a1-117">O tipo de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="566a1-117">The managed application kind.</span></span>
<span data-ttu-id="566a1-118">Um dos marketplaces ou servicecatalog</span><span class="sxs-lookup"><span data-stu-id="566a1-118">One of marketplace or servicecatalog</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationKind
Parameter Sets: (All)
Aliases:
Accepted values: ServiceCatalog, MarketPlace

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566a1-119">-Location</span><span class="sxs-lookup"><span data-stu-id="566a1-119">-Location</span></span>
<span data-ttu-id="566a1-120">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="566a1-120">The resource location.</span></span>

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

### <span data-ttu-id="566a1-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="566a1-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="566a1-122">O nome do grupo de recursos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="566a1-122">The managed resource group name.</span></span>

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

### <span data-ttu-id="566a1-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="566a1-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="566a1-124">O nome do grupo de recursos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="566a1-124">The managed resource group name.</span></span>

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

### <span data-ttu-id="566a1-125">-Name</span><span class="sxs-lookup"><span data-stu-id="566a1-125">-Name</span></span>
<span data-ttu-id="566a1-126">O nome do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="566a1-126">The managed application name.</span></span>

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

### <span data-ttu-id="566a1-127">-Parameter</span><span class="sxs-lookup"><span data-stu-id="566a1-127">-Parameter</span></span>
<span data-ttu-id="566a1-128">A cadeia de caracteres formatada JSON de parâmetros para aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="566a1-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="566a1-129">Isso pode ser um caminho para um nome de arquivo ou uri contendo os parâmetros ou os parâmetros como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="566a1-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="566a1-130">-Plan</span><span class="sxs-lookup"><span data-stu-id="566a1-130">-Plan</span></span>
<span data-ttu-id="566a1-131">Uma tabela de hash que representa propriedades de plano de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="566a1-131">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566a1-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="566a1-132">-Pre</span></span>
<span data-ttu-id="566a1-133">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="566a1-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="566a1-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="566a1-134">-ResourceGroupName</span></span>
<span data-ttu-id="566a1-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="566a1-135">The resource group name.</span></span>

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

### <span data-ttu-id="566a1-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="566a1-136">-Tag</span></span>
<span data-ttu-id="566a1-137">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="566a1-137">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="566a1-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="566a1-138">-Confirm</span></span>
<span data-ttu-id="566a1-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="566a1-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="566a1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="566a1-140">-WhatIf</span></span>
<span data-ttu-id="566a1-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="566a1-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="566a1-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="566a1-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="566a1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="566a1-143">CommonParameters</span></span>
<span data-ttu-id="566a1-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="566a1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="566a1-145">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="566a1-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="566a1-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="566a1-146">INPUTS</span></span>

### <span data-ttu-id="566a1-147">System.String</span><span class="sxs-lookup"><span data-stu-id="566a1-147">System.String</span></span>

### <span data-ttu-id="566a1-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="566a1-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="566a1-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="566a1-149">OUTPUTS</span></span>

### <span data-ttu-id="566a1-150">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="566a1-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="566a1-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="566a1-151">NOTES</span></span>

## <span data-ttu-id="566a1-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="566a1-152">RELATED LINKS</span></span>
