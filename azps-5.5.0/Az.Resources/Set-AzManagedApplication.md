---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
ms.openlocfilehash: 3d8445c78ae2f11fef734db0b24319b524f55704
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113299"
---
# <span data-ttu-id="e0b00-101">Set-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="e0b00-101">Set-AzManagedApplication</span></span>

## <span data-ttu-id="e0b00-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0b00-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b00-103">Atualiza o aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="e0b00-103">Updates managed application</span></span>

## <span data-ttu-id="e0b00-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0b00-104">SYNTAX</span></span>

### <span data-ttu-id="e0b00-105">SetByNameAndResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e0b00-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0b00-106">SetById</span><span class="sxs-lookup"><span data-stu-id="e0b00-106">SetById</span></span>
```
Set-AzManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0b00-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0b00-107">DESCRIPTION</span></span>
<span data-ttu-id="e0b00-108">O **cmdlet Set-AzManagedApplication** atualiza aplicativos gerenciados</span><span class="sxs-lookup"><span data-stu-id="e0b00-108">The **Set-AzManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="e0b00-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e0b00-109">EXAMPLES</span></span>

### <span data-ttu-id="e0b00-110">Exemplo 1: atualizar a descrição da definição de aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="e0b00-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="e0b00-111">Este comando atualiza a descrição do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="e0b00-111">This command updates the managed application description</span></span>

## <span data-ttu-id="e0b00-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0b00-112">PARAMETERS</span></span>

### <span data-ttu-id="e0b00-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e0b00-113">-ApiVersion</span></span>
<span data-ttu-id="e0b00-114">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="e0b00-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e0b00-115">Se não especificado, a versão da API será determinada automaticamente como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="e0b00-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e0b00-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b00-116">-DefaultProfile</span></span>
<span data-ttu-id="e0b00-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e0b00-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0b00-118">-ID</span><span class="sxs-lookup"><span data-stu-id="e0b00-118">-Id</span></span>
<span data-ttu-id="e0b00-119">A ID de aplicativo gerenciado totalmente qualificada, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="e0b00-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="e0b00-120">por exemplo, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0b00-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0b00-121">-Tipo</span><span class="sxs-lookup"><span data-stu-id="e0b00-121">-Kind</span></span>
<span data-ttu-id="e0b00-122">O tipo de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e0b00-122">The managed application kind.</span></span>
<span data-ttu-id="e0b00-123">Um dos marketplaces ou servicecatalog</span><span class="sxs-lookup"><span data-stu-id="e0b00-123">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="e0b00-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="e0b00-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="e0b00-125">O nome do grupo de recursos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="e0b00-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="e0b00-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0b00-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="e0b00-127">O nome do grupo de recursos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="e0b00-127">The managed resource group name.</span></span>

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

### <span data-ttu-id="e0b00-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0b00-128">-Name</span></span>
<span data-ttu-id="e0b00-129">O nome do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e0b00-129">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0b00-130">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0b00-130">-Parameter</span></span>
<span data-ttu-id="e0b00-131">A cadeia de caracteres formatada JSON de parâmetros para aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e0b00-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="e0b00-132">Isso pode ser um caminho para um nome de arquivo ou uri contendo os parâmetros ou os parâmetros como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e0b00-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="e0b00-133">-Plano</span><span class="sxs-lookup"><span data-stu-id="e0b00-133">-Plan</span></span>
<span data-ttu-id="e0b00-134">Uma tabela hash que representa propriedades de plano de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e0b00-134">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="e0b00-135">-Pré-</span><span class="sxs-lookup"><span data-stu-id="e0b00-135">-Pre</span></span>
<span data-ttu-id="e0b00-136">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="e0b00-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e0b00-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0b00-137">-ResourceGroupName</span></span>
<span data-ttu-id="e0b00-138">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0b00-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0b00-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="e0b00-139">-Tag</span></span>
<span data-ttu-id="e0b00-140">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="e0b00-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="e0b00-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e0b00-141">-Confirm</span></span>
<span data-ttu-id="e0b00-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0b00-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0b00-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0b00-143">-WhatIf</span></span>
<span data-ttu-id="e0b00-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e0b00-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0b00-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0b00-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0b00-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b00-146">CommonParameters</span></span>
<span data-ttu-id="e0b00-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0b00-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b00-148">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0b00-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b00-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="e0b00-149">INPUTS</span></span>

### <span data-ttu-id="e0b00-150">System.String</span><span class="sxs-lookup"><span data-stu-id="e0b00-150">System.String</span></span>

### <span data-ttu-id="e0b00-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e0b00-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e0b00-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="e0b00-152">OUTPUTS</span></span>

### <span data-ttu-id="e0b00-153">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="e0b00-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e0b00-154">Notas</span><span class="sxs-lookup"><span data-stu-id="e0b00-154">NOTES</span></span>

## <span data-ttu-id="e0b00-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0b00-155">RELATED LINKS</span></span>
