---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 164fc5edb4bac3b90debde0aaf6205c719f5c95c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433832"
---
# <span data-ttu-id="e391c-101">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e391c-101">Get-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="e391c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e391c-102">SYNOPSIS</span></span>
<span data-ttu-id="e391c-103">Obtém uma definição de política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="e391c-103">Gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="e391c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e391c-104">SYNTAX</span></span>

```
Get-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e391c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e391c-105">DESCRIPTION</span></span>
<span data-ttu-id="e391c-106">O cmdlet **Get-AzServiceEndpointPolicyDefinition** Obtém uma definição de política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="e391c-106">The **Get-AzServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="e391c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e391c-107">EXAMPLES</span></span>

### <span data-ttu-id="e391c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e391c-108">Example 1</span></span>
```
$policydef= Get-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="e391c-109">Esse comando obtém a definição da política de ponto de extremidade do serviço chamada ServiceEndpointPolicyDefinition1 em ServiceEndpointPolicy $Policy a armazena na variável $policydef.</span><span class="sxs-lookup"><span data-stu-id="e391c-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="e391c-110">OS</span><span class="sxs-lookup"><span data-stu-id="e391c-110">PARAMETERS</span></span>

### <span data-ttu-id="e391c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e391c-111">-DefaultProfile</span></span>
<span data-ttu-id="e391c-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e391c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e391c-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="e391c-113">-Name</span></span>
<span data-ttu-id="e391c-114">O nome da definição da política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="e391c-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="e391c-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e391c-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="e391c-116">Política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="e391c-116">The Service endpoint policy</span></span>

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

### <span data-ttu-id="e391c-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e391c-117">-Confirm</span></span>
<span data-ttu-id="e391c-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e391c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e391c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e391c-119">-WhatIf</span></span>
<span data-ttu-id="e391c-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e391c-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e391c-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e391c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e391c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e391c-122">CommonParameters</span></span>
<span data-ttu-id="e391c-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e391c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e391c-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e391c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e391c-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e391c-125">INPUTS</span></span>

### <span data-ttu-id="e391c-126">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e391c-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="e391c-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e391c-127">OUTPUTS</span></span>

### <span data-ttu-id="e391c-128">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e391c-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="e391c-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e391c-129">NOTES</span></span>

## <span data-ttu-id="e391c-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e391c-130">RELATED LINKS</span></span>

[<span data-ttu-id="e391c-131">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e391c-131">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="e391c-132">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e391c-132">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="e391c-133">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e391c-133">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="e391c-134">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e391c-134">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
