---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 455ee170ffba9f601cd8e3034e0c774966f92eba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775316"
---
# <span data-ttu-id="5ac8c-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5ac8c-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="5ac8c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ac8c-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac8c-103">Remove uma política SSL de um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="5ac8c-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="5ac8c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ac8c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ac8c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ac8c-105">DESCRIPTION</span></span>
<span data-ttu-id="5ac8c-106">O cmdlet Remove-AzApplicationGatewaySslPolicy remove a política SSL de um Application Gateway do Azure.</span><span class="sxs-lookup"><span data-stu-id="5ac8c-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="5ac8c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ac8c-107">EXAMPLES</span></span>

### <span data-ttu-id="5ac8c-108">Exemplo 1: remover uma política SSL de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="5ac8c-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="5ac8c-109">Esse comando Remove a política SSL do gateway do aplicativo chamado ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="5ac8c-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="5ac8c-110">OS</span><span class="sxs-lookup"><span data-stu-id="5ac8c-110">PARAMETERS</span></span>

### <span data-ttu-id="5ac8c-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ac8c-111">-ApplicationGateway</span></span>
<span data-ttu-id="5ac8c-112">Especifica o Application Gateway do qual esse cmdlet Remove a política SSL.</span><span class="sxs-lookup"><span data-stu-id="5ac8c-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="5ac8c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac8c-113">-DefaultProfile</span></span>
<span data-ttu-id="5ac8c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5ac8c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ac8c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5ac8c-115">-Force</span></span>
<span data-ttu-id="5ac8c-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="5ac8c-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5ac8c-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5ac8c-117">-Confirm</span></span>
<span data-ttu-id="5ac8c-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ac8c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ac8c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ac8c-119">-WhatIf</span></span>
<span data-ttu-id="5ac8c-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5ac8c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ac8c-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5ac8c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ac8c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac8c-122">CommonParameters</span></span>
<span data-ttu-id="5ac8c-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ac8c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac8c-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ac8c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac8c-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ac8c-125">INPUTS</span></span>

### <span data-ttu-id="5ac8c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5ac8c-126">System.String</span></span>

## <span data-ttu-id="5ac8c-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ac8c-127">OUTPUTS</span></span>

### <span data-ttu-id="5ac8c-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ac8c-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5ac8c-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ac8c-129">NOTES</span></span>
<span data-ttu-id="5ac8c-130">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="5ac8c-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="5ac8c-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ac8c-131">RELATED LINKS</span></span>

[<span data-ttu-id="5ac8c-132">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5ac8c-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="5ac8c-133">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5ac8c-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="5ac8c-134">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5ac8c-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

