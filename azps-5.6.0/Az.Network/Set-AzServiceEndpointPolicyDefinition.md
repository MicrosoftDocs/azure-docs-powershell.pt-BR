---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: bc68a57437bae2af10b5ee39221459aebf82a2df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892939"
---
# <span data-ttu-id="a31e1-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a31e1-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="a31e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a31e1-102">SYNOPSIS</span></span>
<span data-ttu-id="a31e1-103">Atualiza uma definição de política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="a31e1-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="a31e1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a31e1-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a31e1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a31e1-105">DESCRIPTION</span></span>
<span data-ttu-id="a31e1-106">O cmdlet **Set-AzServiceEndpointPolicyDefinition** cria uma definição de política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="a31e1-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="a31e1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a31e1-107">EXAMPLES</span></span>

### <span data-ttu-id="a31e1-108">Exemplo 1: atualiza uma definição de política de ponto de extremidade de serviço em uma política de ponto de extremidade de serviço</span><span class="sxs-lookup"><span data-stu-id="a31e1-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="a31e1-109">Este comando atualiza uma definição de política de ponto de extremidade de serviço chamada Policydef1 na política de ponto de extremidade de serviço definida pelo objeto $ServiceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="a31e1-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="a31e1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a31e1-110">PARAMETERS</span></span>

### <span data-ttu-id="a31e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a31e1-111">-DefaultProfile</span></span>
<span data-ttu-id="a31e1-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a31e1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a31e1-113">-Description</span><span class="sxs-lookup"><span data-stu-id="a31e1-113">-Description</span></span>
<span data-ttu-id="a31e1-114">A descrição da definição</span><span class="sxs-lookup"><span data-stu-id="a31e1-114">The description of the definition</span></span>

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

### <span data-ttu-id="a31e1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a31e1-115">-Name</span></span>
<span data-ttu-id="a31e1-116">O nome da regra</span><span class="sxs-lookup"><span data-stu-id="a31e1-116">The name of the rule</span></span>

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

### <span data-ttu-id="a31e1-117">-Service</span><span class="sxs-lookup"><span data-stu-id="a31e1-117">-Service</span></span>
<span data-ttu-id="a31e1-118">Nome do serviço</span><span class="sxs-lookup"><span data-stu-id="a31e1-118">Name of the service</span></span>

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

### <span data-ttu-id="a31e1-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a31e1-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="a31e1-120">The NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a31e1-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="a31e1-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="a31e1-121">-ServiceResource</span></span>
<span data-ttu-id="a31e1-122">Lista de recursos de serviço</span><span class="sxs-lookup"><span data-stu-id="a31e1-122">List of service resources</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a31e1-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a31e1-123">-Confirm</span></span>
<span data-ttu-id="a31e1-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a31e1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a31e1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a31e1-125">-WhatIf</span></span>
<span data-ttu-id="a31e1-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a31e1-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a31e1-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a31e1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a31e1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a31e1-128">CommonParameters</span></span>
<span data-ttu-id="a31e1-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a31e1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a31e1-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a31e1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a31e1-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a31e1-131">INPUTS</span></span>

### <span data-ttu-id="a31e1-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a31e1-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="a31e1-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a31e1-133">OUTPUTS</span></span>

### <span data-ttu-id="a31e1-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a31e1-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="a31e1-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="a31e1-135">NOTES</span></span>

## <span data-ttu-id="a31e1-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a31e1-136">RELATED LINKS</span></span>

[<span data-ttu-id="a31e1-137">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a31e1-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="a31e1-138">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a31e1-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="a31e1-139">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a31e1-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="a31e1-140">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a31e1-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)
