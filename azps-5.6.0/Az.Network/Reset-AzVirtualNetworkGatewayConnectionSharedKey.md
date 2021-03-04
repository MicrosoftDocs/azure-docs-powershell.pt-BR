---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 6b2121c581d3d7da990813884cf0097064b73f44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888829"
---
# <span data-ttu-id="6ca9f-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6ca9f-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="6ca9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ca9f-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca9f-103">Redefine a chave compartilhada da conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6ca9f-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="6ca9f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6ca9f-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ca9f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6ca9f-105">DESCRIPTION</span></span>
<span data-ttu-id="6ca9f-106">Redefine a chave compartilhada da conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6ca9f-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="6ca9f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ca9f-107">EXAMPLES</span></span>

### <span data-ttu-id="6ca9f-108">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="6ca9f-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="6ca9f-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6ca9f-109">PARAMETERS</span></span>

### <span data-ttu-id="6ca9f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca9f-110">-DefaultProfile</span></span>
<span data-ttu-id="6ca9f-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6ca9f-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ca9f-112">-Force</span><span class="sxs-lookup"><span data-stu-id="6ca9f-112">-Force</span></span>
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

### <span data-ttu-id="6ca9f-113">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="6ca9f-113">-KeyLength</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca9f-114">-Name</span><span class="sxs-lookup"><span data-stu-id="6ca9f-114">-Name</span></span>
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

### <span data-ttu-id="6ca9f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ca9f-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="6ca9f-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ca9f-116">-Confirm</span></span>
<span data-ttu-id="6ca9f-117">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ca9f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ca9f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ca9f-118">-WhatIf</span></span>
<span data-ttu-id="6ca9f-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6ca9f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ca9f-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6ca9f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ca9f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca9f-121">CommonParameters</span></span>
<span data-ttu-id="6ca9f-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ca9f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca9f-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ca9f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca9f-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ca9f-124">INPUTS</span></span>

### <span data-ttu-id="6ca9f-125">System.String</span><span class="sxs-lookup"><span data-stu-id="6ca9f-125">System.String</span></span>

### <span data-ttu-id="6ca9f-126">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="6ca9f-126">System.UInt32</span></span>

## <span data-ttu-id="6ca9f-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6ca9f-127">OUTPUTS</span></span>

### <span data-ttu-id="6ca9f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6ca9f-128">System.String</span></span>

## <span data-ttu-id="6ca9f-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="6ca9f-129">NOTES</span></span>

## <span data-ttu-id="6ca9f-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ca9f-130">RELATED LINKS</span></span>

[<span data-ttu-id="6ca9f-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6ca9f-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="6ca9f-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6ca9f-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
