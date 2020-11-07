---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: 04a24ee5148782f4a15aa5b93ffb937ad312ccfb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772068"
---
# <span data-ttu-id="fd549-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="fd549-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="fd549-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd549-102">SYNOPSIS</span></span>
<span data-ttu-id="fd549-103">Obtém todas as opções de SSL disponíveis para a política SSL do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="fd549-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="fd549-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd549-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd549-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fd549-105">DESCRIPTION</span></span>
<span data-ttu-id="fd549-106">O cmdlet **Get-AzApplicationGatewayAvailableSslOption** obtém todas as opções SSL disponíveis para a política SSL</span><span class="sxs-lookup"><span data-stu-id="fd549-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="fd549-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd549-107">EXAMPLES</span></span>

### <span data-ttu-id="fd549-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fd549-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="fd549-109">Esses comandos retornam todas as opções SSL disponíveis para a política SSL.</span><span class="sxs-lookup"><span data-stu-id="fd549-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="fd549-110">OS</span><span class="sxs-lookup"><span data-stu-id="fd549-110">PARAMETERS</span></span>

### <span data-ttu-id="fd549-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd549-111">-DefaultProfile</span></span>
<span data-ttu-id="fd549-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd549-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd549-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd549-113">CommonParameters</span></span>
<span data-ttu-id="fd549-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd549-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd549-115">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd549-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd549-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fd549-116">INPUTS</span></span>

### <span data-ttu-id="fd549-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fd549-117">None</span></span>

## <span data-ttu-id="fd549-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fd549-118">OUTPUTS</span></span>

### <span data-ttu-id="fd549-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="fd549-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="fd549-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fd549-120">NOTES</span></span>

## <span data-ttu-id="fd549-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd549-121">RELATED LINKS</span></span>
