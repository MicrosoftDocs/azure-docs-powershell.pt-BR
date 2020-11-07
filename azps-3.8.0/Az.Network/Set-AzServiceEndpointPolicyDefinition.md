---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 46d86b6a910abcd00257277f61bb44dd426ab945
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778457"
---
# <span data-ttu-id="2d4c5-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2d4c5-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="2d4c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d4c5-102">SYNOPSIS</span></span>
<span data-ttu-id="2d4c5-103">Atualiza uma definição de política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="2d4c5-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="2d4c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d4c5-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d4c5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2d4c5-105">DESCRIPTION</span></span>
<span data-ttu-id="2d4c5-106">O cmdlet **set-AzServiceEndpointPolicyDefinition** cria uma definição de política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="2d4c5-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="2d4c5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d4c5-107">EXAMPLES</span></span>

### <span data-ttu-id="2d4c5-108">Exemplo 1: atualiza uma definição de política de ponto de extremidade do serviço em uma política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="2d4c5-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="2d4c5-109">Esse comando atualiza uma definição de política de ponto de extremidade de serviço chamada Policydef1 na política de ponto de extremidade do serviço definida pela $ServiceEndpointPolicy do objeto.</span><span class="sxs-lookup"><span data-stu-id="2d4c5-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="2d4c5-110">OS</span><span class="sxs-lookup"><span data-stu-id="2d4c5-110">PARAMETERS</span></span>

### <span data-ttu-id="2d4c5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d4c5-111">-DefaultProfile</span></span>
<span data-ttu-id="2d4c5-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d4c5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d4c5-113">-Descrição</span><span class="sxs-lookup"><span data-stu-id="2d4c5-113">-Description</span></span>
<span data-ttu-id="2d4c5-114">A descrição da definição</span><span class="sxs-lookup"><span data-stu-id="2d4c5-114">The description of the definition</span></span>

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

### <span data-ttu-id="2d4c5-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d4c5-115">-Name</span></span>
<span data-ttu-id="2d4c5-116">O nome da regra</span><span class="sxs-lookup"><span data-stu-id="2d4c5-116">The name of the rule</span></span>

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

### <span data-ttu-id="2d4c5-117">-Serviço</span><span class="sxs-lookup"><span data-stu-id="2d4c5-117">-Service</span></span>
<span data-ttu-id="2d4c5-118">Nome do serviço</span><span class="sxs-lookup"><span data-stu-id="2d4c5-118">Name of the service</span></span>

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

### <span data-ttu-id="2d4c5-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2d4c5-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="2d4c5-120">O NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2d4c5-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="2d4c5-121">-Recurso do recurso</span><span class="sxs-lookup"><span data-stu-id="2d4c5-121">-ServiceResource</span></span>
<span data-ttu-id="2d4c5-122">Lista de recursos de serviço</span><span class="sxs-lookup"><span data-stu-id="2d4c5-122">List of service resources</span></span>

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

### <span data-ttu-id="2d4c5-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2d4c5-123">-Confirm</span></span>
<span data-ttu-id="2d4c5-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d4c5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d4c5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d4c5-125">-WhatIf</span></span>
<span data-ttu-id="2d4c5-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2d4c5-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d4c5-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2d4c5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d4c5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d4c5-128">CommonParameters</span></span>
<span data-ttu-id="2d4c5-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d4c5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d4c5-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d4c5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d4c5-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2d4c5-131">INPUTS</span></span>

### <span data-ttu-id="2d4c5-132">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2d4c5-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="2d4c5-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2d4c5-133">OUTPUTS</span></span>

### <span data-ttu-id="2d4c5-134">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2d4c5-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="2d4c5-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2d4c5-135">NOTES</span></span>

## <span data-ttu-id="2d4c5-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d4c5-136">RELATED LINKS</span></span>

[<span data-ttu-id="2d4c5-137">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2d4c5-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="2d4c5-138">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2d4c5-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="2d4c5-139">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2d4c5-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="2d4c5-140">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2d4c5-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)
