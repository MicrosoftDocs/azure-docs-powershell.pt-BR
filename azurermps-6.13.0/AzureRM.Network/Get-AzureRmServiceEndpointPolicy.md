---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 989b6aa91c0dabec1b72425f214c4097df374041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428476"
---
# <span data-ttu-id="2a199-101">Get-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2a199-101">Get-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="2a199-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a199-102">SYNOPSIS</span></span>
<span data-ttu-id="2a199-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="2a199-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a199-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a199-104">SYNTAX</span></span>

```
Get-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a199-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a199-105">DESCRIPTION</span></span>
<span data-ttu-id="2a199-106">O cmdlet **Get-AzureRmServiceEndpointPolicy** Obtém uma política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="2a199-106">The **Get-AzureRmServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="2a199-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a199-107">EXAMPLES</span></span>

### <span data-ttu-id="2a199-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2a199-108">Example 1</span></span>
```
$policy = Get-AzureRmServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2a199-109">Esse comando obtém a política de ponto de extremidade do serviço chamada ServiceEndpointPolicy1 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $policy.</span><span class="sxs-lookup"><span data-stu-id="2a199-109">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="2a199-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2a199-110">Example 2</span></span>
```
$policyList = Get-AzureRmServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2a199-111">Esse comando obtém uma lista de todas as políticas de ponto de extremidade do serviço no grupo de recursos chamado ResourceGroup01 e as armazena na variável $policyList.</span><span class="sxs-lookup"><span data-stu-id="2a199-111">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

## <span data-ttu-id="2a199-112">OS</span><span class="sxs-lookup"><span data-stu-id="2a199-112">PARAMETERS</span></span>

### <span data-ttu-id="2a199-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a199-113">-DefaultProfile</span></span>
<span data-ttu-id="2a199-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a199-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a199-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a199-115">-Name</span></span>
<span data-ttu-id="2a199-116">O nome da política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="2a199-116">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a199-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a199-117">-ResourceGroupName</span></span>
<span data-ttu-id="2a199-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2a199-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a199-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a199-119">CommonParameters</span></span>
<span data-ttu-id="2a199-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a199-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2a199-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a199-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a199-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a199-122">INPUTS</span></span>

### <span data-ttu-id="2a199-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2a199-123">System.String</span></span>


## <span data-ttu-id="2a199-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a199-124">OUTPUTS</span></span>

### <span data-ttu-id="2a199-125">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2a199-125">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="2a199-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a199-126">NOTES</span></span>

## <span data-ttu-id="2a199-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a199-127">RELATED LINKS</span></span>
