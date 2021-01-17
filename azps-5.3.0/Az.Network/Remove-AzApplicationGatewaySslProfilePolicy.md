---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 541293160a1cf9e3d32de5d378c24d1ee4b2705b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428950"
---
# <span data-ttu-id="1dd04-101">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="1dd04-101">Remove-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="1dd04-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1dd04-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd04-103">Remove uma política SSL de um perfil SSL do gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="1dd04-103">Removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="1dd04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1dd04-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dd04-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1dd04-105">DESCRIPTION</span></span>
<span data-ttu-id="1dd04-106">O cmdlet Remove-AzApplicationGatewaySslProfilePolicy remove uma política SSL de um perfil SSL do gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="1dd04-106">The Remove-AzApplicationGatewaySslProfilePolicy cmdlet removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="1dd04-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1dd04-107">EXAMPLES</span></span>

### <span data-ttu-id="1dd04-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1dd04-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> $profile = Remove-AzApplicationGatewaySslProfilePolicy -SslProfile $profile
```

<span data-ttu-id="1dd04-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1dd04-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="1dd04-110">O segundo comando obtém o perfil SSL chamado Profile01 para $AppGw e o armazena na variável $profile.</span><span class="sxs-lookup"><span data-stu-id="1dd04-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="1dd04-111">O último comando Remove a política SSL do perfil SSL armazenado em $profile.</span><span class="sxs-lookup"><span data-stu-id="1dd04-111">The last command removes the ssl policy of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="1dd04-112">OS</span><span class="sxs-lookup"><span data-stu-id="1dd04-112">PARAMETERS</span></span>

### <span data-ttu-id="1dd04-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd04-113">-DefaultProfile</span></span>
<span data-ttu-id="1dd04-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1dd04-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd04-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="1dd04-115">-SslProfile</span></span>
<span data-ttu-id="1dd04-116">O perfil SSL do applicationGateway</span><span class="sxs-lookup"><span data-stu-id="1dd04-116">The applicationGateway SSL profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd04-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1dd04-117">-Confirm</span></span>
<span data-ttu-id="1dd04-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dd04-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd04-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dd04-119">-WhatIf</span></span>
<span data-ttu-id="1dd04-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1dd04-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dd04-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1dd04-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd04-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd04-122">CommonParameters</span></span>
<span data-ttu-id="1dd04-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dd04-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd04-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1dd04-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd04-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1dd04-125">INPUTS</span></span>

### <span data-ttu-id="1dd04-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1dd04-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="1dd04-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1dd04-127">OUTPUTS</span></span>

### <span data-ttu-id="1dd04-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1dd04-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="1dd04-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1dd04-129">NOTES</span></span>

## <span data-ttu-id="1dd04-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1dd04-130">RELATED LINKS</span></span>

[<span data-ttu-id="1dd04-131">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="1dd04-131">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="1dd04-132">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="1dd04-132">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="1dd04-133">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="1dd04-133">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="1dd04-134">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="1dd04-134">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)