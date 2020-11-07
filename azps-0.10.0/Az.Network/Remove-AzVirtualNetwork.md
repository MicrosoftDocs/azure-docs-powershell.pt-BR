---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetwork.md
ms.openlocfilehash: b65fcbc132923f18c0a70187403e4c4ba2cef52a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776606"
---
# <span data-ttu-id="f3e0a-101">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f3e0a-101">Remove-AzVirtualNetwork</span></span>

## <span data-ttu-id="f3e0a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f3e0a-102">SYNOPSIS</span></span>
<span data-ttu-id="f3e0a-103">Remove uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f3e0a-103">Removes a virtual network.</span></span>

## <span data-ttu-id="f3e0a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3e0a-104">SYNTAX</span></span>

```
Remove-AzVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3e0a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f3e0a-105">DESCRIPTION</span></span>
<span data-ttu-id="f3e0a-106">O cmdlet **Remove-AzVirtualNetwork** remove uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="f3e0a-106">The **Remove-AzVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="f3e0a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f3e0a-107">EXAMPLES</span></span>

### <span data-ttu-id="f3e0a-108">1: criar e excluir uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="f3e0a-108">1: Create and delete a virtual network</span></span>
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

<span data-ttu-id="f3e0a-109">Este exemplo cria uma rede virtual em um grupo de recursos e, em seguida, a exclui imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f3e0a-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="f3e0a-110">Para suprimir o prompt ao excluir a rede virtual, use o sinalizador-Force.</span><span class="sxs-lookup"><span data-stu-id="f3e0a-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="f3e0a-111">OS</span><span class="sxs-lookup"><span data-stu-id="f3e0a-111">PARAMETERS</span></span>

### <span data-ttu-id="f3e0a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3e0a-112">-AsJob</span></span>
<span data-ttu-id="f3e0a-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f3e0a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3e0a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3e0a-114">-DefaultProfile</span></span>
<span data-ttu-id="f3e0a-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f3e0a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3e0a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f3e0a-116">-Force</span></span>
<span data-ttu-id="f3e0a-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f3e0a-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f3e0a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3e0a-118">-Name</span></span>
<span data-ttu-id="f3e0a-119">Especifica o nome da rede virtual que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="f3e0a-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f3e0a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3e0a-120">-PassThru</span></span>
<span data-ttu-id="f3e0a-121">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="f3e0a-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f3e0a-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f3e0a-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f3e0a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3e0a-123">-ResourceGroupName</span></span>
<span data-ttu-id="f3e0a-124">Especifica o nome do grupo de recursos que contém a rede virtual que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="f3e0a-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f3e0a-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f3e0a-125">-Confirm</span></span>
<span data-ttu-id="f3e0a-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3e0a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3e0a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3e0a-127">-WhatIf</span></span>
<span data-ttu-id="f3e0a-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f3e0a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3e0a-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f3e0a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3e0a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3e0a-130">CommonParameters</span></span>
<span data-ttu-id="f3e0a-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3e0a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3e0a-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3e0a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3e0a-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f3e0a-133">INPUTS</span></span>

## <span data-ttu-id="f3e0a-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f3e0a-134">OUTPUTS</span></span>

## <span data-ttu-id="f3e0a-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f3e0a-135">NOTES</span></span>

## <span data-ttu-id="f3e0a-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3e0a-136">RELATED LINKS</span></span>

[<span data-ttu-id="f3e0a-137">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f3e0a-137">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="f3e0a-138">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f3e0a-138">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="f3e0a-139">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f3e0a-139">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

