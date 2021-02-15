---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
ms.openlocfilehash: cdea7cba3dea72df80b8571198bb50d5e337b14e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111565"
---
# <span data-ttu-id="6429e-101">Reset-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6429e-101">Reset-AzP2sVpnGateway</span></span>

## <span data-ttu-id="6429e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6429e-102">SYNOPSIS</span></span>
<span data-ttu-id="6429e-103">Redefine o gateway VPN escalável P2S.</span><span class="sxs-lookup"><span data-stu-id="6429e-103">Resets the scalable P2S VPN gateway.</span></span>

## <span data-ttu-id="6429e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6429e-104">SYNTAX</span></span>

```
Reset-AzP2sVpnGateway -P2SVpnGateway <PSP2SVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6429e-105">ByP2SVpnGatewayName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6429e-105">ByP2SVpnGatewayName (Default)</span></span>
```
Reset-- -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6429e-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="6429e-106">ByP2SVpnGatewayObject</span></span>
```
Reset-- -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6429e-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="6429e-107">ByP2SVpnGatewayResourceId</span></span>
```
Reset-- -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6429e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6429e-108">DESCRIPTION</span></span>
<span data-ttu-id="6429e-109">Redefine o P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6429e-109">Resets the P2SVpnGateway</span></span>

## <span data-ttu-id="6429e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6429e-110">EXAMPLES</span></span>

### <span data-ttu-id="6429e-111">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="6429e-111">Example 1:</span></span>
```
$Gateway = Get-AzP2SVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzP2sVpnGateway -P2SVpnGateway $Gateway
```

## <span data-ttu-id="6429e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6429e-112">PARAMETERS</span></span>

### <span data-ttu-id="6429e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6429e-113">-AsJob</span></span>
<span data-ttu-id="6429e-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6429e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6429e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6429e-115">-DefaultProfile</span></span>
<span data-ttu-id="6429e-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6429e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6429e-117">-P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6429e-117">-P2SVpnGateway</span></span>
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

### <span data-ttu-id="6429e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6429e-118">CommonParameters</span></span>
<span data-ttu-id="6429e-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6429e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6429e-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6429e-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6429e-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="6429e-121">INPUTS</span></span>

### <span data-ttu-id="6429e-122">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6429e-122">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

### <span data-ttu-id="6429e-123">System.String</span><span class="sxs-lookup"><span data-stu-id="6429e-123">System.String</span></span>

## <span data-ttu-id="6429e-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="6429e-124">OUTPUTS</span></span>

### <span data-ttu-id="6429e-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6429e-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="6429e-126">Notas</span><span class="sxs-lookup"><span data-stu-id="6429e-126">NOTES</span></span>

## <span data-ttu-id="6429e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6429e-127">RELATED LINKS</span></span>

[<span data-ttu-id="6429e-128">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6429e-128">Get-AzP2sVpnGateway</span></span>](./Get-AzP2sVpnGateway.md)

[<span data-ttu-id="6429e-129">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6429e-129">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="6429e-130">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6429e-130">Remove-AzP2sVpnGateway</span></span>](./Remove-AzP2sVpnGateway.md)

[<span data-ttu-id="6429e-131">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6429e-131">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)
