---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 554d3285c80370559bbedfb91430d2b6801a6f51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886323"
---
# <span data-ttu-id="ecc64-101">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ecc64-101">Get-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="ecc64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecc64-102">SYNOPSIS</span></span>
<span data-ttu-id="ecc64-103">Obtém uma definição de política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="ecc64-103">Gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="ecc64-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ecc64-104">SYNTAX</span></span>

```
Get-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecc64-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ecc64-105">DESCRIPTION</span></span>
<span data-ttu-id="ecc64-106">O cmdlet **Get-AzServiceEndpointPolicyDefinition** obtém uma definição de política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="ecc64-106">The **Get-AzServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="ecc64-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ecc64-107">EXAMPLES</span></span>

### <span data-ttu-id="ecc64-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ecc64-108">Example 1</span></span>
```
$policydef= Get-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="ecc64-109">Este comando obtém a definição de política de ponto de extremidade de serviço chamada ServiceEndpointPolicyDefinition1 em ServiceEndpointPolicy $Policy armazena na variável $policydef.</span><span class="sxs-lookup"><span data-stu-id="ecc64-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="ecc64-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ecc64-110">PARAMETERS</span></span>

### <span data-ttu-id="ecc64-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecc64-111">-DefaultProfile</span></span>
<span data-ttu-id="ecc64-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ecc64-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecc64-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ecc64-113">-Name</span></span>
<span data-ttu-id="ecc64-114">O nome da definição da política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="ecc64-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="ecc64-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ecc64-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="ecc64-116">A política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="ecc64-116">The Service endpoint policy</span></span>

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

### <span data-ttu-id="ecc64-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecc64-117">-Confirm</span></span>
<span data-ttu-id="ecc64-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecc64-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecc64-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecc64-119">-WhatIf</span></span>
<span data-ttu-id="ecc64-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ecc64-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ecc64-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ecc64-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecc64-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecc64-122">CommonParameters</span></span>
<span data-ttu-id="ecc64-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecc64-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecc64-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecc64-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecc64-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ecc64-125">INPUTS</span></span>

### <span data-ttu-id="ecc64-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ecc64-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="ecc64-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ecc64-127">OUTPUTS</span></span>

### <span data-ttu-id="ecc64-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ecc64-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="ecc64-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="ecc64-129">NOTES</span></span>

## <span data-ttu-id="ecc64-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ecc64-130">RELATED LINKS</span></span>

[<span data-ttu-id="ecc64-131">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ecc64-131">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="ecc64-132">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ecc64-132">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="ecc64-133">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ecc64-133">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="ecc64-134">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ecc64-134">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
