---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: 271033c39e049a423a15228968ad20c985b57036
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115093"
---
# <span data-ttu-id="5b949-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b949-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="5b949-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b949-102">SYNOPSIS</span></span>
<span data-ttu-id="5b949-103">Remove um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="5b949-103">Removes a load balancer.</span></span>

## <span data-ttu-id="5b949-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b949-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b949-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b949-105">DESCRIPTION</span></span>
<span data-ttu-id="5b949-106">O **cmdlet Remove-AzLoadBalancer** remove um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="5b949-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="5b949-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5b949-107">EXAMPLES</span></span>

### <span data-ttu-id="5b949-108">Exemplo 1: Remover um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="5b949-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="5b949-109">Esse comando exclui um balanceador de carga chamado MyLoadBalancer no grupo de recursos chamado MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5b949-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="5b949-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b949-110">PARAMETERS</span></span>

### <span data-ttu-id="5b949-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b949-111">-AsJob</span></span>
<span data-ttu-id="5b949-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5b949-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b949-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b949-113">-DefaultProfile</span></span>
<span data-ttu-id="5b949-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="5b949-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b949-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="5b949-115">-Force</span></span>
<span data-ttu-id="5b949-116">Indica que esse cmdlet remove o balanceador de carga, independentemente de se os recursos estão atribuídos a ele.</span><span class="sxs-lookup"><span data-stu-id="5b949-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="5b949-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b949-117">-Name</span></span>
<span data-ttu-id="5b949-118">Especifica o nome do balanceador de carga a ser removido.</span><span class="sxs-lookup"><span data-stu-id="5b949-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="5b949-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b949-119">-PassThru</span></span>
<span data-ttu-id="5b949-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="5b949-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5b949-121">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="5b949-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5b949-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b949-122">-ResourceGroupName</span></span>
<span data-ttu-id="5b949-123">Especifica o nome do grupo de recursos que contém o balanceador de carga a ser removido.</span><span class="sxs-lookup"><span data-stu-id="5b949-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="5b949-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5b949-124">-Confirm</span></span>
<span data-ttu-id="5b949-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b949-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b949-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b949-126">-WhatIf</span></span>
<span data-ttu-id="5b949-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5b949-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b949-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5b949-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b949-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b949-129">CommonParameters</span></span>
<span data-ttu-id="5b949-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b949-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b949-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b949-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b949-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="5b949-132">INPUTS</span></span>

### <span data-ttu-id="5b949-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5b949-133">System.String</span></span>

## <span data-ttu-id="5b949-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="5b949-134">OUTPUTS</span></span>

### <span data-ttu-id="5b949-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5b949-135">System.Boolean</span></span>

## <span data-ttu-id="5b949-136">Notas</span><span class="sxs-lookup"><span data-stu-id="5b949-136">NOTES</span></span>

## <span data-ttu-id="5b949-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b949-137">RELATED LINKS</span></span>

[<span data-ttu-id="5b949-138">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b949-138">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="5b949-139">Novo-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b949-139">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="5b949-140">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b949-140">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


