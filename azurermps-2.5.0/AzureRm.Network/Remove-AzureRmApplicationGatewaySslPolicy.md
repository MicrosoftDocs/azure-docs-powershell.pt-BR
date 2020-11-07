---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslpolicy
schema: 2.0.0
ms.openlocfilehash: 383ad627ff7a633d508daccde70e3de395e4ad57
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785476"
---
# <span data-ttu-id="331ce-101">Remove-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="331ce-101">Remove-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="331ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="331ce-102">SYNOPSIS</span></span>
<span data-ttu-id="331ce-103">Remove uma política SSL de um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="331ce-103">Removes an SSL policy from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="331ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="331ce-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="331ce-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="331ce-105">DESCRIPTION</span></span>
<span data-ttu-id="331ce-106">O cmdlet Remove-AzureRmApplicationGatewaySslPolicy remove a política SSL de um Application Gateway do Azure.</span><span class="sxs-lookup"><span data-stu-id="331ce-106">The Remove-AzureRmApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="331ce-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="331ce-107">EXAMPLES</span></span>

### <span data-ttu-id="331ce-108">Exemplo 1: remover uma política SSL de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="331ce-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="331ce-109">Esse comando Remove a política SSL do gateway do aplicativo chamado ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="331ce-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="331ce-110">OS</span><span class="sxs-lookup"><span data-stu-id="331ce-110">PARAMETERS</span></span>

### <span data-ttu-id="331ce-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="331ce-111">-ApplicationGateway</span></span>
<span data-ttu-id="331ce-112">Especifica o Application Gateway do qual esse cmdlet Remove a política SSL.</span><span class="sxs-lookup"><span data-stu-id="331ce-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="331ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="331ce-113">-DefaultProfile</span></span>
<span data-ttu-id="331ce-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="331ce-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331ce-115">-Force</span><span class="sxs-lookup"><span data-stu-id="331ce-115">-Force</span></span>
<span data-ttu-id="331ce-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="331ce-116">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331ce-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="331ce-117">-Confirm</span></span>
<span data-ttu-id="331ce-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="331ce-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="331ce-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="331ce-119">-WhatIf</span></span>
<span data-ttu-id="331ce-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="331ce-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="331ce-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="331ce-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="331ce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="331ce-122">CommonParameters</span></span>
<span data-ttu-id="331ce-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="331ce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="331ce-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="331ce-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="331ce-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="331ce-125">INPUTS</span></span>

### <span data-ttu-id="331ce-126">System. String</span><span class="sxs-lookup"><span data-stu-id="331ce-126">System.String</span></span>

## <span data-ttu-id="331ce-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="331ce-127">OUTPUTS</span></span>

### <span data-ttu-id="331ce-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="331ce-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="331ce-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="331ce-129">NOTES</span></span>
<span data-ttu-id="331ce-130">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="331ce-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="331ce-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="331ce-131">RELATED LINKS</span></span>

[<span data-ttu-id="331ce-132">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="331ce-132">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="331ce-133">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="331ce-133">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="331ce-134">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="331ce-134">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

