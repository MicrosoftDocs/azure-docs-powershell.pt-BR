---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 74b8664a9b57089fd116620779354515ea984c79
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785448"
---
# <span data-ttu-id="d81ab-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d81ab-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="d81ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d81ab-102">SYNOPSIS</span></span>
<span data-ttu-id="d81ab-103">Interrompe um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="d81ab-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d81ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d81ab-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d81ab-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d81ab-105">DESCRIPTION</span></span>
<span data-ttu-id="d81ab-106">O cmdlet **Stop-AzureRmApplicationGateway** interrompe um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d81ab-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="d81ab-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d81ab-107">EXAMPLES</span></span>

### <span data-ttu-id="d81ab-108">Exemplo 1: parar um gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="d81ab-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="d81ab-109">Esse comando interrompe o aplicativo gateway armazenado na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d81ab-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="d81ab-110">OS</span><span class="sxs-lookup"><span data-stu-id="d81ab-110">PARAMETERS</span></span>

### <span data-ttu-id="d81ab-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d81ab-111">-ApplicationGateway</span></span>
<span data-ttu-id="d81ab-112">Especifica o gateway do aplicativo em que este cmdlet é interrompido.</span><span class="sxs-lookup"><span data-stu-id="d81ab-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="d81ab-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d81ab-113">-AsJob</span></span>
<span data-ttu-id="d81ab-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d81ab-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d81ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d81ab-115">-DefaultProfile</span></span>
<span data-ttu-id="d81ab-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d81ab-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d81ab-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d81ab-117">CommonParameters</span></span>
<span data-ttu-id="d81ab-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d81ab-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d81ab-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d81ab-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d81ab-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d81ab-120">INPUTS</span></span>

### <span data-ttu-id="d81ab-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d81ab-121">System.String</span></span>

## <span data-ttu-id="d81ab-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d81ab-122">OUTPUTS</span></span>

### <span data-ttu-id="d81ab-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d81ab-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d81ab-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d81ab-124">NOTES</span></span>

## <span data-ttu-id="d81ab-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d81ab-125">RELATED LINKS</span></span>

[<span data-ttu-id="d81ab-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d81ab-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="d81ab-127">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d81ab-127">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="d81ab-128">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d81ab-128">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="d81ab-129">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d81ab-129">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="d81ab-130">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d81ab-130">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


