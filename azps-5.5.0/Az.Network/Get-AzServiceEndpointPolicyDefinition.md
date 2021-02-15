---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 164fc5edb4bac3b90debde0aaf6205c719f5c95c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115150"
---
# <span data-ttu-id="b914b-101">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b914b-101">Get-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="b914b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b914b-102">SYNOPSIS</span></span>
<span data-ttu-id="b914b-103">Obtém uma definição de política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b914b-103">Gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="b914b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b914b-104">SYNTAX</span></span>

```
Get-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b914b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b914b-105">DESCRIPTION</span></span>
<span data-ttu-id="b914b-106">O cmdlet **Get-AzServiceEndpointPolicyDefinition obtém** uma definição de política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b914b-106">The **Get-AzServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="b914b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b914b-107">EXAMPLES</span></span>

### <span data-ttu-id="b914b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b914b-108">Example 1</span></span>
```
$policydef= Get-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="b914b-109">Esse comando obtém a definição de política de ponto de extremidade de serviço chamada ServiceEndpointPolicyDefinition1 no ServiceEndpointPolicy $Policy armazena-a na variável $policydef.</span><span class="sxs-lookup"><span data-stu-id="b914b-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="b914b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b914b-110">PARAMETERS</span></span>

### <span data-ttu-id="b914b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b914b-111">-DefaultProfile</span></span>
<span data-ttu-id="b914b-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b914b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b914b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="b914b-113">-Name</span></span>
<span data-ttu-id="b914b-114">O nome da definição da política de ponto de extremidade de serviço</span><span class="sxs-lookup"><span data-stu-id="b914b-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="b914b-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b914b-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="b914b-116">A política de ponto de extremidade serviço</span><span class="sxs-lookup"><span data-stu-id="b914b-116">The Service endpoint policy</span></span>

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

### <span data-ttu-id="b914b-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b914b-117">-Confirm</span></span>
<span data-ttu-id="b914b-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b914b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b914b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b914b-119">-WhatIf</span></span>
<span data-ttu-id="b914b-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b914b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b914b-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b914b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b914b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b914b-122">CommonParameters</span></span>
<span data-ttu-id="b914b-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b914b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b914b-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b914b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b914b-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="b914b-125">INPUTS</span></span>

### <span data-ttu-id="b914b-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b914b-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="b914b-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="b914b-127">OUTPUTS</span></span>

### <span data-ttu-id="b914b-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b914b-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="b914b-129">Notas</span><span class="sxs-lookup"><span data-stu-id="b914b-129">NOTES</span></span>

## <span data-ttu-id="b914b-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b914b-130">RELATED LINKS</span></span>

[<span data-ttu-id="b914b-131">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b914b-131">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="b914b-132">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b914b-132">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="b914b-133">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b914b-133">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="b914b-134">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b914b-134">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
