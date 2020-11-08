---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 496e5aca71d1a947b97c8fd27cab348cee9ba49b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115954"
---
# <span data-ttu-id="f1a2a-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f1a2a-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="f1a2a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1a2a-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a2a-103">Redefine a chave compartilhada da conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f1a2a-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="f1a2a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1a2a-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1a2a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1a2a-105">DESCRIPTION</span></span>
<span data-ttu-id="f1a2a-106">Redefine a chave compartilhada da conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f1a2a-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="f1a2a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1a2a-107">EXAMPLES</span></span>

### <span data-ttu-id="f1a2a-108">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="f1a2a-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="f1a2a-109">OS</span><span class="sxs-lookup"><span data-stu-id="f1a2a-109">PARAMETERS</span></span>

### <span data-ttu-id="f1a2a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a2a-110">-DefaultProfile</span></span>
<span data-ttu-id="f1a2a-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1a2a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1a2a-112">-Force</span><span class="sxs-lookup"><span data-stu-id="f1a2a-112">-Force</span></span>
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

### <span data-ttu-id="f1a2a-113">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="f1a2a-113">-KeyLength</span></span>
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

### <span data-ttu-id="f1a2a-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1a2a-114">-Name</span></span>
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

### <span data-ttu-id="f1a2a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1a2a-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="f1a2a-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f1a2a-116">-Confirm</span></span>
<span data-ttu-id="f1a2a-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1a2a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1a2a-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1a2a-118">-WhatIf</span></span>
<span data-ttu-id="f1a2a-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f1a2a-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1a2a-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1a2a-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1a2a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a2a-121">CommonParameters</span></span>
<span data-ttu-id="f1a2a-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1a2a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a2a-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1a2a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a2a-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1a2a-124">INPUTS</span></span>

### <span data-ttu-id="f1a2a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f1a2a-125">System.String</span></span>

### <span data-ttu-id="f1a2a-126">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="f1a2a-126">System.UInt32</span></span>

## <span data-ttu-id="f1a2a-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1a2a-127">OUTPUTS</span></span>

### <span data-ttu-id="f1a2a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f1a2a-128">System.String</span></span>

## <span data-ttu-id="f1a2a-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1a2a-129">NOTES</span></span>

## <span data-ttu-id="f1a2a-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1a2a-130">RELATED LINKS</span></span>

[<span data-ttu-id="f1a2a-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f1a2a-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="f1a2a-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f1a2a-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
