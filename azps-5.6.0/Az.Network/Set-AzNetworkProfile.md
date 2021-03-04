---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
ms.openlocfilehash: 5cb8c8f93b491476e01d5ae54cf2db93ac4a848a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892067"
---
# <span data-ttu-id="6401a-101">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6401a-101">Set-AzNetworkProfile</span></span>

## <span data-ttu-id="6401a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6401a-102">SYNOPSIS</span></span>
<span data-ttu-id="6401a-103">Atualiza um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="6401a-103">Updates a network profile.</span></span>

## <span data-ttu-id="6401a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6401a-104">SYNTAX</span></span>

```
Set-AzNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6401a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6401a-105">DESCRIPTION</span></span>
<span data-ttu-id="6401a-106">O cmdlet **Set-AzPublicIpPrefix** atualiza um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="6401a-106">The **Set-AzPublicIpPrefix** cmdlet updates a network profile.</span></span>

## <span data-ttu-id="6401a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6401a-107">EXAMPLES</span></span>

### <span data-ttu-id="6401a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6401a-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzNetworkProfile
```

<span data-ttu-id="6401a-109">O primeiro comando obtém um perfil de rede existente.</span><span class="sxs-lookup"><span data-stu-id="6401a-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="6401a-110">O segundo comando atualiza uma marca e o terceiro adiciona uma configuração de interface de rede no perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="6401a-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="6401a-111">O quarto comando atualiza o perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="6401a-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="6401a-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6401a-112">PARAMETERS</span></span>

### <span data-ttu-id="6401a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6401a-113">-AsJob</span></span>
<span data-ttu-id="6401a-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6401a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6401a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6401a-115">-DefaultProfile</span></span>
<span data-ttu-id="6401a-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6401a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6401a-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6401a-117">-NetworkProfile</span></span>
<span data-ttu-id="6401a-118">O perfil de rede</span><span class="sxs-lookup"><span data-stu-id="6401a-118">The network profile</span></span>

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

### <span data-ttu-id="6401a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6401a-119">-Confirm</span></span>
<span data-ttu-id="6401a-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6401a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6401a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6401a-121">-WhatIf</span></span>
<span data-ttu-id="6401a-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6401a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6401a-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6401a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6401a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6401a-124">CommonParameters</span></span>
<span data-ttu-id="6401a-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6401a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6401a-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6401a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6401a-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6401a-127">INPUTS</span></span>

### <span data-ttu-id="6401a-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6401a-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="6401a-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6401a-129">OUTPUTS</span></span>

### <span data-ttu-id="6401a-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6401a-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="6401a-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="6401a-131">NOTES</span></span>

## <span data-ttu-id="6401a-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6401a-132">RELATED LINKS</span></span>

[<span data-ttu-id="6401a-133">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6401a-133">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="6401a-134">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6401a-134">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="6401a-135">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6401a-135">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)
