---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: fdff53931891ce62b2182f2c8c78d54312141f5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771974"
---
# <span data-ttu-id="b3208-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b3208-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="b3208-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3208-102">SYNOPSIS</span></span>
<span data-ttu-id="b3208-103">Obtém uma política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="b3208-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="b3208-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3208-104">SYNTAX</span></span>

### <span data-ttu-id="b3208-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b3208-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3208-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3208-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3208-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b3208-107">DESCRIPTION</span></span>
<span data-ttu-id="b3208-108">O cmdlet **Get-AzServiceEndpointPolicy** Obtém uma política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="b3208-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="b3208-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3208-109">EXAMPLES</span></span>

### <span data-ttu-id="b3208-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b3208-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b3208-111">Esse comando obtém a política de ponto de extremidade do serviço chamada ServiceEndpointPolicy1 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $policy.</span><span class="sxs-lookup"><span data-stu-id="b3208-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="b3208-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b3208-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b3208-113">Esse comando obtém uma lista de todas as políticas de ponto de extremidade do serviço no grupo de recursos chamado ResourceGroup01 e as armazena na variável $policyList.</span><span class="sxs-lookup"><span data-stu-id="b3208-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="b3208-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b3208-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="b3208-115">Esse comando obtém uma lista de todas as políticas de ponto de extremidade do serviço que começam com "ServiceEndpointPolicy".</span><span class="sxs-lookup"><span data-stu-id="b3208-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="b3208-116">OS</span><span class="sxs-lookup"><span data-stu-id="b3208-116">PARAMETERS</span></span>

### <span data-ttu-id="b3208-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3208-117">-DefaultProfile</span></span>
<span data-ttu-id="b3208-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b3208-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3208-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3208-119">-Name</span></span>
<span data-ttu-id="b3208-120">O nome da política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="b3208-120">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="b3208-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3208-121">-ResourceGroupName</span></span>
<span data-ttu-id="b3208-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b3208-122">The resource group name.</span></span>

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

### <span data-ttu-id="b3208-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3208-123">-ResourceId</span></span>
<span data-ttu-id="b3208-124">A ID da política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="b3208-124">The ID of the service endpoint policy.</span></span>

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

### <span data-ttu-id="b3208-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b3208-125">-Confirm</span></span>
<span data-ttu-id="b3208-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3208-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3208-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3208-127">-WhatIf</span></span>
<span data-ttu-id="b3208-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b3208-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3208-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b3208-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3208-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3208-130">CommonParameters</span></span>
<span data-ttu-id="b3208-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3208-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3208-132">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3208-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3208-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b3208-133">INPUTS</span></span>

### <span data-ttu-id="b3208-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b3208-134">System.String</span></span>

## <span data-ttu-id="b3208-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b3208-135">OUTPUTS</span></span>

### <span data-ttu-id="b3208-136">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b3208-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="b3208-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b3208-137">NOTES</span></span>

## <span data-ttu-id="b3208-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3208-138">RELATED LINKS</span></span>

[<span data-ttu-id="b3208-139">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b3208-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="b3208-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b3208-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="b3208-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b3208-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
