---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 12d809ad4c1df021891ab5acf384415d64aa08a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433199"
---
# <span data-ttu-id="f8b7f-101">New-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f8b7f-101">New-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="f8b7f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8b7f-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b7f-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="f8b7f-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8b7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8b7f-104">SYNTAX</span></span>

```
New-AzureRmServiceEndpointPolicyDefinition -Name <String> [-Description <String>]
 [-ServiceResource <System.Collections.Generic.List`1[System.String]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8b7f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f8b7f-105">DESCRIPTION</span></span>
<span data-ttu-id="f8b7f-106">O cmdlet **New-AzureRmServiceEndpointPolicyDefinition** cria uma definição de política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="f8b7f-106">The **New-AzureRmServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="f8b7f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f8b7f-107">EXAMPLES</span></span>

### <span data-ttu-id="f8b7f-108">Exemplo 1: cria uma política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="f8b7f-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="f8b7f-109">Esse comando cria a definição da política de ponto de extremidade do serviço com o nome ServiceEndpointPolicyDefinition1, serviço Microsoft. Storage, assinaturas de recursos de serviço/Sub1 e descrição "New Definition" que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $policydef.</span><span class="sxs-lookup"><span data-stu-id="f8b7f-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="f8b7f-110">OS</span><span class="sxs-lookup"><span data-stu-id="f8b7f-110">PARAMETERS</span></span>

### <span data-ttu-id="f8b7f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b7f-111">-DefaultProfile</span></span>
<span data-ttu-id="f8b7f-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f8b7f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8b7f-113">-Descrição</span><span class="sxs-lookup"><span data-stu-id="f8b7f-113">-Description</span></span>
<span data-ttu-id="f8b7f-114">A descrição da definição</span><span class="sxs-lookup"><span data-stu-id="f8b7f-114">The description of the definition</span></span>

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

### <span data-ttu-id="f8b7f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8b7f-115">-Name</span></span>
<span data-ttu-id="f8b7f-116">O nome da política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="f8b7f-116">The name of the service endpoint policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8b7f-117">-Serviço</span><span class="sxs-lookup"><span data-stu-id="f8b7f-117">-Service</span></span>
<span data-ttu-id="f8b7f-118">Nome do serviço</span><span class="sxs-lookup"><span data-stu-id="f8b7f-118">Name of the service</span></span>

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

### <span data-ttu-id="f8b7f-119">-Recurso do recurso</span><span class="sxs-lookup"><span data-stu-id="f8b7f-119">-ServiceResource</span></span>
<span data-ttu-id="f8b7f-120">Lista de recursos de serviço</span><span class="sxs-lookup"><span data-stu-id="f8b7f-120">List of service resources</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8b7f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b7f-121">CommonParameters</span></span>
<span data-ttu-id="f8b7f-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8b7f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f8b7f-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8b7f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b7f-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f8b7f-124">INPUTS</span></span>

### <span data-ttu-id="f8b7f-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f8b7f-125">None</span></span>


## <span data-ttu-id="f8b7f-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f8b7f-126">OUTPUTS</span></span>

### <span data-ttu-id="f8b7f-127">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f8b7f-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>


## <span data-ttu-id="f8b7f-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f8b7f-128">NOTES</span></span>

## <span data-ttu-id="f8b7f-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8b7f-129">RELATED LINKS</span></span>
