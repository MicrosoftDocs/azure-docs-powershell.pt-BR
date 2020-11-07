---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablessloptions
schema: 2.0.0
ms.openlocfilehash: 023b2a43114fe47b50956e7f4626a75706e914f5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785731"
---
# <span data-ttu-id="6b565-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="6b565-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="6b565-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b565-102">SYNOPSIS</span></span>
<span data-ttu-id="6b565-103">Obtém todas as opções de SSL disponíveis para a política SSL do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="6b565-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b565-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b565-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableSslOptions [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b565-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b565-105">DESCRIPTION</span></span>
<span data-ttu-id="6b565-106">O cmdlet **Get-AzureRmApplicationGatewayAvailableSslOptions** obtém todas as opções SSL disponíveis para a política SSL</span><span class="sxs-lookup"><span data-stu-id="6b565-106">The **Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="6b565-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b565-107">EXAMPLES</span></span>

### <span data-ttu-id="6b565-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6b565-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzureRmApplicationGatewayAvailableSslOptions
```

<span data-ttu-id="6b565-109">Esses comandos retornam todas as opções SSL disponíveis para a política SSL.</span><span class="sxs-lookup"><span data-stu-id="6b565-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="6b565-110">OS</span><span class="sxs-lookup"><span data-stu-id="6b565-110">PARAMETERS</span></span>

### <span data-ttu-id="6b565-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b565-111">-DefaultProfile</span></span>
<span data-ttu-id="6b565-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6b565-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b565-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b565-113">CommonParameters</span></span>
<span data-ttu-id="6b565-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b565-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b565-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b565-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b565-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b565-116">INPUTS</span></span>

### <span data-ttu-id="6b565-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6b565-117">None</span></span>

## <span data-ttu-id="6b565-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b565-118">OUTPUTS</span></span>

### <span data-ttu-id="6b565-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="6b565-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="6b565-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b565-120">NOTES</span></span>

## <span data-ttu-id="6b565-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b565-121">RELATED LINKS</span></span>

