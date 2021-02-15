---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: f2175583aaaf3af04120e22e32db79d7b20f1e30
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114187"
---
# <span data-ttu-id="061e6-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="061e6-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="061e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="061e6-102">SYNOPSIS</span></span>
<span data-ttu-id="061e6-103">Obtém todas as opções de SSL disponíveis para a política SSL do Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="061e6-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="061e6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="061e6-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="061e6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="061e6-105">DESCRIPTION</span></span>
<span data-ttu-id="061e6-106">O cmdlet **Get-AzApplicationGatewayAvailableSslOption** obtém todas as opções de ssl disponíveis para a política ssl</span><span class="sxs-lookup"><span data-stu-id="061e6-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="061e6-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="061e6-107">EXAMPLES</span></span>

### <span data-ttu-id="061e6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="061e6-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="061e6-109">Esses comandos retornam todas as opções de SSL disponíveis para a política SSL.</span><span class="sxs-lookup"><span data-stu-id="061e6-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="061e6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="061e6-110">PARAMETERS</span></span>

### <span data-ttu-id="061e6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="061e6-111">-DefaultProfile</span></span>
<span data-ttu-id="061e6-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="061e6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="061e6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="061e6-113">CommonParameters</span></span>
<span data-ttu-id="061e6-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="061e6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="061e6-115">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="061e6-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="061e6-116">Entradas</span><span class="sxs-lookup"><span data-stu-id="061e6-116">INPUTS</span></span>

### <span data-ttu-id="061e6-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="061e6-117">None</span></span>

## <span data-ttu-id="061e6-118">Saídas</span><span class="sxs-lookup"><span data-stu-id="061e6-118">OUTPUTS</span></span>

### <span data-ttu-id="061e6-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="061e6-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="061e6-120">Notas</span><span class="sxs-lookup"><span data-stu-id="061e6-120">NOTES</span></span>

## <span data-ttu-id="061e6-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="061e6-121">RELATED LINKS</span></span>
