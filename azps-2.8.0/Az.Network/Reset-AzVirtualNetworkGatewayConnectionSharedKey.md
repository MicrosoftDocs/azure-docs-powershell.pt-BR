---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 1fa793396fba139d1aa08e760c9aa780f8e0f166
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772233"
---
# <span data-ttu-id="52646-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="52646-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="52646-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52646-102">SYNOPSIS</span></span>
<span data-ttu-id="52646-103">Redefine a chave compartilhada da conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="52646-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="52646-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52646-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52646-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52646-105">DESCRIPTION</span></span>
<span data-ttu-id="52646-106">Redefine a chave compartilhada da conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="52646-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="52646-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52646-107">EXAMPLES</span></span>

### <span data-ttu-id="52646-108">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="52646-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="52646-109">OS</span><span class="sxs-lookup"><span data-stu-id="52646-109">PARAMETERS</span></span>

### <span data-ttu-id="52646-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52646-110">-DefaultProfile</span></span>
<span data-ttu-id="52646-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52646-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52646-112">-Force</span><span class="sxs-lookup"><span data-stu-id="52646-112">-Force</span></span>
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

### <span data-ttu-id="52646-113">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="52646-113">-KeyLength</span></span>
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

### <span data-ttu-id="52646-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="52646-114">-Name</span></span>
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

### <span data-ttu-id="52646-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52646-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="52646-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52646-116">-Confirm</span></span>
<span data-ttu-id="52646-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52646-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52646-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52646-118">-WhatIf</span></span>
<span data-ttu-id="52646-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52646-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52646-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52646-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52646-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52646-121">CommonParameters</span></span>
<span data-ttu-id="52646-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52646-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52646-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52646-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52646-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52646-124">INPUTS</span></span>

### <span data-ttu-id="52646-125">System. String</span><span class="sxs-lookup"><span data-stu-id="52646-125">System.String</span></span>

### <span data-ttu-id="52646-126">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="52646-126">System.UInt32</span></span>

## <span data-ttu-id="52646-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52646-127">OUTPUTS</span></span>

### <span data-ttu-id="52646-128">System. String</span><span class="sxs-lookup"><span data-stu-id="52646-128">System.String</span></span>

## <span data-ttu-id="52646-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52646-129">NOTES</span></span>

## <span data-ttu-id="52646-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52646-130">RELATED LINKS</span></span>

[<span data-ttu-id="52646-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="52646-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="52646-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="52646-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)