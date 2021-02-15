---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 496e5aca71d1a947b97c8fd27cab348cee9ba49b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112782"
---
# <span data-ttu-id="c512e-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c512e-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="c512e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c512e-102">SYNOPSIS</span></span>
<span data-ttu-id="c512e-103">Redefine a chave compartilhada da conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c512e-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="c512e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c512e-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c512e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c512e-105">DESCRIPTION</span></span>
<span data-ttu-id="c512e-106">Redefine a chave compartilhada da conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c512e-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="c512e-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c512e-107">EXAMPLES</span></span>

### <span data-ttu-id="c512e-108">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="c512e-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="c512e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c512e-109">PARAMETERS</span></span>

### <span data-ttu-id="c512e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c512e-110">-DefaultProfile</span></span>
<span data-ttu-id="c512e-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c512e-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c512e-112">-Forçar</span><span class="sxs-lookup"><span data-stu-id="c512e-112">-Force</span></span>
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

### <span data-ttu-id="c512e-113">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="c512e-113">-KeyLength</span></span>
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

### <span data-ttu-id="c512e-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="c512e-114">-Name</span></span>
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

### <span data-ttu-id="c512e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c512e-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c512e-116">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c512e-116">-Confirm</span></span>
<span data-ttu-id="c512e-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c512e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c512e-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c512e-118">-WhatIf</span></span>
<span data-ttu-id="c512e-119">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c512e-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c512e-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c512e-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c512e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c512e-121">CommonParameters</span></span>
<span data-ttu-id="c512e-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c512e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c512e-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c512e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c512e-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="c512e-124">INPUTS</span></span>

### <span data-ttu-id="c512e-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c512e-125">System.String</span></span>

### <span data-ttu-id="c512e-126">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="c512e-126">System.UInt32</span></span>

## <span data-ttu-id="c512e-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="c512e-127">OUTPUTS</span></span>

### <span data-ttu-id="c512e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c512e-128">System.String</span></span>

## <span data-ttu-id="c512e-129">Notas</span><span class="sxs-lookup"><span data-stu-id="c512e-129">NOTES</span></span>

## <span data-ttu-id="c512e-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c512e-130">RELATED LINKS</span></span>

[<span data-ttu-id="c512e-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c512e-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="c512e-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c512e-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
