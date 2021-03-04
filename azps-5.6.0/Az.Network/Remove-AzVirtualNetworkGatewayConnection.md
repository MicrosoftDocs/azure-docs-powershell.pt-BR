---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 3a598001421bf237f93a63fb4f45d069bf9404ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892403"
---
# <span data-ttu-id="e510a-101">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e510a-101">Remove-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="e510a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e510a-102">SYNOPSIS</span></span>
<span data-ttu-id="e510a-103">Exclui uma conexão de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="e510a-103">Deletes a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="e510a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e510a-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e510a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e510a-105">DESCRIPTION</span></span>
<span data-ttu-id="e510a-106">A Conexão de Gateway de Rede Virtual é o objeto que representa o túnel IPsec (Site para Site ou Vnet-para-Vnet) conectado ao Gateway de Rede Virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="e510a-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="e510a-107">O cmdlet **Remove-AzVirtualNetworkGatewayConnection** exclui o objeto de sua conexão com base em Nome e Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="e510a-107">The **Remove-AzVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="e510a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e510a-108">EXAMPLES</span></span>

### <span data-ttu-id="e510a-109">Exemplo 1: Excluir uma conexão de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="e510a-109">Example 1: Delete a Virtual Network Gateway Connection</span></span>
```powershell
Remove-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="e510a-110">Exclui o objeto da Conexão de Gateway de Rede Virtual com o nome "myTunnel" dentro do grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="e510a-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="e510a-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e510a-111">PARAMETERS</span></span>

### <span data-ttu-id="e510a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e510a-112">-DefaultProfile</span></span>
<span data-ttu-id="e510a-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e510a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e510a-114">-Force</span><span class="sxs-lookup"><span data-stu-id="e510a-114">-Force</span></span>
<span data-ttu-id="e510a-115">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e510a-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e510a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e510a-116">-Name</span></span>
<span data-ttu-id="e510a-117">Especifica o nome da conexão de gateway de rede virtual que esse cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="e510a-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e510a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e510a-118">-PassThru</span></span>
<span data-ttu-id="e510a-119">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="e510a-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e510a-120">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e510a-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e510a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e510a-121">-ResourceGroupName</span></span>
<span data-ttu-id="e510a-122">Especifica o nome do grupo de recursos que contém a conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e510a-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="e510a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e510a-123">-Confirm</span></span>
<span data-ttu-id="e510a-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e510a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e510a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e510a-125">-WhatIf</span></span>
<span data-ttu-id="e510a-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e510a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e510a-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e510a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e510a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e510a-128">CommonParameters</span></span>
<span data-ttu-id="e510a-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e510a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e510a-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e510a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e510a-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e510a-131">INPUTS</span></span>

### <span data-ttu-id="e510a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e510a-132">System.String</span></span>

## <span data-ttu-id="e510a-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e510a-133">OUTPUTS</span></span>

### <span data-ttu-id="e510a-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e510a-134">System.Boolean</span></span>

## <span data-ttu-id="e510a-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="e510a-135">NOTES</span></span>

## <span data-ttu-id="e510a-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e510a-136">RELATED LINKS</span></span>

[<span data-ttu-id="e510a-137">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e510a-137">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="e510a-138">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e510a-138">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="e510a-139">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e510a-139">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
