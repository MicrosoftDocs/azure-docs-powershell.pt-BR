---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
ms.openlocfilehash: c63940ab03f6d288de3c1b5b0d767182168ed1fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599986"
---
# <span data-ttu-id="7204c-101">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7204c-101">Set-AzNetworkProfile</span></span>

## <span data-ttu-id="7204c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7204c-102">SYNOPSIS</span></span>
<span data-ttu-id="7204c-103">Atualiza um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="7204c-103">Updates a network profile.</span></span>

## <span data-ttu-id="7204c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7204c-104">SYNTAX</span></span>

```
Set-AzNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7204c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7204c-105">DESCRIPTION</span></span>
<span data-ttu-id="7204c-106">O cmdlet **set-AzPublicIpPrefix** atualiza um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="7204c-106">The **Set-AzPublicIpPrefix** cmdlet updates a network profile.</span></span>

## <span data-ttu-id="7204c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7204c-107">EXAMPLES</span></span>

### <span data-ttu-id="7204c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7204c-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzNetworkProfile
```

<span data-ttu-id="7204c-109">O primeiro comando obtém um perfil de rede existente.</span><span class="sxs-lookup"><span data-stu-id="7204c-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="7204c-110">O segundo comando atualiza uma marca e a terceira adiciona uma configuração de interface de rede no perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="7204c-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="7204c-111">O quarto comando atualiza o perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="7204c-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="7204c-112">OS</span><span class="sxs-lookup"><span data-stu-id="7204c-112">PARAMETERS</span></span>

### <span data-ttu-id="7204c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7204c-113">-AsJob</span></span>
<span data-ttu-id="7204c-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7204c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7204c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7204c-115">-DefaultProfile</span></span>
<span data-ttu-id="7204c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7204c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7204c-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7204c-117">-NetworkProfile</span></span>
<span data-ttu-id="7204c-118">O perfil de rede</span><span class="sxs-lookup"><span data-stu-id="7204c-118">The network profile</span></span>

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

### <span data-ttu-id="7204c-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7204c-119">-Confirm</span></span>
<span data-ttu-id="7204c-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7204c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7204c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7204c-121">-WhatIf</span></span>
<span data-ttu-id="7204c-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7204c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7204c-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7204c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7204c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7204c-124">CommonParameters</span></span>
<span data-ttu-id="7204c-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7204c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7204c-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7204c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7204c-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7204c-127">INPUTS</span></span>

### <span data-ttu-id="7204c-128">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7204c-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="7204c-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7204c-129">OUTPUTS</span></span>

### <span data-ttu-id="7204c-130">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7204c-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="7204c-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7204c-131">NOTES</span></span>

## <span data-ttu-id="7204c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7204c-132">RELATED LINKS</span></span>

[<span data-ttu-id="7204c-133">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7204c-133">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="7204c-134">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7204c-134">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="7204c-135">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7204c-135">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)
