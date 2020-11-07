---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: 1602c9e5fb0244239eea4eec53661c3392ac0354
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775304"
---
# <span data-ttu-id="6cfb5-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6cfb5-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="6cfb5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6cfb5-102">SYNOPSIS</span></span>
<span data-ttu-id="6cfb5-103">Remove um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-103">Removes a load balancer.</span></span>

## <span data-ttu-id="6cfb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6cfb5-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cfb5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6cfb5-105">DESCRIPTION</span></span>
<span data-ttu-id="6cfb5-106">O cmdlet **Remove-AzLoadBalancer** remove um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="6cfb5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6cfb5-107">EXAMPLES</span></span>

### <span data-ttu-id="6cfb5-108">Exemplo 1: remover um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="6cfb5-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="6cfb5-109">Esse comando exclui um balanceador de carga chamado MyLoadBalancer no grupo de recursos chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="6cfb5-110">OS</span><span class="sxs-lookup"><span data-stu-id="6cfb5-110">PARAMETERS</span></span>

### <span data-ttu-id="6cfb5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cfb5-111">-AsJob</span></span>
<span data-ttu-id="6cfb5-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6cfb5-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cfb5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cfb5-113">-DefaultProfile</span></span>
<span data-ttu-id="6cfb5-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cfb5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6cfb5-115">-Force</span></span>
<span data-ttu-id="6cfb5-116">Indica que esse cmdlet Remove o balanceador de carga independentemente de os recursos serem atribuídos a ele.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cfb5-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6cfb5-117">-Name</span></span>
<span data-ttu-id="6cfb5-118">Especifica o nome do balanceador de carga a ser removido.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-118">Specifies the name of the load balancer to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cfb5-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6cfb5-119">-PassThru</span></span>
<span data-ttu-id="6cfb5-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6cfb5-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cfb5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cfb5-122">-ResourceGroupName</span></span>
<span data-ttu-id="6cfb5-123">Especifica o nome do grupo de recursos que contém o balanceador de carga a ser removido.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cfb5-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6cfb5-124">-Confirm</span></span>
<span data-ttu-id="6cfb5-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cfb5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cfb5-126">-WhatIf</span></span>
<span data-ttu-id="6cfb5-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cfb5-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cfb5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cfb5-129">CommonParameters</span></span>
<span data-ttu-id="6cfb5-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cfb5-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cfb5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cfb5-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6cfb5-132">INPUTS</span></span>

## <span data-ttu-id="6cfb5-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6cfb5-133">OUTPUTS</span></span>

## <span data-ttu-id="6cfb5-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6cfb5-134">NOTES</span></span>

## <span data-ttu-id="6cfb5-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6cfb5-135">RELATED LINKS</span></span>

[<span data-ttu-id="6cfb5-136">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6cfb5-136">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="6cfb5-137">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6cfb5-137">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="6cfb5-138">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6cfb5-138">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


