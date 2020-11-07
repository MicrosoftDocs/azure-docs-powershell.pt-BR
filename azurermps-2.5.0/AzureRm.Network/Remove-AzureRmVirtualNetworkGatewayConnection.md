---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
ms.openlocfilehash: fd50f9d9c49b91139753d9ac0fc503a71955962a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785462"
---
# <span data-ttu-id="cc732-101">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cc732-101">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="cc732-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc732-102">SYNOPSIS</span></span>
<span data-ttu-id="cc732-103">Exclui uma conexão de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="cc732-103">Deletes a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc732-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc732-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc732-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc732-105">DESCRIPTION</span></span>
<span data-ttu-id="cc732-106">A conexão de gateway de rede virtual é o objeto que representa o túnel IPsec (de site para site ou vnet para vnet) conectado ao gateway de rede virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="cc732-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="cc732-107">O cmdlet **Remove-AzureRmVirtualNetworkGatewayConnection** exclui o objeto da sua conexão com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cc732-107">The **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="cc732-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc732-108">EXAMPLES</span></span>

### <span data-ttu-id="cc732-109">1: excluir uma conexão de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="cc732-109">1: Delete a Virtual Network Gateway Connection</span></span>
```
Remove-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="cc732-110">Exclui o objeto da conexão do gateway de rede virtual com o nome "mytunnel" dentro do grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="cc732-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="cc732-111">OS</span><span class="sxs-lookup"><span data-stu-id="cc732-111">PARAMETERS</span></span>

### <span data-ttu-id="cc732-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc732-112">-DefaultProfile</span></span>
<span data-ttu-id="cc732-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc732-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc732-114">-Force</span><span class="sxs-lookup"><span data-stu-id="cc732-114">-Force</span></span>
<span data-ttu-id="cc732-115">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="cc732-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cc732-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="cc732-116">-Name</span></span>
<span data-ttu-id="cc732-117">Especifica o nome da conexão de gateway de rede virtual que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="cc732-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cc732-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc732-118">-PassThru</span></span>
<span data-ttu-id="cc732-119">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="cc732-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cc732-120">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="cc732-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cc732-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc732-121">-ResourceGroupName</span></span>
<span data-ttu-id="cc732-122">Especifica o nome do grupo de recursos que contém a conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="cc732-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="cc732-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cc732-123">-Confirm</span></span>
<span data-ttu-id="cc732-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc732-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc732-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc732-125">-WhatIf</span></span>
<span data-ttu-id="cc732-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cc732-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc732-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cc732-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc732-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc732-128">CommonParameters</span></span>
<span data-ttu-id="cc732-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc732-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc732-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc732-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc732-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc732-131">INPUTS</span></span>

## <span data-ttu-id="cc732-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc732-132">OUTPUTS</span></span>

## <span data-ttu-id="cc732-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc732-133">NOTES</span></span>

## <span data-ttu-id="cc732-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc732-134">RELATED LINKS</span></span>

[<span data-ttu-id="cc732-135">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cc732-135">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="cc732-136">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cc732-136">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="cc732-137">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cc732-137">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)


