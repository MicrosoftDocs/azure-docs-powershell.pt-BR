---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: ac58450295e0e2d988c12c308c0210b38ad71b4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609771"
---
# <span data-ttu-id="dee6f-101">Add-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dee6f-101">Add-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="dee6f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dee6f-102">SYNOPSIS</span></span>
<span data-ttu-id="dee6f-103">Adiciona uma definição de política de ponto de extremidade de serviço a uma política especificada.</span><span class="sxs-lookup"><span data-stu-id="dee6f-103">Adds a service endpoint policy definition to a specified policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dee6f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dee6f-104">SYNTAX</span></span>

```
Add-AzureRmServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <System.Collections.Generic.List`1[System.String]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dee6f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dee6f-105">DESCRIPTION</span></span>
<span data-ttu-id="dee6f-106">O cmdlet **Add-AzureRmServiceEndpointPolicyDefinition** adiciona uma definição de política de ponto de extremidade do serviço à política.</span><span class="sxs-lookup"><span data-stu-id="dee6f-106">The **Add-AzureRmServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="dee6f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dee6f-107">EXAMPLES</span></span>

### <span data-ttu-id="dee6f-108">Exemplo 1: atualiza uma definição de política de ponto de extremidade do serviço em uma política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="dee6f-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="dee6f-109">Este comando atualizou a definição da política de ponto de extremidade do serviço com o nome ServiceEndpointPolicyDefinition1, serviço Microsoft. Storage, assinaturas de recursos de serviço/Sub1 e descrição "New Definition" que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $policydef.</span><span class="sxs-lookup"><span data-stu-id="dee6f-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="dee6f-110">OS</span><span class="sxs-lookup"><span data-stu-id="dee6f-110">PARAMETERS</span></span>

### <span data-ttu-id="dee6f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dee6f-111">-DefaultProfile</span></span>
<span data-ttu-id="dee6f-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dee6f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dee6f-113">-Descrição</span><span class="sxs-lookup"><span data-stu-id="dee6f-113">-Description</span></span>
<span data-ttu-id="dee6f-114">A descrição da definição</span><span class="sxs-lookup"><span data-stu-id="dee6f-114">The description of the definition</span></span>

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

### <span data-ttu-id="dee6f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="dee6f-115">-Name</span></span>
<span data-ttu-id="dee6f-116">O nome da definição da política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="dee6f-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="dee6f-117">-Serviço</span><span class="sxs-lookup"><span data-stu-id="dee6f-117">-Service</span></span>
<span data-ttu-id="dee6f-118">Nome do serviço</span><span class="sxs-lookup"><span data-stu-id="dee6f-118">Name of the service</span></span>

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

### <span data-ttu-id="dee6f-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="dee6f-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="dee6f-120">O ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="dee6f-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="dee6f-121">-Recurso do recurso</span><span class="sxs-lookup"><span data-stu-id="dee6f-121">-ServiceResource</span></span>
<span data-ttu-id="dee6f-122">Lista de recursos de serviço</span><span class="sxs-lookup"><span data-stu-id="dee6f-122">List of service resources</span></span>

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

### <span data-ttu-id="dee6f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dee6f-123">CommonParameters</span></span>
<span data-ttu-id="dee6f-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dee6f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dee6f-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dee6f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dee6f-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dee6f-126">INPUTS</span></span>

### <span data-ttu-id="dee6f-127">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="dee6f-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="dee6f-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dee6f-128">OUTPUTS</span></span>

### <span data-ttu-id="dee6f-129">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="dee6f-129">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="dee6f-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dee6f-130">NOTES</span></span>

## <span data-ttu-id="dee6f-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dee6f-131">RELATED LINKS</span></span>
