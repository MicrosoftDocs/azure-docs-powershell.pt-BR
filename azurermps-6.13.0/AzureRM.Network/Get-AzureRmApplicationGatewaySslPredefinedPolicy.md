---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 82713c41d6f2e3882c50ffbd5ab6b276a90dc2e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432770"
---
# <span data-ttu-id="e192e-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="e192e-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="e192e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e192e-102">SYNOPSIS</span></span>
<span data-ttu-id="e192e-103">Obtém políticas SSL predefinidas fornecidas pelo Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e192e-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e192e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e192e-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e192e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e192e-105">DESCRIPTION</span></span>
<span data-ttu-id="e192e-106">O cmdlet **Get-AzureRmApplicationGatewaySslPredefinedPolicy** tem diretivas SSL predefinidas fornecidas pelo Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e192e-106">The **Get-AzureRmApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="e192e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e192e-107">EXAMPLES</span></span>

### <span data-ttu-id="e192e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e192e-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzureRmApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="e192e-109">Esses comandos retornam todas as políticas de SSL predefinidas.</span><span class="sxs-lookup"><span data-stu-id="e192e-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="e192e-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e192e-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzureRmApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="e192e-111">Esses comandos retornam uma política predefinida com o nome AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="e192e-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="e192e-112">OS</span><span class="sxs-lookup"><span data-stu-id="e192e-112">PARAMETERS</span></span>

### <span data-ttu-id="e192e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e192e-113">-DefaultProfile</span></span>
<span data-ttu-id="e192e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e192e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e192e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e192e-115">-Name</span></span>
<span data-ttu-id="e192e-116">Nome da política predefinida SSL</span><span class="sxs-lookup"><span data-stu-id="e192e-116">Name of the ssl predefined policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e192e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e192e-117">CommonParameters</span></span>
<span data-ttu-id="e192e-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e192e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e192e-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e192e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e192e-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e192e-120">INPUTS</span></span>

### <span data-ttu-id="e192e-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e192e-121">None</span></span>

## <span data-ttu-id="e192e-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e192e-122">OUTPUTS</span></span>

### <span data-ttu-id="e192e-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="e192e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="e192e-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e192e-124">NOTES</span></span>

## <span data-ttu-id="e192e-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e192e-125">RELATED LINKS</span></span>