---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 146e43ce5f1816994a1d408e215e4b3e27c2bbca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262904"
---
# <span data-ttu-id="796b5-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="796b5-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="796b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="796b5-102">SYNOPSIS</span></span>
<span data-ttu-id="796b5-103">Remove uma definição de política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="796b5-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="796b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="796b5-104">SYNTAX</span></span>

### <span data-ttu-id="796b5-105">RemoveByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="796b5-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="796b5-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="796b5-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="796b5-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="796b5-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="796b5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="796b5-108">DESCRIPTION</span></span>
<span data-ttu-id="796b5-109">O cmdlet **Remove-AzServiceEndpointPolicy** remove uma política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="796b5-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="796b5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="796b5-110">EXAMPLES</span></span>

### <span data-ttu-id="796b5-111">Exemplo 1: Remove uma política de ponto de extremidade do serviço usando Name</span><span class="sxs-lookup"><span data-stu-id="796b5-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="796b5-112">Esse comando Remove uma política de ponto de extremidade de serviço com o nome PolicyDef1</span><span class="sxs-lookup"><span data-stu-id="796b5-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="796b5-113">OS</span><span class="sxs-lookup"><span data-stu-id="796b5-113">PARAMETERS</span></span>

### <span data-ttu-id="796b5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="796b5-114">-DefaultProfile</span></span>
<span data-ttu-id="796b5-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="796b5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="796b5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="796b5-116">-InputObject</span></span>
<span data-ttu-id="796b5-117">O objeto de definição da política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="796b5-117">The service endpoint policy definition object.</span></span>

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

### <span data-ttu-id="796b5-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="796b5-118">-Name</span></span>
<span data-ttu-id="796b5-119">O nome da definição de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="796b5-119">The name of the service endpoint definition</span></span>

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

### <span data-ttu-id="796b5-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="796b5-120">-ResourceId</span></span>
<span data-ttu-id="796b5-121">A ID da definição de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="796b5-121">The ID of the service endpoint definition.</span></span>

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

### <span data-ttu-id="796b5-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="796b5-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="796b5-123">O ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="796b5-123">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="796b5-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="796b5-124">-Confirm</span></span>
<span data-ttu-id="796b5-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="796b5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="796b5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="796b5-126">-WhatIf</span></span>
<span data-ttu-id="796b5-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="796b5-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="796b5-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="796b5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="796b5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="796b5-129">CommonParameters</span></span>
<span data-ttu-id="796b5-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="796b5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="796b5-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="796b5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="796b5-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="796b5-132">INPUTS</span></span>

### <span data-ttu-id="796b5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="796b5-133">System.String</span></span>

### <span data-ttu-id="796b5-134">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="796b5-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="796b5-135">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="796b5-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="796b5-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="796b5-136">OUTPUTS</span></span>

### <span data-ttu-id="796b5-137">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="796b5-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="796b5-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="796b5-138">NOTES</span></span>

## <span data-ttu-id="796b5-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="796b5-139">RELATED LINKS</span></span>

[<span data-ttu-id="796b5-140">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="796b5-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="796b5-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="796b5-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="796b5-142">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="796b5-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="796b5-143">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="796b5-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
