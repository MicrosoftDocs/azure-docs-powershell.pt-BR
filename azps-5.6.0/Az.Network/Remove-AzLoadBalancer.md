---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: efe24ad1feae60ed71bd65206c52cfbf0b27df18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891136"
---
# <span data-ttu-id="83320-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="83320-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="83320-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83320-102">SYNOPSIS</span></span>
<span data-ttu-id="83320-103">Remove um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="83320-103">Removes a load balancer.</span></span>

## <span data-ttu-id="83320-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="83320-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83320-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="83320-105">DESCRIPTION</span></span>
<span data-ttu-id="83320-106">O cmdlet **Remove-AzLoadBalancer** remove um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="83320-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="83320-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="83320-107">EXAMPLES</span></span>

### <span data-ttu-id="83320-108">Exemplo 1: Remover um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="83320-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="83320-109">Este comando exclui um balanceador de carga chamado MyLoadBalancer no grupo de recursos chamado MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="83320-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="83320-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="83320-110">PARAMETERS</span></span>

### <span data-ttu-id="83320-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83320-111">-AsJob</span></span>
<span data-ttu-id="83320-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="83320-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83320-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83320-113">-DefaultProfile</span></span>
<span data-ttu-id="83320-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="83320-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83320-115">-Force</span><span class="sxs-lookup"><span data-stu-id="83320-115">-Force</span></span>
<span data-ttu-id="83320-116">Indica que esse cmdlet remove o balanceador de carga, independentemente de os recursos a ele atribuídos.</span><span class="sxs-lookup"><span data-stu-id="83320-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83320-117">-Name</span><span class="sxs-lookup"><span data-stu-id="83320-117">-Name</span></span>
<span data-ttu-id="83320-118">Especifica o nome do balanceador de carga a ser removido.</span><span class="sxs-lookup"><span data-stu-id="83320-118">Specifies the name of the load balancer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83320-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83320-119">-PassThru</span></span>
<span data-ttu-id="83320-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="83320-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="83320-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="83320-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83320-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83320-122">-ResourceGroupName</span></span>
<span data-ttu-id="83320-123">Especifica o nome do grupo de recursos que contém o balanceador de carga a ser removido.</span><span class="sxs-lookup"><span data-stu-id="83320-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83320-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83320-124">-Confirm</span></span>
<span data-ttu-id="83320-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83320-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83320-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83320-126">-WhatIf</span></span>
<span data-ttu-id="83320-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="83320-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83320-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="83320-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83320-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83320-129">CommonParameters</span></span>
<span data-ttu-id="83320-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83320-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83320-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83320-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83320-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83320-132">INPUTS</span></span>

### <span data-ttu-id="83320-133">System.String</span><span class="sxs-lookup"><span data-stu-id="83320-133">System.String</span></span>

## <span data-ttu-id="83320-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="83320-134">OUTPUTS</span></span>

### <span data-ttu-id="83320-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="83320-135">System.Boolean</span></span>

## <span data-ttu-id="83320-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="83320-136">NOTES</span></span>

## <span data-ttu-id="83320-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83320-137">RELATED LINKS</span></span>

[<span data-ttu-id="83320-138">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="83320-138">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="83320-139">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="83320-139">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="83320-140">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="83320-140">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


