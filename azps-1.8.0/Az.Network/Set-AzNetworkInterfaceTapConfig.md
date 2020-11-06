---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 2a860c295106755c326624a0bb37de22976d072d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599992"
---
# <span data-ttu-id="6de4b-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6de4b-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="6de4b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6de4b-102">SYNOPSIS</span></span>
<span data-ttu-id="6de4b-103">Atualiza uma configuração de toque para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="6de4b-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="6de4b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6de4b-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6de4b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6de4b-105">DESCRIPTION</span></span>
<span data-ttu-id="6de4b-106">O **set-AzNetworkInterfaceTapConfig** atualiza uma configuração de toque para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="6de4b-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="6de4b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6de4b-107">EXAMPLES</span></span>

### <span data-ttu-id="6de4b-108">Exemplo 1: definir o TapConfiguration com o nome TapConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="6de4b-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="6de4b-109">OS</span><span class="sxs-lookup"><span data-stu-id="6de4b-109">PARAMETERS</span></span>

### <span data-ttu-id="6de4b-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6de4b-110">-AsJob</span></span>
<span data-ttu-id="6de4b-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6de4b-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6de4b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de4b-112">-DefaultProfile</span></span>
<span data-ttu-id="6de4b-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6de4b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6de4b-114">-Force</span><span class="sxs-lookup"><span data-stu-id="6de4b-114">-Force</span></span>
<span data-ttu-id="6de4b-115">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="6de4b-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6de4b-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6de4b-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="6de4b-117">A NetworkInterface, toque em configurtion</span><span class="sxs-lookup"><span data-stu-id="6de4b-117">The NetworkInterface Tap configurtion</span></span>

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

### <span data-ttu-id="6de4b-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6de4b-118">-Confirm</span></span>
<span data-ttu-id="6de4b-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6de4b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6de4b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6de4b-120">-WhatIf</span></span>
<span data-ttu-id="6de4b-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6de4b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6de4b-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6de4b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6de4b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de4b-123">CommonParameters</span></span>
<span data-ttu-id="6de4b-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6de4b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de4b-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6de4b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de4b-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6de4b-126">INPUTS</span></span>

### <span data-ttu-id="6de4b-127">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="6de4b-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="6de4b-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6de4b-128">OUTPUTS</span></span>

### <span data-ttu-id="6de4b-129">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6de4b-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="6de4b-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6de4b-130">NOTES</span></span>

## <span data-ttu-id="6de4b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6de4b-131">RELATED LINKS</span></span>

[<span data-ttu-id="6de4b-132">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6de4b-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="6de4b-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6de4b-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="6de4b-134">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6de4b-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)
