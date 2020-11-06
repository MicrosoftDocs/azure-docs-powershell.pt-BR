---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkProfile.md
ms.openlocfilehash: 370229f44b260367759ca2f51319258627d3d8c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426316"
---
# <span data-ttu-id="c9ee5-101">Set-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c9ee5-101">Set-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="c9ee5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="c9ee5-103">Define o estado da meta para um perfil de rede existente</span><span class="sxs-lookup"><span data-stu-id="c9ee5-103">Sets the goal state for an existing network profile</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9ee5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9ee5-104">SYNTAX</span></span>

```
Set-AzureRmNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9ee5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c9ee5-105">DESCRIPTION</span></span>
<span data-ttu-id="c9ee5-106">O cmdlet **set-AzureRmPublicIpPrefix** define o estado da meta para um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="c9ee5-106">The **Set-AzureRmPublicIpPrefix** cmdlet sets the goal state for a network profile.</span></span>

## <span data-ttu-id="c9ee5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9ee5-107">EXAMPLES</span></span>

### <span data-ttu-id="c9ee5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c9ee5-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzureRmNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzureRmNetworkProfile
```

<span data-ttu-id="c9ee5-109">O primeiro comando obtém um perfil de rede existente.</span><span class="sxs-lookup"><span data-stu-id="c9ee5-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="c9ee5-110">O segundo comando atualiza uma marca e a terceira adiciona uma configuração de interface de rede no perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="c9ee5-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="c9ee5-111">O quarto comando atualiza o perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="c9ee5-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="c9ee5-112">OS</span><span class="sxs-lookup"><span data-stu-id="c9ee5-112">PARAMETERS</span></span>

### <span data-ttu-id="c9ee5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9ee5-113">-AsJob</span></span>
<span data-ttu-id="c9ee5-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c9ee5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9ee5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9ee5-115">-DefaultProfile</span></span>
<span data-ttu-id="c9ee5-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c9ee5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9ee5-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c9ee5-117">-NetworkProfile</span></span>
<span data-ttu-id="c9ee5-118">O perfil de rede</span><span class="sxs-lookup"><span data-stu-id="c9ee5-118">The network profile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9ee5-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c9ee5-119">-Confirm</span></span>
<span data-ttu-id="c9ee5-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9ee5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9ee5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9ee5-121">-WhatIf</span></span>
<span data-ttu-id="c9ee5-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c9ee5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9ee5-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c9ee5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9ee5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9ee5-124">CommonParameters</span></span>
<span data-ttu-id="c9ee5-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9ee5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9ee5-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9ee5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9ee5-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c9ee5-127">INPUTS</span></span>

### <span data-ttu-id="c9ee5-128">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c9ee5-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="c9ee5-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c9ee5-129">OUTPUTS</span></span>

### <span data-ttu-id="c9ee5-130">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c9ee5-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="c9ee5-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c9ee5-131">NOTES</span></span>

## <span data-ttu-id="c9ee5-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9ee5-132">RELATED LINKS</span></span>
