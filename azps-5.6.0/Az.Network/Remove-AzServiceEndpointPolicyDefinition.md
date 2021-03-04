---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 65303db1c76f6e7c6e1323ed0cfc88132e4c1c23
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892418"
---
# <span data-ttu-id="ee3b9-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ee3b9-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="ee3b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee3b9-102">SYNOPSIS</span></span>
<span data-ttu-id="ee3b9-103">Remove uma definição de política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="ee3b9-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="ee3b9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ee3b9-104">SYNTAX</span></span>

### <span data-ttu-id="ee3b9-105">RemoveByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ee3b9-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee3b9-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee3b9-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee3b9-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee3b9-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee3b9-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ee3b9-108">DESCRIPTION</span></span>
<span data-ttu-id="ee3b9-109">O cmdlet **Remove-AzServiceEndpointPolicy** remove uma política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="ee3b9-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="ee3b9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee3b9-110">EXAMPLES</span></span>

### <span data-ttu-id="ee3b9-111">Exemplo 1: remove uma política de ponto de extremidade de serviço usando o nome</span><span class="sxs-lookup"><span data-stu-id="ee3b9-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="ee3b9-112">Este comando remove uma política de ponto de extremidade de serviço com o nome PolicyDef1</span><span class="sxs-lookup"><span data-stu-id="ee3b9-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="ee3b9-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ee3b9-113">PARAMETERS</span></span>

### <span data-ttu-id="ee3b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee3b9-114">-DefaultProfile</span></span>
<span data-ttu-id="ee3b9-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ee3b9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee3b9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee3b9-116">-InputObject</span></span>
<span data-ttu-id="ee3b9-117">O objeto de definição de política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="ee3b9-117">The service endpoint policy definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee3b9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ee3b9-118">-Name</span></span>
<span data-ttu-id="ee3b9-119">O nome da definição do ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="ee3b9-119">The name of the service endpoint definition</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee3b9-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee3b9-120">-ResourceId</span></span>
<span data-ttu-id="ee3b9-121">A ID da definição do ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="ee3b9-121">The ID of the service endpoint definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee3b9-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ee3b9-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="ee3b9-123">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ee3b9-123">The ServiceEndpointPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee3b9-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee3b9-124">-Confirm</span></span>
<span data-ttu-id="ee3b9-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee3b9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee3b9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee3b9-126">-WhatIf</span></span>
<span data-ttu-id="ee3b9-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ee3b9-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee3b9-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ee3b9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee3b9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee3b9-129">CommonParameters</span></span>
<span data-ttu-id="ee3b9-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee3b9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee3b9-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee3b9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee3b9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee3b9-132">INPUTS</span></span>

### <span data-ttu-id="ee3b9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ee3b9-133">System.String</span></span>

### <span data-ttu-id="ee3b9-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ee3b9-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="ee3b9-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ee3b9-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="ee3b9-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ee3b9-136">OUTPUTS</span></span>

### <span data-ttu-id="ee3b9-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ee3b9-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="ee3b9-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="ee3b9-138">NOTES</span></span>

## <span data-ttu-id="ee3b9-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee3b9-139">RELATED LINKS</span></span>

[<span data-ttu-id="ee3b9-140">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ee3b9-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="ee3b9-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ee3b9-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="ee3b9-142">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ee3b9-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="ee3b9-143">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ee3b9-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
