---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: a542b69b1f028a7fdfd3e02d02f95735bc4add9f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892070"
---
# <span data-ttu-id="d458f-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d458f-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="d458f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d458f-102">SYNOPSIS</span></span>
<span data-ttu-id="d458f-103">Atualiza uma configuração de toque para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d458f-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="d458f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d458f-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d458f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d458f-105">DESCRIPTION</span></span>
<span data-ttu-id="d458f-106">O **Set-AzNetworkInterfaceTapConfig** atualiza uma configuração de toque para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d458f-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="d458f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d458f-107">EXAMPLES</span></span>

### <span data-ttu-id="d458f-108">Exemplo 1: Definir o TapConfiguration com o nome TapConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="d458f-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="d458f-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d458f-109">PARAMETERS</span></span>

### <span data-ttu-id="d458f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d458f-110">-AsJob</span></span>
<span data-ttu-id="d458f-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d458f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d458f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d458f-112">-DefaultProfile</span></span>
<span data-ttu-id="d458f-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d458f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d458f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="d458f-114">-Force</span></span>
<span data-ttu-id="d458f-115">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="d458f-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d458f-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d458f-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="d458f-117">A configuração de Toque de NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d458f-117">The NetworkInterface Tap configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d458f-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d458f-118">-Confirm</span></span>
<span data-ttu-id="d458f-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d458f-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d458f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d458f-120">-WhatIf</span></span>
<span data-ttu-id="d458f-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d458f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d458f-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d458f-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d458f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d458f-123">CommonParameters</span></span>
<span data-ttu-id="d458f-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d458f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d458f-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d458f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d458f-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d458f-126">INPUTS</span></span>

### <span data-ttu-id="d458f-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="d458f-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="d458f-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d458f-128">OUTPUTS</span></span>

### <span data-ttu-id="d458f-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d458f-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="d458f-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="d458f-130">NOTES</span></span>

## <span data-ttu-id="d458f-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d458f-131">RELATED LINKS</span></span>

[<span data-ttu-id="d458f-132">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d458f-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="d458f-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d458f-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="d458f-134">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d458f-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)
