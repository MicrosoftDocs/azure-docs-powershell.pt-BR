---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: c907c60619f5a0a2fc5f0620f086ba0b99ca62ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600114"
---
# <span data-ttu-id="f4740-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f4740-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="f4740-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f4740-102">SYNOPSIS</span></span>
<span data-ttu-id="f4740-103">Remove uma definição de política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="f4740-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="f4740-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4740-104">SYNTAX</span></span>

### <span data-ttu-id="f4740-105">RemoveByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f4740-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4740-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4740-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4740-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4740-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4740-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f4740-108">DESCRIPTION</span></span>
<span data-ttu-id="f4740-109">O cmdlet **Remove-AzServiceEndpointPolicy** remove uma política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="f4740-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="f4740-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4740-110">EXAMPLES</span></span>

### <span data-ttu-id="f4740-111">Exemplo 1: Remove uma política de ponto de extremidade do serviço usando Name</span><span class="sxs-lookup"><span data-stu-id="f4740-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="f4740-112">Esse comando Remove uma política de ponto de extremidade de serviço com o nome PolicyDef1</span><span class="sxs-lookup"><span data-stu-id="f4740-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="f4740-113">OS</span><span class="sxs-lookup"><span data-stu-id="f4740-113">PARAMETERS</span></span>

### <span data-ttu-id="f4740-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4740-114">-DefaultProfile</span></span>
<span data-ttu-id="f4740-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f4740-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4740-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4740-116">-InputObject</span></span>
<span data-ttu-id="f4740-117">O objeto de definição da política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="f4740-117">The service endpoint policy definition object.</span></span>

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

### <span data-ttu-id="f4740-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4740-118">-Name</span></span>
<span data-ttu-id="f4740-119">O nome da definição de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="f4740-119">The name of the service endpoint definition</span></span>

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

### <span data-ttu-id="f4740-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4740-120">-ResourceId</span></span>
<span data-ttu-id="f4740-121">A ID da definição de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="f4740-121">The ID of the service endpoint definition.</span></span>

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

### <span data-ttu-id="f4740-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f4740-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="f4740-123">O ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f4740-123">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="f4740-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f4740-124">-Confirm</span></span>
<span data-ttu-id="f4740-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4740-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4740-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4740-126">-WhatIf</span></span>
<span data-ttu-id="f4740-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f4740-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4740-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f4740-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4740-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4740-129">CommonParameters</span></span>
<span data-ttu-id="f4740-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4740-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4740-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4740-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4740-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f4740-132">INPUTS</span></span>

### <span data-ttu-id="f4740-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f4740-133">System.String</span></span>

### <span data-ttu-id="f4740-134">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f4740-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="f4740-135">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f4740-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f4740-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f4740-136">OUTPUTS</span></span>

### <span data-ttu-id="f4740-137">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f4740-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f4740-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f4740-138">NOTES</span></span>

## <span data-ttu-id="f4740-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4740-139">RELATED LINKS</span></span>

[<span data-ttu-id="f4740-140">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f4740-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f4740-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f4740-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f4740-142">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f4740-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f4740-143">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f4740-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
