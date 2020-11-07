---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 70d110e9a539661d780c2dbce7fb8166a8f4ba97
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776603"
---
# <span data-ttu-id="6cef5-101">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6cef5-101">Remove-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="6cef5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6cef5-102">SYNOPSIS</span></span>
<span data-ttu-id="6cef5-103">Exclui uma conexão de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="6cef5-103">Deletes a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="6cef5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6cef5-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cef5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6cef5-105">DESCRIPTION</span></span>
<span data-ttu-id="6cef5-106">A conexão de gateway de rede virtual é o objeto que representa o túnel IPsec (de site para site ou vnet para vnet) conectado ao gateway de rede virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="6cef5-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="6cef5-107">O cmdlet **Remove-AzVirtualNetworkGatewayConnection** exclui o objeto da sua conexão com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6cef5-107">The **Remove-AzVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="6cef5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6cef5-108">EXAMPLES</span></span>

### <span data-ttu-id="6cef5-109">1: excluir uma conexão de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="6cef5-109">1: Delete a Virtual Network Gateway Connection</span></span>
```
Remove-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="6cef5-110">Exclui o objeto da conexão do gateway de rede virtual com o nome "mytunnel" dentro do grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="6cef5-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="6cef5-111">OS</span><span class="sxs-lookup"><span data-stu-id="6cef5-111">PARAMETERS</span></span>

### <span data-ttu-id="6cef5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cef5-112">-DefaultProfile</span></span>
<span data-ttu-id="6cef5-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6cef5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cef5-114">-Force</span><span class="sxs-lookup"><span data-stu-id="6cef5-114">-Force</span></span>
<span data-ttu-id="6cef5-115">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="6cef5-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6cef5-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="6cef5-116">-Name</span></span>
<span data-ttu-id="6cef5-117">Especifica o nome da conexão de gateway de rede virtual que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="6cef5-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6cef5-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6cef5-118">-PassThru</span></span>
<span data-ttu-id="6cef5-119">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="6cef5-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6cef5-120">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="6cef5-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6cef5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cef5-121">-ResourceGroupName</span></span>
<span data-ttu-id="6cef5-122">Especifica o nome do grupo de recursos que contém a conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6cef5-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="6cef5-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6cef5-123">-Confirm</span></span>
<span data-ttu-id="6cef5-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cef5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cef5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cef5-125">-WhatIf</span></span>
<span data-ttu-id="6cef5-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6cef5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cef5-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6cef5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cef5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cef5-128">CommonParameters</span></span>
<span data-ttu-id="6cef5-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cef5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cef5-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cef5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cef5-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6cef5-131">INPUTS</span></span>

## <span data-ttu-id="6cef5-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6cef5-132">OUTPUTS</span></span>

## <span data-ttu-id="6cef5-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6cef5-133">NOTES</span></span>

## <span data-ttu-id="6cef5-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6cef5-134">RELATED LINKS</span></span>

[<span data-ttu-id="6cef5-135">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6cef5-135">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="6cef5-136">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6cef5-136">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="6cef5-137">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6cef5-137">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)

