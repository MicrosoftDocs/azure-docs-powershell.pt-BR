---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: eaab1bdf26fb1cb99bfa7e947a4b7140971fda53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114208"
---
# <span data-ttu-id="4a915-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4a915-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="4a915-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a915-102">SYNOPSIS</span></span>
<span data-ttu-id="4a915-103">Adiciona uma definição de política de ponto de extremidade de serviço a uma política especificada.</span><span class="sxs-lookup"><span data-stu-id="4a915-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="4a915-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a915-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a915-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4a915-105">DESCRIPTION</span></span>
<span data-ttu-id="4a915-106">O cmdlet **Add-AzServiceEndpointPolicyDefinition** adiciona uma definição de política de ponto de extremidade de serviço à política.</span><span class="sxs-lookup"><span data-stu-id="4a915-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="4a915-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4a915-107">EXAMPLES</span></span>

### <span data-ttu-id="4a915-108">Exemplo 1: atualiza uma definição de política de ponto de extremidade de serviço em uma política de ponto de extremidade de serviço</span><span class="sxs-lookup"><span data-stu-id="4a915-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="4a915-109">Este comando atualizou a definição da política de ponto de extremidade de serviço com o nome ServiceEndpointPolicyDefinition1, serviço Microsoft.Storage, assinaturas de recursos de serviço/sub1 e descrição "Nova Definição" que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $policydef.</span><span class="sxs-lookup"><span data-stu-id="4a915-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="4a915-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a915-110">PARAMETERS</span></span>

### <span data-ttu-id="4a915-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a915-111">-DefaultProfile</span></span>
<span data-ttu-id="4a915-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4a915-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a915-113">-Descrição</span><span class="sxs-lookup"><span data-stu-id="4a915-113">-Description</span></span>
<span data-ttu-id="4a915-114">A descrição da definição</span><span class="sxs-lookup"><span data-stu-id="4a915-114">The description of the definition</span></span>

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

### <span data-ttu-id="4a915-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a915-115">-Name</span></span>
<span data-ttu-id="4a915-116">O nome da definição da política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="4a915-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="4a915-117">-Serviço</span><span class="sxs-lookup"><span data-stu-id="4a915-117">-Service</span></span>
<span data-ttu-id="4a915-118">Nome do serviço</span><span class="sxs-lookup"><span data-stu-id="4a915-118">Name of the service</span></span>

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

### <span data-ttu-id="4a915-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4a915-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="4a915-120">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4a915-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="4a915-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="4a915-121">-ServiceResource</span></span>
<span data-ttu-id="4a915-122">Lista de recursos de serviço</span><span class="sxs-lookup"><span data-stu-id="4a915-122">List of service resources</span></span>

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

### <span data-ttu-id="4a915-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4a915-123">-Confirm</span></span>
<span data-ttu-id="4a915-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a915-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a915-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a915-125">-WhatIf</span></span>
<span data-ttu-id="4a915-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4a915-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a915-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4a915-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a915-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a915-128">CommonParameters</span></span>
<span data-ttu-id="4a915-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a915-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a915-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a915-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a915-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="4a915-131">INPUTS</span></span>

### <span data-ttu-id="4a915-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4a915-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="4a915-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="4a915-133">OUTPUTS</span></span>

### <span data-ttu-id="4a915-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4a915-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="4a915-135">Notas</span><span class="sxs-lookup"><span data-stu-id="4a915-135">NOTES</span></span>

## <span data-ttu-id="4a915-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a915-136">RELATED LINKS</span></span>

[<span data-ttu-id="4a915-137">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4a915-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="4a915-138">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4a915-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="4a915-139">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4a915-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="4a915-140">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4a915-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
