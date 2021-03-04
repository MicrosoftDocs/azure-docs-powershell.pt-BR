---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/powershell/module/az.resources/move-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
ms.openlocfilehash: 16e43df2da9509d7fb222f3299a4c611d146026c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886718"
---
# <span data-ttu-id="4a819-101">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="4a819-101">Move-AzResource</span></span>

## <span data-ttu-id="4a819-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a819-102">SYNOPSIS</span></span>
<span data-ttu-id="4a819-103">Move um recurso para um grupo de recursos ou assinatura diferente.</span><span class="sxs-lookup"><span data-stu-id="4a819-103">Moves a resource to a different resource group or subscription.</span></span>

## <span data-ttu-id="4a819-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4a819-104">SYNTAX</span></span>

```
Move-AzResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a819-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4a819-105">DESCRIPTION</span></span>
<span data-ttu-id="4a819-106">O cmdlet **Move-AzResource** move os recursos existentes para um grupo de recursos diferente.</span><span class="sxs-lookup"><span data-stu-id="4a819-106">The **Move-AzResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="4a819-107">Esse grupo de recursos pode estar em uma assinatura diferente.</span><span class="sxs-lookup"><span data-stu-id="4a819-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="4a819-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a819-108">EXAMPLES</span></span>

### <span data-ttu-id="4a819-109">Exemplo 1: mover um recurso para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4a819-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="4a819-110">O primeiro comando obtém um recurso chamado ContosoStorageAccount usando o cmdlet Get-AzResource e armazena esse recurso na variável $Resource.</span><span class="sxs-lookup"><span data-stu-id="4a819-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="4a819-111">O segundo comando move esse recurso para o grupo de recursos chamado ResourceGroup14.</span><span class="sxs-lookup"><span data-stu-id="4a819-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="4a819-112">O comando identifica o recurso a ser movimentado usando a **propriedade ResourceId** do $Resource.</span><span class="sxs-lookup"><span data-stu-id="4a819-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="4a819-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4a819-113">PARAMETERS</span></span>

### <span data-ttu-id="4a819-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4a819-114">-ApiVersion</span></span>
<span data-ttu-id="4a819-115">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="4a819-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4a819-116">Se você não especificar uma versão, este cmdlet usará a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="4a819-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4a819-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a819-117">-DefaultProfile</span></span>
<span data-ttu-id="4a819-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4a819-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a819-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a819-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="4a819-120">Especifica o nome do grupo de recursos no qual esse cmdlet move recursos.</span><span class="sxs-lookup"><span data-stu-id="4a819-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a819-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a819-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="4a819-122">Especifica a ID da assinatura na qual esse cmdlet move recursos .</span><span class="sxs-lookup"><span data-stu-id="4a819-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: Id, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a819-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4a819-123">-Force</span></span>
<span data-ttu-id="4a819-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="4a819-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4a819-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="4a819-125">-Pre</span></span>
<span data-ttu-id="4a819-126">Indica que esse cmdlet considera versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="4a819-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4a819-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a819-127">-ResourceId</span></span>
<span data-ttu-id="4a819-128">Especifica uma matriz de IDs dos recursos que esse cmdlet move.</span><span class="sxs-lookup"><span data-stu-id="4a819-128">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a819-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a819-129">-Confirm</span></span>
<span data-ttu-id="4a819-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a819-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a819-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a819-131">-WhatIf</span></span>
<span data-ttu-id="4a819-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4a819-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a819-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4a819-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a819-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a819-134">CommonParameters</span></span>
<span data-ttu-id="4a819-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a819-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a819-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a819-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a819-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a819-137">INPUTS</span></span>

### <span data-ttu-id="4a819-138">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4a819-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4a819-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4a819-139">System.String[]</span></span>

## <span data-ttu-id="4a819-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4a819-140">OUTPUTS</span></span>

### <span data-ttu-id="4a819-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4a819-141">System.Boolean</span></span>

## <span data-ttu-id="4a819-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="4a819-142">NOTES</span></span>

## <span data-ttu-id="4a819-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a819-143">RELATED LINKS</span></span>

[<span data-ttu-id="4a819-144">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="4a819-144">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="4a819-145">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="4a819-145">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="4a819-146">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="4a819-146">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="4a819-147">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="4a819-147">Set-AzResource</span></span>](./Set-AzResource.md)


