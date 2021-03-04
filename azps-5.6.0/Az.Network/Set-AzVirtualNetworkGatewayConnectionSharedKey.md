---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 2c32263d52f8e260c67395484b2a9a2e3e479ecb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888092"
---
# <span data-ttu-id="c7481-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c7481-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="c7481-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7481-102">SYNOPSIS</span></span>
<span data-ttu-id="c7481-103">Configura a chave compartilhada da conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c7481-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="c7481-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c7481-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7481-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c7481-105">DESCRIPTION</span></span>
<span data-ttu-id="c7481-106">O cmdlet **Set-AzVirtualNetworkGatewayConnectionSharedKey** configura a chave compartilhada da conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c7481-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="c7481-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7481-107">EXAMPLES</span></span>

### <span data-ttu-id="c7481-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c7481-108">Example 1</span></span>
```powershell
PS C:\Users\alzam> Set-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

## <span data-ttu-id="c7481-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c7481-109">PARAMETERS</span></span>

### <span data-ttu-id="c7481-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7481-110">-DefaultProfile</span></span>
<span data-ttu-id="c7481-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c7481-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7481-112">-Force</span><span class="sxs-lookup"><span data-stu-id="c7481-112">-Force</span></span>
<span data-ttu-id="c7481-113">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c7481-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c7481-114">-Name</span><span class="sxs-lookup"><span data-stu-id="c7481-114">-Name</span></span>
<span data-ttu-id="c7481-115">Especifica o nome da chave compartilhada do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c7481-115">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="c7481-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7481-116">-ResourceGroupName</span></span>
<span data-ttu-id="c7481-117">Especifica o nome do grupo de recursos ao que o gateway de rede virtual pertence</span><span class="sxs-lookup"><span data-stu-id="c7481-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="c7481-118">-Value</span><span class="sxs-lookup"><span data-stu-id="c7481-118">-Value</span></span>
<span data-ttu-id="c7481-119">Especifica o valor da chave compartilhada.</span><span class="sxs-lookup"><span data-stu-id="c7481-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="c7481-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7481-120">-Confirm</span></span>
<span data-ttu-id="c7481-121">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7481-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7481-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7481-122">-WhatIf</span></span>
<span data-ttu-id="c7481-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c7481-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7481-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c7481-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7481-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7481-125">CommonParameters</span></span>
<span data-ttu-id="c7481-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7481-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7481-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7481-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7481-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7481-128">INPUTS</span></span>

### <span data-ttu-id="c7481-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c7481-129">System.String</span></span>

## <span data-ttu-id="c7481-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c7481-130">OUTPUTS</span></span>

### <span data-ttu-id="c7481-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c7481-131">System.String</span></span>

## <span data-ttu-id="c7481-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="c7481-132">NOTES</span></span>

## <span data-ttu-id="c7481-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7481-133">RELATED LINKS</span></span>

[<span data-ttu-id="c7481-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c7481-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="c7481-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c7481-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)
