---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
ms.openlocfilehash: 6757c9c0b9eeb0b3408a07713c62812d361d814a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440994"
---
# <span data-ttu-id="94809-101">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="94809-101">Remove-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="94809-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94809-102">SYNOPSIS</span></span>
<span data-ttu-id="94809-103">Remove um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="94809-103">Removes a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94809-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94809-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94809-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="94809-105">DESCRIPTION</span></span>
<span data-ttu-id="94809-106">O cmdlet **Remove-AzureRmLoadBalancer** remove um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="94809-106">The **Remove-AzureRmLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="94809-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94809-107">EXAMPLES</span></span>

### <span data-ttu-id="94809-108">Exemplo 1: remover um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="94809-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="94809-109">Esse comando exclui um balanceador de carga chamado MyLoadBalancer no grupo de recursos chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="94809-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="94809-110">OS</span><span class="sxs-lookup"><span data-stu-id="94809-110">PARAMETERS</span></span>

### <span data-ttu-id="94809-111">-Force</span><span class="sxs-lookup"><span data-stu-id="94809-111">-Force</span></span>
<span data-ttu-id="94809-112">Indica que esse cmdlet Remove o balanceador de carga independentemente de os recursos serem atribuídos a ele.</span><span class="sxs-lookup"><span data-stu-id="94809-112">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94809-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="94809-113">-Name</span></span>
<span data-ttu-id="94809-114">Especifica o nome do balanceador de carga a ser removido.</span><span class="sxs-lookup"><span data-stu-id="94809-114">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="94809-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94809-115">-PassThru</span></span>
<span data-ttu-id="94809-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="94809-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="94809-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="94809-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="94809-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94809-118">-ResourceGroupName</span></span>
<span data-ttu-id="94809-119">Especifica o nome do grupo de recursos que contém o balanceador de carga a ser removido.</span><span class="sxs-lookup"><span data-stu-id="94809-119">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="94809-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="94809-120">-Confirm</span></span>
<span data-ttu-id="94809-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94809-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94809-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94809-122">-WhatIf</span></span>
<span data-ttu-id="94809-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="94809-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94809-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="94809-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94809-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94809-125">-DefaultProfile</span></span>
<span data-ttu-id="94809-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94809-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94809-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94809-127">CommonParameters</span></span>
<span data-ttu-id="94809-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94809-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94809-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94809-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94809-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="94809-130">INPUTS</span></span>

## <span data-ttu-id="94809-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="94809-131">OUTPUTS</span></span>

## <span data-ttu-id="94809-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="94809-132">NOTES</span></span>

## <span data-ttu-id="94809-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94809-133">RELATED LINKS</span></span>

[<span data-ttu-id="94809-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="94809-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="94809-135">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="94809-135">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="94809-136">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="94809-136">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


