---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: f5ea9c291d23c6378170946ee6b605ec02742ed8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118302"
---
# <span data-ttu-id="9c2f2-101">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9c2f2-101">Remove-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="9c2f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c2f2-102">SYNOPSIS</span></span>
<span data-ttu-id="9c2f2-103">Exclui uma conexão de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="9c2f2-103">Deletes a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="9c2f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c2f2-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c2f2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c2f2-105">DESCRIPTION</span></span>
<span data-ttu-id="9c2f2-106">A conexão de gateway de rede virtual é o objeto que representa o túnel IPsec (de site para site ou vnet para vnet) conectado ao gateway de rede virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="9c2f2-107">O cmdlet **Remove-AzVirtualNetworkGatewayConnection** exclui o objeto da sua conexão com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-107">The **Remove-AzVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="9c2f2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c2f2-108">EXAMPLES</span></span>

### <span data-ttu-id="9c2f2-109">Exemplo 1: excluir uma conexão de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="9c2f2-109">Example 1: Delete a Virtual Network Gateway Connection</span></span>
```powershell
Remove-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="9c2f2-110">Exclui o objeto da conexão do gateway de rede virtual com o nome "mytunnel" dentro do grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="9c2f2-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="9c2f2-111">OS</span><span class="sxs-lookup"><span data-stu-id="9c2f2-111">PARAMETERS</span></span>

### <span data-ttu-id="9c2f2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c2f2-112">-DefaultProfile</span></span>
<span data-ttu-id="9c2f2-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c2f2-114">-Force</span><span class="sxs-lookup"><span data-stu-id="9c2f2-114">-Force</span></span>
<span data-ttu-id="9c2f2-115">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9c2f2-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c2f2-116">-Name</span></span>
<span data-ttu-id="9c2f2-117">Especifica o nome da conexão de gateway de rede virtual que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9c2f2-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c2f2-118">-PassThru</span></span>
<span data-ttu-id="9c2f2-119">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9c2f2-120">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9c2f2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c2f2-121">-ResourceGroupName</span></span>
<span data-ttu-id="9c2f2-122">Especifica o nome do grupo de recursos que contém a conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="9c2f2-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9c2f2-123">-Confirm</span></span>
<span data-ttu-id="9c2f2-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c2f2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c2f2-125">-WhatIf</span></span>
<span data-ttu-id="9c2f2-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c2f2-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c2f2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c2f2-128">CommonParameters</span></span>
<span data-ttu-id="9c2f2-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c2f2-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c2f2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c2f2-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c2f2-131">INPUTS</span></span>

### <span data-ttu-id="9c2f2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9c2f2-132">System.String</span></span>

## <span data-ttu-id="9c2f2-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c2f2-133">OUTPUTS</span></span>

### <span data-ttu-id="9c2f2-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c2f2-134">System.Boolean</span></span>

## <span data-ttu-id="9c2f2-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c2f2-135">NOTES</span></span>

## <span data-ttu-id="9c2f2-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c2f2-136">RELATED LINKS</span></span>

[<span data-ttu-id="9c2f2-137">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9c2f2-137">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="9c2f2-138">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9c2f2-138">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="9c2f2-139">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9c2f2-139">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
