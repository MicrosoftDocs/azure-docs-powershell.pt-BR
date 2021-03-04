---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: 8d2022f79dff5263f07737d525169dad3566fcda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892107"
---
# <span data-ttu-id="b5a5c-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="b5a5c-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="b5a5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5a5c-102">SYNOPSIS</span></span>
<span data-ttu-id="b5a5c-103">Obtém todas as opções de ssl disponíveis para a política ssl do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b5a5c-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="b5a5c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b5a5c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5a5c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b5a5c-105">DESCRIPTION</span></span>
<span data-ttu-id="b5a5c-106">O cmdlet **Get-AzApplicationGatewayAvailableSslOption** obtém todas as opções ssl disponíveis para a política ssl</span><span class="sxs-lookup"><span data-stu-id="b5a5c-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="b5a5c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b5a5c-107">EXAMPLES</span></span>

### <span data-ttu-id="b5a5c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b5a5c-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="b5a5c-109">Esses comandos retornam todas as opções de ssl disponíveis para a política ssl.</span><span class="sxs-lookup"><span data-stu-id="b5a5c-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="b5a5c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b5a5c-110">PARAMETERS</span></span>

### <span data-ttu-id="b5a5c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5a5c-111">-DefaultProfile</span></span>
<span data-ttu-id="b5a5c-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b5a5c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5a5c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5a5c-113">CommonParameters</span></span>
<span data-ttu-id="b5a5c-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5a5c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5a5c-115">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5a5c-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5a5c-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5a5c-116">INPUTS</span></span>

### <span data-ttu-id="b5a5c-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b5a5c-117">None</span></span>

## <span data-ttu-id="b5a5c-118">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b5a5c-118">OUTPUTS</span></span>

### <span data-ttu-id="b5a5c-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="b5a5c-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="b5a5c-120">NOTES</span><span class="sxs-lookup"><span data-stu-id="b5a5c-120">NOTES</span></span>

## <span data-ttu-id="b5a5c-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5a5c-121">RELATED LINKS</span></span>
