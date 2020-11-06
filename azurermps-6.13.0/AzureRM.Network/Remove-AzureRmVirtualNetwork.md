---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
ms.openlocfilehash: b27ad6bfc08f6c6d9304cc78f888870a8a2dbad4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440331"
---
# <span data-ttu-id="da34c-101">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="da34c-101">Remove-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="da34c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da34c-102">SYNOPSIS</span></span>
<span data-ttu-id="da34c-103">Remove uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="da34c-103">Removes a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da34c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da34c-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da34c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da34c-105">DESCRIPTION</span></span>
<span data-ttu-id="da34c-106">O cmdlet **Remove-AzureRmVirtualNetwork** remove uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="da34c-106">The **Remove-AzureRmVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="da34c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da34c-107">EXAMPLES</span></span>

### <span data-ttu-id="da34c-108">1: criar e excluir uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="da34c-108">1: Create and delete a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="da34c-109">Este exemplo cria uma rede virtual em um grupo de recursos e, em seguida, a exclui imediatamente.</span><span class="sxs-lookup"><span data-stu-id="da34c-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="da34c-110">Para suprimir o prompt ao excluir a rede virtual, use o sinalizador-Force.</span><span class="sxs-lookup"><span data-stu-id="da34c-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="da34c-111">OS</span><span class="sxs-lookup"><span data-stu-id="da34c-111">PARAMETERS</span></span>

### <span data-ttu-id="da34c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da34c-112">-AsJob</span></span>
<span data-ttu-id="da34c-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="da34c-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da34c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da34c-114">-DefaultProfile</span></span>
<span data-ttu-id="da34c-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da34c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da34c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="da34c-116">-Force</span></span>
<span data-ttu-id="da34c-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="da34c-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="da34c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="da34c-118">-Name</span></span>
<span data-ttu-id="da34c-119">Especifica o nome da rede virtual que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="da34c-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="da34c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da34c-120">-PassThru</span></span>
<span data-ttu-id="da34c-121">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="da34c-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="da34c-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="da34c-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="da34c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da34c-123">-ResourceGroupName</span></span>
<span data-ttu-id="da34c-124">Especifica o nome do grupo de recursos que contém a rede virtual que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="da34c-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="da34c-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="da34c-125">-Confirm</span></span>
<span data-ttu-id="da34c-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da34c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da34c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da34c-127">-WhatIf</span></span>
<span data-ttu-id="da34c-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="da34c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da34c-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="da34c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da34c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da34c-130">CommonParameters</span></span>
<span data-ttu-id="da34c-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da34c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da34c-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da34c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da34c-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da34c-133">INPUTS</span></span>

### <span data-ttu-id="da34c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="da34c-134">System.String</span></span>

## <span data-ttu-id="da34c-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da34c-135">OUTPUTS</span></span>

### <span data-ttu-id="da34c-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="da34c-136">System.Boolean</span></span>

## <span data-ttu-id="da34c-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da34c-137">NOTES</span></span>

## <span data-ttu-id="da34c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da34c-138">RELATED LINKS</span></span>

[<span data-ttu-id="da34c-139">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="da34c-139">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="da34c-140">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="da34c-140">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="da34c-141">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="da34c-141">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


