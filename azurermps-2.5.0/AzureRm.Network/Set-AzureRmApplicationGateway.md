---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 1b852be30b513963f5d311940162078bdf6f692a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786398"
---
# <span data-ttu-id="22b72-101">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22b72-101">Set-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="22b72-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22b72-102">SYNOPSIS</span></span>
<span data-ttu-id="22b72-103">Atualiza um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22b72-103">Updates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22b72-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22b72-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22b72-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22b72-105">DESCRIPTION</span></span>
<span data-ttu-id="22b72-106">O cmdlet **set-AzureRmApplicationGateway** atualiza um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="22b72-106">The **Set-AzureRmApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="22b72-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22b72-107">EXAMPLES</span></span>

### <span data-ttu-id="22b72-108">Exemplo 1: atualizar um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="22b72-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="22b72-109">Esse comando atualiza o gateway do aplicativo com configurações na variável $AppGw e armazena o gateway atualizado na variável $UpdatedAppGw.</span><span class="sxs-lookup"><span data-stu-id="22b72-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="22b72-110">OS</span><span class="sxs-lookup"><span data-stu-id="22b72-110">PARAMETERS</span></span>

### <span data-ttu-id="22b72-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22b72-111">-ApplicationGateway</span></span>
<span data-ttu-id="22b72-112">Especifica um objeto do aplicativo gateway que representa o estado para o qual o gateway do aplicativo deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="22b72-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="22b72-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22b72-113">-AsJob</span></span>
<span data-ttu-id="22b72-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="22b72-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22b72-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b72-115">-DefaultProfile</span></span>
<span data-ttu-id="22b72-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="22b72-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22b72-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b72-117">CommonParameters</span></span>
<span data-ttu-id="22b72-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22b72-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b72-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22b72-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b72-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22b72-120">INPUTS</span></span>

### <span data-ttu-id="22b72-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22b72-121">PSApplicationGateway</span></span>
<span data-ttu-id="22b72-122">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="22b72-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="22b72-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22b72-123">OUTPUTS</span></span>

### <span data-ttu-id="22b72-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22b72-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="22b72-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22b72-125">NOTES</span></span>

## <span data-ttu-id="22b72-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22b72-126">RELATED LINKS</span></span>

[<span data-ttu-id="22b72-127">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22b72-127">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


