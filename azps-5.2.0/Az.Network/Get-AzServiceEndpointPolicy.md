---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: a74edbec0051e3a77ab3ac10595f787dd45a2dfc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263255"
---
# <span data-ttu-id="adba6-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="adba6-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="adba6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="adba6-102">SYNOPSIS</span></span>
<span data-ttu-id="adba6-103">Obtém uma política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="adba6-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="adba6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="adba6-104">SYNTAX</span></span>

### <span data-ttu-id="adba6-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="adba6-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adba6-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="adba6-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adba6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="adba6-107">DESCRIPTION</span></span>
<span data-ttu-id="adba6-108">O cmdlet **Get-AzServiceEndpointPolicy** Obtém uma política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="adba6-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="adba6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="adba6-109">EXAMPLES</span></span>

### <span data-ttu-id="adba6-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="adba6-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="adba6-111">Esse comando obtém a política de ponto de extremidade do serviço chamada ServiceEndpointPolicy1 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $policy.</span><span class="sxs-lookup"><span data-stu-id="adba6-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="adba6-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="adba6-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="adba6-113">Esse comando obtém uma lista de todas as políticas de ponto de extremidade do serviço no grupo de recursos chamado ResourceGroup01 e as armazena na variável $policyList.</span><span class="sxs-lookup"><span data-stu-id="adba6-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="adba6-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="adba6-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="adba6-115">Esse comando obtém uma lista de todas as políticas de ponto de extremidade do serviço que começam com "ServiceEndpointPolicy".</span><span class="sxs-lookup"><span data-stu-id="adba6-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="adba6-116">OS</span><span class="sxs-lookup"><span data-stu-id="adba6-116">PARAMETERS</span></span>

### <span data-ttu-id="adba6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adba6-117">-DefaultProfile</span></span>
<span data-ttu-id="adba6-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="adba6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adba6-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="adba6-119">-Name</span></span>
<span data-ttu-id="adba6-120">O nome da política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="adba6-120">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="adba6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adba6-121">-ResourceGroupName</span></span>
<span data-ttu-id="adba6-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="adba6-122">The resource group name.</span></span>

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

### <span data-ttu-id="adba6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adba6-123">-ResourceId</span></span>
<span data-ttu-id="adba6-124">A ID da política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="adba6-124">The ID of the service endpoint policy.</span></span>

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

### <span data-ttu-id="adba6-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="adba6-125">-Confirm</span></span>
<span data-ttu-id="adba6-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adba6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adba6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adba6-127">-WhatIf</span></span>
<span data-ttu-id="adba6-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="adba6-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="adba6-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="adba6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adba6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adba6-130">CommonParameters</span></span>
<span data-ttu-id="adba6-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adba6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adba6-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="adba6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adba6-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="adba6-133">INPUTS</span></span>

### <span data-ttu-id="adba6-134">System. String</span><span class="sxs-lookup"><span data-stu-id="adba6-134">System.String</span></span>

## <span data-ttu-id="adba6-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="adba6-135">OUTPUTS</span></span>

### <span data-ttu-id="adba6-136">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="adba6-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="adba6-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="adba6-137">NOTES</span></span>

## <span data-ttu-id="adba6-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="adba6-138">RELATED LINKS</span></span>

[<span data-ttu-id="adba6-139">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="adba6-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="adba6-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="adba6-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="adba6-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="adba6-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
