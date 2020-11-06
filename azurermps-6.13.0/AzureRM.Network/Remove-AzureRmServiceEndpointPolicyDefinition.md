---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 3d406bf0dffb0ee250e1494fc05727d0a4c983ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440335"
---
# <span data-ttu-id="2e8d2-101">Remove-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2e8d2-101">Remove-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="2e8d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e8d2-102">SYNOPSIS</span></span>
<span data-ttu-id="2e8d2-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="2e8d2-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e8d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e8d2-104">SYNTAX</span></span>

```
Remove-AzureRmServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e8d2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e8d2-105">DESCRIPTION</span></span>
<span data-ttu-id="2e8d2-106">O cmdlet **Remove-AzureRmServiceEndpointPolicy** remove uma política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="2e8d2-106">The **Remove-AzureRmServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="2e8d2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e8d2-107">EXAMPLES</span></span>

### <span data-ttu-id="2e8d2-108">Exemplo 1: Remove uma política de ponto de extremidade do serviço usando Name</span><span class="sxs-lookup"><span data-stu-id="2e8d2-108">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzureRmServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="2e8d2-109">Esse comando Remove uma política de ponto de extremidade de serviço com o nome PolicyDef1</span><span class="sxs-lookup"><span data-stu-id="2e8d2-109">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="2e8d2-110">OS</span><span class="sxs-lookup"><span data-stu-id="2e8d2-110">PARAMETERS</span></span>

### <span data-ttu-id="2e8d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e8d2-111">-DefaultProfile</span></span>
<span data-ttu-id="2e8d2-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e8d2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e8d2-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e8d2-113">-Name</span></span>
<span data-ttu-id="2e8d2-114">O nome da definição de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="2e8d2-114">The name of the service endpoint definition</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e8d2-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2e8d2-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="2e8d2-116">O ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2e8d2-116">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="2e8d2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e8d2-117">CommonParameters</span></span>
<span data-ttu-id="2e8d2-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e8d2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2e8d2-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e8d2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e8d2-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e8d2-120">INPUTS</span></span>

### <span data-ttu-id="2e8d2-121">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2e8d2-121">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="2e8d2-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e8d2-122">OUTPUTS</span></span>

### <span data-ttu-id="2e8d2-123">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2e8d2-123">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="2e8d2-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e8d2-124">NOTES</span></span>

## <span data-ttu-id="2e8d2-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e8d2-125">RELATED LINKS</span></span>
