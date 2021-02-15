---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: a74edbec0051e3a77ab3ac10595f787dd45a2dfc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117444"
---
# <span data-ttu-id="96b79-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="96b79-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="96b79-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96b79-102">SYNOPSIS</span></span>
<span data-ttu-id="96b79-103">Obtém uma política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="96b79-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="96b79-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96b79-104">SYNTAX</span></span>

### <span data-ttu-id="96b79-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="96b79-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96b79-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96b79-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96b79-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="96b79-107">DESCRIPTION</span></span>
<span data-ttu-id="96b79-108">O **cmdlet Get-AzServiceEndpointPolicy** obtém uma política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="96b79-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="96b79-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="96b79-109">EXAMPLES</span></span>

### <span data-ttu-id="96b79-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="96b79-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="96b79-111">Esse comando obtém a política de ponto de extremidade de serviço chamada ServiceEndpointPolicy1 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $policy.</span><span class="sxs-lookup"><span data-stu-id="96b79-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="96b79-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="96b79-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="96b79-113">Esse comando obtém uma lista de todas as políticas de ponto de extremidade de serviço no grupo de recursos chamado ResourceGroup01 e o armazena na variável $policyList serviço.</span><span class="sxs-lookup"><span data-stu-id="96b79-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="96b79-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="96b79-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="96b79-115">Esse comando obtém uma lista de todas as políticas de ponto de extremidade de serviço que começam com "ServiceEndpointPolicy".</span><span class="sxs-lookup"><span data-stu-id="96b79-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="96b79-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96b79-116">PARAMETERS</span></span>

### <span data-ttu-id="96b79-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96b79-117">-DefaultProfile</span></span>
<span data-ttu-id="96b79-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="96b79-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96b79-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="96b79-119">-Name</span></span>
<span data-ttu-id="96b79-120">O nome da política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="96b79-120">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="96b79-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96b79-121">-ResourceGroupName</span></span>
<span data-ttu-id="96b79-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="96b79-122">The resource group name.</span></span>

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

### <span data-ttu-id="96b79-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96b79-123">-ResourceId</span></span>
<span data-ttu-id="96b79-124">A ID da política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="96b79-124">The ID of the service endpoint policy.</span></span>

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

### <span data-ttu-id="96b79-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="96b79-125">-Confirm</span></span>
<span data-ttu-id="96b79-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96b79-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96b79-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96b79-127">-WhatIf</span></span>
<span data-ttu-id="96b79-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="96b79-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96b79-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="96b79-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96b79-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96b79-130">CommonParameters</span></span>
<span data-ttu-id="96b79-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96b79-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96b79-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96b79-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96b79-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="96b79-133">INPUTS</span></span>

### <span data-ttu-id="96b79-134">System.String</span><span class="sxs-lookup"><span data-stu-id="96b79-134">System.String</span></span>

## <span data-ttu-id="96b79-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="96b79-135">OUTPUTS</span></span>

### <span data-ttu-id="96b79-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="96b79-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="96b79-137">Notas</span><span class="sxs-lookup"><span data-stu-id="96b79-137">NOTES</span></span>

## <span data-ttu-id="96b79-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96b79-138">RELATED LINKS</span></span>

[<span data-ttu-id="96b79-139">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="96b79-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="96b79-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="96b79-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="96b79-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="96b79-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
