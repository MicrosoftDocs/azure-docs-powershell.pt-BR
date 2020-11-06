---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
ms.openlocfilehash: 37dfce09dfcfc2dac3e561abc5957245d844763a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600109"
---
# <span data-ttu-id="cbfbe-101">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cbfbe-101">Remove-AzVirtualNetwork</span></span>

## <span data-ttu-id="cbfbe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cbfbe-102">SYNOPSIS</span></span>
<span data-ttu-id="cbfbe-103">Remove uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-103">Removes a virtual network.</span></span>

## <span data-ttu-id="cbfbe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cbfbe-104">SYNTAX</span></span>

```
Remove-AzVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbfbe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cbfbe-105">DESCRIPTION</span></span>
<span data-ttu-id="cbfbe-106">O cmdlet **Remove-AzVirtualNetwork** remove uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-106">The **Remove-AzVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="cbfbe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbfbe-107">EXAMPLES</span></span>

### <span data-ttu-id="cbfbe-108">1: criar e excluir uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="cbfbe-108">1: Create and delete a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="cbfbe-109">Este exemplo cria uma rede virtual em um grupo de recursos e, em seguida, a exclui imediatamente.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="cbfbe-110">Para suprimir o prompt ao excluir a rede virtual, use o sinalizador-Force.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="cbfbe-111">OS</span><span class="sxs-lookup"><span data-stu-id="cbfbe-111">PARAMETERS</span></span>

### <span data-ttu-id="cbfbe-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbfbe-112">-AsJob</span></span>
<span data-ttu-id="cbfbe-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cbfbe-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cbfbe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbfbe-114">-DefaultProfile</span></span>
<span data-ttu-id="cbfbe-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbfbe-116">-Force</span><span class="sxs-lookup"><span data-stu-id="cbfbe-116">-Force</span></span>
<span data-ttu-id="cbfbe-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cbfbe-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="cbfbe-118">-Name</span></span>
<span data-ttu-id="cbfbe-119">Especifica o nome da rede virtual que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cbfbe-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbfbe-120">-PassThru</span></span>
<span data-ttu-id="cbfbe-121">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cbfbe-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cbfbe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbfbe-123">-ResourceGroupName</span></span>
<span data-ttu-id="cbfbe-124">Especifica o nome do grupo de recursos que contém a rede virtual que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cbfbe-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cbfbe-125">-Confirm</span></span>
<span data-ttu-id="cbfbe-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbfbe-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbfbe-127">-WhatIf</span></span>
<span data-ttu-id="cbfbe-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbfbe-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbfbe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbfbe-130">CommonParameters</span></span>
<span data-ttu-id="cbfbe-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbfbe-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbfbe-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbfbe-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cbfbe-133">INPUTS</span></span>

### <span data-ttu-id="cbfbe-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cbfbe-134">System.String</span></span>

## <span data-ttu-id="cbfbe-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cbfbe-135">OUTPUTS</span></span>

### <span data-ttu-id="cbfbe-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cbfbe-136">System.Boolean</span></span>

## <span data-ttu-id="cbfbe-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cbfbe-137">NOTES</span></span>

## <span data-ttu-id="cbfbe-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbfbe-138">RELATED LINKS</span></span>

[<span data-ttu-id="cbfbe-139">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cbfbe-139">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="cbfbe-140">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cbfbe-140">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="cbfbe-141">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cbfbe-141">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


