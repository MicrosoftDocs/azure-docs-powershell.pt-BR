---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: ecd5a8eafc70a88b4ebda17a83f2b40139f5463f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602915"
---
# <span data-ttu-id="d4783-101">Set-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d4783-101">Set-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="d4783-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d4783-102">SYNOPSIS</span></span>
<span data-ttu-id="d4783-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="d4783-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4783-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d4783-104">SYNTAX</span></span>

```
Set-AzureRmServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4783-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d4783-105">DESCRIPTION</span></span>
<span data-ttu-id="d4783-106">O cmdlet **set-AzureRmServiceEndpointPolicy** cria uma política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="d4783-106">The **Set-AzureRmServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="d4783-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d4783-107">EXAMPLES</span></span>

### <span data-ttu-id="d4783-108">Exemplo 1: define uma política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="d4783-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzureRmServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="d4783-109">Esse comando atualiza uma política de ponto de extremidade de serviço chamada Policy1 definida pela $serviceEndpointPolicy do objeto pertencer ao o objeto de Resource "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="d4783-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="d4783-110">OS</span><span class="sxs-lookup"><span data-stu-id="d4783-110">PARAMETERS</span></span>

### <span data-ttu-id="d4783-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4783-111">-DefaultProfile</span></span>
<span data-ttu-id="d4783-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d4783-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4783-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d4783-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="d4783-114">O ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d4783-114">The ServiceEndpointPolicy</span></span>

```yaml
Type: PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4783-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4783-115">CommonParameters</span></span>
<span data-ttu-id="d4783-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4783-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d4783-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4783-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4783-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d4783-118">INPUTS</span></span>

### <span data-ttu-id="d4783-119">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d4783-119">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="d4783-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d4783-120">OUTPUTS</span></span>

### <span data-ttu-id="d4783-121">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d4783-121">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="d4783-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d4783-122">NOTES</span></span>

## <span data-ttu-id="d4783-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d4783-123">RELATED LINKS</span></span>
