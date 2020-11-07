---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
ms.openlocfilehash: 83a0e39d5b21aad0d23e4513793b5b9ed00fa0d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773308"
---
# <span data-ttu-id="98db5-101">Set-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="98db5-101">Set-AzManagedApplication</span></span>

## <span data-ttu-id="98db5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98db5-102">SYNOPSIS</span></span>
<span data-ttu-id="98db5-103">Atualiza o aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="98db5-103">Updates managed application</span></span>

## <span data-ttu-id="98db5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98db5-104">SYNTAX</span></span>

### <span data-ttu-id="98db5-105">SetByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="98db5-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98db5-106">SetById</span><span class="sxs-lookup"><span data-stu-id="98db5-106">SetById</span></span>
```
Set-AzManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98db5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98db5-107">DESCRIPTION</span></span>
<span data-ttu-id="98db5-108">O cmdlet **set-AzManagedApplication** atualiza os aplicativos gerenciados</span><span class="sxs-lookup"><span data-stu-id="98db5-108">The **Set-AzManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="98db5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98db5-109">EXAMPLES</span></span>

### <span data-ttu-id="98db5-110">Exemplo 1: atualizar descrição da definição do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="98db5-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="98db5-111">Este comando atualiza a descrição do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="98db5-111">This command updates the managed application description</span></span>

## <span data-ttu-id="98db5-112">OS</span><span class="sxs-lookup"><span data-stu-id="98db5-112">PARAMETERS</span></span>

### <span data-ttu-id="98db5-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="98db5-113">-ApiVersion</span></span>
<span data-ttu-id="98db5-114">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="98db5-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="98db5-115">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="98db5-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="98db5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98db5-116">-DefaultProfile</span></span>
<span data-ttu-id="98db5-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98db5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98db5-118">-ID</span><span class="sxs-lookup"><span data-stu-id="98db5-118">-Id</span></span>
<span data-ttu-id="98db5-119">A ID de aplicativo gerenciada totalmente qualificada, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="98db5-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="98db5-120">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98db5-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="98db5-121">-Kind</span><span class="sxs-lookup"><span data-stu-id="98db5-121">-Kind</span></span>
<span data-ttu-id="98db5-122">O tipo de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="98db5-122">The managed application kind.</span></span>
<span data-ttu-id="98db5-123">Um dos Marketplaces ou catálogos</span><span class="sxs-lookup"><span data-stu-id="98db5-123">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="98db5-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="98db5-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="98db5-125">O nome do grupo de recursos gerenciado.</span><span class="sxs-lookup"><span data-stu-id="98db5-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="98db5-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98db5-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="98db5-127">O nome do grupo de recursos gerenciado.</span><span class="sxs-lookup"><span data-stu-id="98db5-127">The managed resource group name.</span></span>

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

### <span data-ttu-id="98db5-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="98db5-128">-Name</span></span>
<span data-ttu-id="98db5-129">O nome do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="98db5-129">The managed application name.</span></span>

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

### <span data-ttu-id="98db5-130">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="98db5-130">-Parameter</span></span>
<span data-ttu-id="98db5-131">A cadeia de caracteres de parâmetros da JSON formatada para o aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="98db5-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="98db5-132">Isso pode ser um caminho para um nome de arquivo ou URI que contém os parâmetros ou os parâmetros como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="98db5-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="98db5-133">-Plano</span><span class="sxs-lookup"><span data-stu-id="98db5-133">-Plan</span></span>
<span data-ttu-id="98db5-134">Uma tabela de hash que representa as propriedades do plano de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="98db5-134">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="98db5-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="98db5-135">-Pre</span></span>
<span data-ttu-id="98db5-136">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="98db5-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="98db5-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98db5-137">-ResourceGroupName</span></span>
<span data-ttu-id="98db5-138">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="98db5-138">The resource group name.</span></span>

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

### <span data-ttu-id="98db5-139">-Marca</span><span class="sxs-lookup"><span data-stu-id="98db5-139">-Tag</span></span>
<span data-ttu-id="98db5-140">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="98db5-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="98db5-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="98db5-141">-Confirm</span></span>
<span data-ttu-id="98db5-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98db5-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98db5-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98db5-143">-WhatIf</span></span>
<span data-ttu-id="98db5-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="98db5-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98db5-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="98db5-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98db5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98db5-146">CommonParameters</span></span>
<span data-ttu-id="98db5-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98db5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98db5-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98db5-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98db5-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98db5-149">INPUTS</span></span>

### <span data-ttu-id="98db5-150">System. String</span><span class="sxs-lookup"><span data-stu-id="98db5-150">System.String</span></span>

### <span data-ttu-id="98db5-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="98db5-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="98db5-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98db5-152">OUTPUTS</span></span>

### <span data-ttu-id="98db5-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="98db5-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="98db5-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98db5-154">NOTES</span></span>

## <span data-ttu-id="98db5-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98db5-155">RELATED LINKS</span></span>