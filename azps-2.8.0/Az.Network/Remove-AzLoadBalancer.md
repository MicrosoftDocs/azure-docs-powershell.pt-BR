---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: b91a807d5499236d45e84a9a064e7f64daa1fb57
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771526"
---
# <span data-ttu-id="a5d71-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5d71-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="a5d71-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5d71-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d71-103">Remove um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a5d71-103">Removes a load balancer.</span></span>

## <span data-ttu-id="a5d71-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5d71-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5d71-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5d71-105">DESCRIPTION</span></span>
<span data-ttu-id="a5d71-106">O cmdlet **Remove-AzLoadBalancer** remove um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="a5d71-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="a5d71-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5d71-107">EXAMPLES</span></span>

### <span data-ttu-id="a5d71-108">Exemplo 1: remover um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="a5d71-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="a5d71-109">Esse comando exclui um balanceador de carga chamado MyLoadBalancer no grupo de recursos chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="a5d71-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="a5d71-110">OS</span><span class="sxs-lookup"><span data-stu-id="a5d71-110">PARAMETERS</span></span>

### <span data-ttu-id="a5d71-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5d71-111">-AsJob</span></span>
<span data-ttu-id="a5d71-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a5d71-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5d71-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d71-113">-DefaultProfile</span></span>
<span data-ttu-id="a5d71-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5d71-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5d71-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a5d71-115">-Force</span></span>
<span data-ttu-id="a5d71-116">Indica que esse cmdlet Remove o balanceador de carga independentemente de os recursos serem atribuídos a ele.</span><span class="sxs-lookup"><span data-stu-id="a5d71-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="a5d71-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5d71-117">-Name</span></span>
<span data-ttu-id="a5d71-118">Especifica o nome do balanceador de carga a ser removido.</span><span class="sxs-lookup"><span data-stu-id="a5d71-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="a5d71-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5d71-119">-PassThru</span></span>
<span data-ttu-id="a5d71-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="a5d71-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a5d71-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="a5d71-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a5d71-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d71-122">-ResourceGroupName</span></span>
<span data-ttu-id="a5d71-123">Especifica o nome do grupo de recursos que contém o balanceador de carga a ser removido.</span><span class="sxs-lookup"><span data-stu-id="a5d71-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="a5d71-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a5d71-124">-Confirm</span></span>
<span data-ttu-id="a5d71-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5d71-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5d71-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5d71-126">-WhatIf</span></span>
<span data-ttu-id="a5d71-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a5d71-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5d71-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a5d71-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5d71-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d71-129">CommonParameters</span></span>
<span data-ttu-id="a5d71-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5d71-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d71-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5d71-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d71-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5d71-132">INPUTS</span></span>

### <span data-ttu-id="a5d71-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a5d71-133">System.String</span></span>

## <span data-ttu-id="a5d71-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5d71-134">OUTPUTS</span></span>

### <span data-ttu-id="a5d71-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5d71-135">System.Boolean</span></span>

## <span data-ttu-id="a5d71-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5d71-136">NOTES</span></span>

## <span data-ttu-id="a5d71-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5d71-137">RELATED LINKS</span></span>

[<span data-ttu-id="a5d71-138">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5d71-138">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a5d71-139">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5d71-139">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="a5d71-140">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5d71-140">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


