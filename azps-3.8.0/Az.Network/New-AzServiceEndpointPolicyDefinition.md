---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 27124aa859fc9c97a74a3ed401c67de328d93884
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943247"
---
# <span data-ttu-id="dbf3c-101">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dbf3c-101">New-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="dbf3c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dbf3c-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf3c-103">Cria uma definição de política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="dbf3c-103">Creates a service endpoint policy definition.</span></span>

## <span data-ttu-id="dbf3c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbf3c-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicyDefinition -Name <String> [-Description <String>] [-ServiceResource <String[]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbf3c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dbf3c-105">DESCRIPTION</span></span>
<span data-ttu-id="dbf3c-106">O cmdlet **New-AzServiceEndpointPolicyDefinition** cria uma definição de política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="dbf3c-106">The **New-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="dbf3c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dbf3c-107">EXAMPLES</span></span>

### <span data-ttu-id="dbf3c-108">Exemplo 1: cria uma política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="dbf3c-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="dbf3c-109">Esse comando cria a definição da política de ponto de extremidade do serviço com o nome ServiceEndpointPolicyDefinition1, serviço Microsoft. Storage, assinaturas de recursos de serviço/Sub1 e descrição "New Definition" que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $policydef.</span><span class="sxs-lookup"><span data-stu-id="dbf3c-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="dbf3c-110">OS</span><span class="sxs-lookup"><span data-stu-id="dbf3c-110">PARAMETERS</span></span>

### <span data-ttu-id="dbf3c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbf3c-111">-DefaultProfile</span></span>
<span data-ttu-id="dbf3c-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dbf3c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbf3c-113">-Descrição</span><span class="sxs-lookup"><span data-stu-id="dbf3c-113">-Description</span></span>
<span data-ttu-id="dbf3c-114">A descrição da definição</span><span class="sxs-lookup"><span data-stu-id="dbf3c-114">The description of the definition</span></span>

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

### <span data-ttu-id="dbf3c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="dbf3c-115">-Name</span></span>
<span data-ttu-id="dbf3c-116">O nome da política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="dbf3c-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="dbf3c-117">-Serviço</span><span class="sxs-lookup"><span data-stu-id="dbf3c-117">-Service</span></span>
<span data-ttu-id="dbf3c-118">Nome do serviço</span><span class="sxs-lookup"><span data-stu-id="dbf3c-118">Name of the service</span></span>

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

### <span data-ttu-id="dbf3c-119">-Recurso do recurso</span><span class="sxs-lookup"><span data-stu-id="dbf3c-119">-ServiceResource</span></span>
<span data-ttu-id="dbf3c-120">Lista de recursos de serviço</span><span class="sxs-lookup"><span data-stu-id="dbf3c-120">List of service resources</span></span>

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

### <span data-ttu-id="dbf3c-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dbf3c-121">-Confirm</span></span>
<span data-ttu-id="dbf3c-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbf3c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbf3c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbf3c-123">-WhatIf</span></span>
<span data-ttu-id="dbf3c-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dbf3c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dbf3c-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dbf3c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbf3c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf3c-126">CommonParameters</span></span>
<span data-ttu-id="dbf3c-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbf3c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf3c-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbf3c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf3c-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dbf3c-129">INPUTS</span></span>

### <span data-ttu-id="dbf3c-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="dbf3c-130">None</span></span>

## <span data-ttu-id="dbf3c-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dbf3c-131">OUTPUTS</span></span>

### <span data-ttu-id="dbf3c-132">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dbf3c-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="dbf3c-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dbf3c-133">NOTES</span></span>

## <span data-ttu-id="dbf3c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dbf3c-134">RELATED LINKS</span></span>

[<span data-ttu-id="dbf3c-135">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dbf3c-135">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="dbf3c-136">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dbf3c-136">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="dbf3c-137">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dbf3c-137">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="dbf3c-138">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dbf3c-138">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
