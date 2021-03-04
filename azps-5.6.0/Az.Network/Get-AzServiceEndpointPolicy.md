---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: eac0d67e2c9ffc77d9387eeb599ad624ac01fbbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892437"
---
# <span data-ttu-id="915d9-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="915d9-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="915d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="915d9-102">SYNOPSIS</span></span>
<span data-ttu-id="915d9-103">Obtém uma política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="915d9-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="915d9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="915d9-104">SYNTAX</span></span>

### <span data-ttu-id="915d9-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="915d9-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="915d9-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="915d9-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="915d9-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="915d9-107">DESCRIPTION</span></span>
<span data-ttu-id="915d9-108">O cmdlet **Get-AzServiceEndpointPolicy** obtém uma política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="915d9-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="915d9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="915d9-109">EXAMPLES</span></span>

### <span data-ttu-id="915d9-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="915d9-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="915d9-111">Este comando obtém a política de ponto de extremidade de serviço chamada ServiceEndpointPolicy1 que pertence ao grupo de recursos chamado ResourceGroup01 e armazena-a na variável $policy.</span><span class="sxs-lookup"><span data-stu-id="915d9-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="915d9-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="915d9-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="915d9-113">Este comando obtém uma lista de todas as políticas de ponto de extremidade de serviço no grupo de recursos chamado ResourceGroup01 e armazena-a na variável $policyList de serviço.</span><span class="sxs-lookup"><span data-stu-id="915d9-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="915d9-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="915d9-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="915d9-115">Este comando obtém uma lista de todas as políticas de ponto de extremidade de serviço que começam com "ServiceEndpointPolicy".</span><span class="sxs-lookup"><span data-stu-id="915d9-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="915d9-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="915d9-116">PARAMETERS</span></span>

### <span data-ttu-id="915d9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="915d9-117">-DefaultProfile</span></span>
<span data-ttu-id="915d9-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="915d9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="915d9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="915d9-119">-Name</span></span>
<span data-ttu-id="915d9-120">O nome da política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="915d9-120">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="915d9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="915d9-121">-ResourceGroupName</span></span>
<span data-ttu-id="915d9-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="915d9-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="915d9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="915d9-123">-ResourceId</span></span>
<span data-ttu-id="915d9-124">A ID da política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="915d9-124">The ID of the service endpoint policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="915d9-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="915d9-125">-Confirm</span></span>
<span data-ttu-id="915d9-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="915d9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="915d9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="915d9-127">-WhatIf</span></span>
<span data-ttu-id="915d9-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="915d9-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="915d9-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="915d9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="915d9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="915d9-130">CommonParameters</span></span>
<span data-ttu-id="915d9-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="915d9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="915d9-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="915d9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="915d9-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="915d9-133">INPUTS</span></span>

### <span data-ttu-id="915d9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="915d9-134">System.String</span></span>

## <span data-ttu-id="915d9-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="915d9-135">OUTPUTS</span></span>

### <span data-ttu-id="915d9-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="915d9-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="915d9-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="915d9-137">NOTES</span></span>

## <span data-ttu-id="915d9-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="915d9-138">RELATED LINKS</span></span>

[<span data-ttu-id="915d9-139">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="915d9-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="915d9-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="915d9-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="915d9-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="915d9-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
