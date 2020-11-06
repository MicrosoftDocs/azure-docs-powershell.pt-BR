---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
ms.openlocfilehash: 2a242f7a265efa2dd97f967101074615381d4cd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429120"
---
# <span data-ttu-id="09eb2-101">Set-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="09eb2-101">Set-AzureRmManagedApplication</span></span>

## <span data-ttu-id="09eb2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09eb2-102">SYNOPSIS</span></span>
<span data-ttu-id="09eb2-103">Atualiza o aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="09eb2-103">Updates managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09eb2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09eb2-104">SYNTAX</span></span>

### <span data-ttu-id="09eb2-105">O conjunto de parâmetros de nome do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="09eb2-105">The managed application name parameter set.</span></span> <span data-ttu-id="09eb2-106">Assume</span><span class="sxs-lookup"><span data-stu-id="09eb2-106">(Default)</span></span>
```
Set-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09eb2-107">O conjunto de parâmetros de ID do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="09eb2-107">The managed application Id parameter set.</span></span>
```
Set-AzureRmManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09eb2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09eb2-108">DESCRIPTION</span></span>
<span data-ttu-id="09eb2-109">O cmdlet **set-AzureRmManagedApplication** atualiza os aplicativos gerenciados</span><span class="sxs-lookup"><span data-stu-id="09eb2-109">The **Set-AzureRmManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="09eb2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09eb2-110">EXAMPLES</span></span>

### <span data-ttu-id="09eb2-111">Exemplo 1: atualizar descrição da definição do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="09eb2-111">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="09eb2-112">Este comando atualiza a descrição do aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="09eb2-112">This command updates the managed application description</span></span>

## <span data-ttu-id="09eb2-113">OS</span><span class="sxs-lookup"><span data-stu-id="09eb2-113">PARAMETERS</span></span>

### <span data-ttu-id="09eb2-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="09eb2-114">-ApiVersion</span></span>
<span data-ttu-id="09eb2-115">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="09eb2-115">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="09eb2-116">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="09eb2-116">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="09eb2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09eb2-117">-DefaultProfile</span></span>
<span data-ttu-id="09eb2-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09eb2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09eb2-119">-Kind</span><span class="sxs-lookup"><span data-stu-id="09eb2-119">-Kind</span></span>
<span data-ttu-id="09eb2-120">O tipo de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="09eb2-120">The managed application kind.</span></span>
<span data-ttu-id="09eb2-121">Um dos Marketplaces ou catálogos</span><span class="sxs-lookup"><span data-stu-id="09eb2-121">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="09eb2-122">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="09eb2-122">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="09eb2-123">O nome do grupo de recursos gerenciado.</span><span class="sxs-lookup"><span data-stu-id="09eb2-123">The managed resource group name.</span></span>

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

### <span data-ttu-id="09eb2-124">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09eb2-124">-ManagedResourceGroupName</span></span>
<span data-ttu-id="09eb2-125">O nome do grupo de recursos gerenciado.</span><span class="sxs-lookup"><span data-stu-id="09eb2-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="09eb2-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="09eb2-126">-Name</span></span>
<span data-ttu-id="09eb2-127">O nome do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="09eb2-127">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09eb2-128">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="09eb2-128">-Parameter</span></span>
<span data-ttu-id="09eb2-129">A cadeia de caracteres de parâmetros da JSON formatada para o aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="09eb2-129">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="09eb2-130">Isso pode ser um caminho para um nome de arquivo ou URI que contém os parâmetros ou os parâmetros como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="09eb2-130">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="09eb2-131">-Plano</span><span class="sxs-lookup"><span data-stu-id="09eb2-131">-Plan</span></span>
<span data-ttu-id="09eb2-132">Uma tabela de hash que representa as propriedades do plano de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="09eb2-132">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="09eb2-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="09eb2-133">-Pre</span></span>
<span data-ttu-id="09eb2-134">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="09eb2-134">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="09eb2-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09eb2-135">-ResourceGroupName</span></span>
<span data-ttu-id="09eb2-136">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="09eb2-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09eb2-137">-Marca</span><span class="sxs-lookup"><span data-stu-id="09eb2-137">-Tag</span></span>
<span data-ttu-id="09eb2-138">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="09eb2-138">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="09eb2-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="09eb2-139">-Confirm</span></span>
<span data-ttu-id="09eb2-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09eb2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09eb2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09eb2-141">-WhatIf</span></span>
<span data-ttu-id="09eb2-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="09eb2-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09eb2-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="09eb2-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09eb2-144">-ID</span><span class="sxs-lookup"><span data-stu-id="09eb2-144">-Id</span></span>
<span data-ttu-id="09eb2-145">A ID de aplicativo gerenciada totalmente qualificada, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="09eb2-145">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="09eb2-146">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="09eb2-146">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09eb2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09eb2-147">CommonParameters</span></span>
<span data-ttu-id="09eb2-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09eb2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09eb2-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09eb2-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09eb2-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09eb2-150">INPUTS</span></span>

### <span data-ttu-id="09eb2-151">System. String</span><span class="sxs-lookup"><span data-stu-id="09eb2-151">System.String</span></span>
<span data-ttu-id="09eb2-152">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="09eb2-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="09eb2-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09eb2-153">OUTPUTS</span></span>

### <span data-ttu-id="09eb2-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="09eb2-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="09eb2-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09eb2-155">NOTES</span></span>

## <span data-ttu-id="09eb2-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09eb2-156">RELATED LINKS</span></span>

