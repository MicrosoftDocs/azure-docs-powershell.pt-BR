---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
ms.openlocfilehash: 1ab783b4b5a49793b4f4c91f2f7bc9f5410e5ddd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427839"
---
# <span data-ttu-id="3a21a-101">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3a21a-101">Remove-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="3a21a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a21a-102">SYNOPSIS</span></span>
<span data-ttu-id="3a21a-103">Remove uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="3a21a-103">Removes a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a21a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a21a-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a21a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a21a-105">DESCRIPTION</span></span>
<span data-ttu-id="3a21a-106">O cmdlet **Remove-AzureRmVirtualNetwork** remove uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="3a21a-106">The **Remove-AzureRmVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="3a21a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a21a-107">EXAMPLES</span></span>

### <span data-ttu-id="3a21a-108">1: criar e excluir uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="3a21a-108">1: Create and delete a virtual network</span></span>
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

<span data-ttu-id="3a21a-109">Este exemplo cria uma rede virtual em um grupo de recursos e, em seguida, a exclui imediatamente.</span><span class="sxs-lookup"><span data-stu-id="3a21a-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="3a21a-110">Para suprimir o prompt ao excluir a rede virtual, use o sinalizador-Force.</span><span class="sxs-lookup"><span data-stu-id="3a21a-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="3a21a-111">OS</span><span class="sxs-lookup"><span data-stu-id="3a21a-111">PARAMETERS</span></span>

### <span data-ttu-id="3a21a-112">-Force</span><span class="sxs-lookup"><span data-stu-id="3a21a-112">-Force</span></span>
<span data-ttu-id="3a21a-113">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3a21a-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a21a-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a21a-114">-Name</span></span>
<span data-ttu-id="3a21a-115">Especifica o nome da rede virtual que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="3a21a-115">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3a21a-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a21a-116">-PassThru</span></span>
<span data-ttu-id="3a21a-117">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="3a21a-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3a21a-118">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="3a21a-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a21a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a21a-119">-ResourceGroupName</span></span>
<span data-ttu-id="3a21a-120">Especifica o nome do grupo de recursos que contém a rede virtual que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="3a21a-120">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3a21a-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3a21a-121">-Confirm</span></span>
<span data-ttu-id="3a21a-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a21a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a21a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a21a-123">-WhatIf</span></span>
<span data-ttu-id="3a21a-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3a21a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a21a-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3a21a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a21a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a21a-126">-DefaultProfile</span></span>
<span data-ttu-id="3a21a-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a21a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a21a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a21a-128">CommonParameters</span></span>
<span data-ttu-id="3a21a-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a21a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a21a-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a21a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a21a-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a21a-131">INPUTS</span></span>

## <span data-ttu-id="3a21a-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a21a-132">OUTPUTS</span></span>

## <span data-ttu-id="3a21a-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a21a-133">NOTES</span></span>

## <span data-ttu-id="3a21a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a21a-134">RELATED LINKS</span></span>

[<span data-ttu-id="3a21a-135">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3a21a-135">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="3a21a-136">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3a21a-136">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="3a21a-137">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3a21a-137">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


