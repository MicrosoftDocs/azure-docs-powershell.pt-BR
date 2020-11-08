---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
ms.openlocfilehash: 736e9abe12b00420a4d494510f2cd0d737ae3e02
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124759"
---
# <span data-ttu-id="e50a1-101">Reset-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e50a1-101">Reset-AzP2sVpnGateway</span></span>

## <span data-ttu-id="e50a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e50a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e50a1-103">Redefine o gateway de VPN P2S escalável.</span><span class="sxs-lookup"><span data-stu-id="e50a1-103">Resets the scalable P2S VPN gateway.</span></span>

## <span data-ttu-id="e50a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e50a1-104">SYNTAX</span></span>

```
Reset-AzP2sVpnGateway -P2SVpnGateway <PSP2SVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e50a1-105">ByP2SVpnGatewayName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e50a1-105">ByP2SVpnGatewayName (Default)</span></span>
```
Reset-- -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e50a1-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="e50a1-106">ByP2SVpnGatewayObject</span></span>
```
Reset-- -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e50a1-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="e50a1-107">ByP2SVpnGatewayResourceId</span></span>
```
Reset-- -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e50a1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e50a1-108">DESCRIPTION</span></span>
<span data-ttu-id="e50a1-109">Redefine o P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e50a1-109">Resets the P2SVpnGateway</span></span>

## <span data-ttu-id="e50a1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e50a1-110">EXAMPLES</span></span>

### <span data-ttu-id="e50a1-111">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="e50a1-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzP2sVpnGateway -P2SVpnGateway $Gateway
```

## <span data-ttu-id="e50a1-112">OS</span><span class="sxs-lookup"><span data-stu-id="e50a1-112">PARAMETERS</span></span>

### <span data-ttu-id="e50a1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e50a1-113">-AsJob</span></span>
<span data-ttu-id="e50a1-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e50a1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e50a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e50a1-115">-DefaultProfile</span></span>
<span data-ttu-id="e50a1-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e50a1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e50a1-117">-P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e50a1-117">-P2SVpnGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e50a1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e50a1-118">CommonParameters</span></span>
<span data-ttu-id="e50a1-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e50a1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e50a1-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e50a1-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e50a1-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e50a1-121">INPUTS</span></span>

### <span data-ttu-id="e50a1-122">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e50a1-122">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

### <span data-ttu-id="e50a1-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e50a1-123">System.String</span></span>

## <span data-ttu-id="e50a1-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e50a1-124">OUTPUTS</span></span>

### <span data-ttu-id="e50a1-125">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e50a1-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="e50a1-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e50a1-126">NOTES</span></span>

## <span data-ttu-id="e50a1-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e50a1-127">RELATED LINKS</span></span>

[<span data-ttu-id="e50a1-128">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e50a1-128">Get-AzP2sVpnGateway</span></span>](./Get-AzP2sVpnGateway.md)

[<span data-ttu-id="e50a1-129">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e50a1-129">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="e50a1-130">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e50a1-130">Remove-AzP2sVpnGateway</span></span>](./Remove-AzP2sVpnGateway.md)

[<span data-ttu-id="e50a1-131">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e50a1-131">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)
