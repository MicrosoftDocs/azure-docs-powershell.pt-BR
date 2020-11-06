---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
ms.openlocfilehash: 60e380ffd046c61abb218395a838c6e0d5d785f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427878"
---
# <span data-ttu-id="2ffaf-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="2ffaf-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="2ffaf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2ffaf-102">SYNOPSIS</span></span>
<span data-ttu-id="2ffaf-103">Obtém todas as opções de SSL disponíveis para a política SSL do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="2ffaf-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ffaf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ffaf-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableSslOptions [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ffaf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2ffaf-105">DESCRIPTION</span></span>
<span data-ttu-id="2ffaf-106">O cmdlet **Get-AzureRmApplicationGatewayAvailableSslOptions** obtém todas as opções SSL disponíveis para a política SSL</span><span class="sxs-lookup"><span data-stu-id="2ffaf-106">The **Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="2ffaf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ffaf-107">EXAMPLES</span></span>

### <span data-ttu-id="2ffaf-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2ffaf-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzureRmApplicationGatewayAvailableSslOptions
```

<span data-ttu-id="2ffaf-109">Esses comandos retornam todas as opções SSL disponíveis para a política SSL.</span><span class="sxs-lookup"><span data-stu-id="2ffaf-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="2ffaf-110">OS</span><span class="sxs-lookup"><span data-stu-id="2ffaf-110">PARAMETERS</span></span>

### <span data-ttu-id="2ffaf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ffaf-111">-DefaultProfile</span></span>
<span data-ttu-id="2ffaf-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2ffaf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ffaf-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ffaf-113">CommonParameters</span></span>
<span data-ttu-id="2ffaf-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ffaf-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ffaf-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ffaf-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ffaf-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2ffaf-116">INPUTS</span></span>

### <span data-ttu-id="2ffaf-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2ffaf-117">None</span></span>

## <span data-ttu-id="2ffaf-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2ffaf-118">OUTPUTS</span></span>

### <span data-ttu-id="2ffaf-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="2ffaf-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="2ffaf-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2ffaf-120">NOTES</span></span>

## <span data-ttu-id="2ffaf-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ffaf-121">RELATED LINKS</span></span>

