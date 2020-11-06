---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 1348eff2e4a2ac755ac0f425ddb29816438199b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602914"
---
# <span data-ttu-id="5b41e-101">Set-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5b41e-101">Set-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="5b41e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b41e-102">SYNOPSIS</span></span>
<span data-ttu-id="5b41e-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="5b41e-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b41e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b41e-104">SYNTAX</span></span>

```
Set-AzureRmServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <System.Collections.Generic.List`1[System.String]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b41e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5b41e-105">DESCRIPTION</span></span>
<span data-ttu-id="5b41e-106">O cmdlet **set-AzureRmServiceEndpointPolicyDefinition** cria uma definição de política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="5b41e-106">The **Set-AzureRmServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="5b41e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5b41e-107">EXAMPLES</span></span>

### <span data-ttu-id="5b41e-108">Exemplo 1: atualiza uma definição de política de ponto de extremidade do serviço em uma política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="5b41e-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzureRmServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="5b41e-109">Esse comando atualiza uma definição de política de ponto de extremidade de serviço chamada Policydef1 na política de ponto de extremidade do serviço definida pela $ServiceEndpointPolicy do objeto.</span><span class="sxs-lookup"><span data-stu-id="5b41e-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="5b41e-110">OS</span><span class="sxs-lookup"><span data-stu-id="5b41e-110">PARAMETERS</span></span>

### <span data-ttu-id="5b41e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b41e-111">-DefaultProfile</span></span>
<span data-ttu-id="5b41e-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5b41e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b41e-113">-Descrição</span><span class="sxs-lookup"><span data-stu-id="5b41e-113">-Description</span></span>
<span data-ttu-id="5b41e-114">A descrição da definição</span><span class="sxs-lookup"><span data-stu-id="5b41e-114">The description of the definition</span></span>

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

### <span data-ttu-id="5b41e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b41e-115">-Name</span></span>
<span data-ttu-id="5b41e-116">O nome da regra</span><span class="sxs-lookup"><span data-stu-id="5b41e-116">The name of the rule</span></span>

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

### <span data-ttu-id="5b41e-117">-Serviço</span><span class="sxs-lookup"><span data-stu-id="5b41e-117">-Service</span></span>
<span data-ttu-id="5b41e-118">Nome do serviço</span><span class="sxs-lookup"><span data-stu-id="5b41e-118">Name of the service</span></span>

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

### <span data-ttu-id="5b41e-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5b41e-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="5b41e-120">O NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5b41e-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="5b41e-121">-Recurso do recurso</span><span class="sxs-lookup"><span data-stu-id="5b41e-121">-ServiceResource</span></span>
<span data-ttu-id="5b41e-122">Lista de recursos de serviço</span><span class="sxs-lookup"><span data-stu-id="5b41e-122">List of service resources</span></span>

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

### <span data-ttu-id="5b41e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b41e-123">CommonParameters</span></span>
<span data-ttu-id="5b41e-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b41e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5b41e-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b41e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b41e-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5b41e-126">INPUTS</span></span>

### <span data-ttu-id="5b41e-127">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5b41e-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="5b41e-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5b41e-128">OUTPUTS</span></span>

### <span data-ttu-id="5b41e-129">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5b41e-129">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="5b41e-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5b41e-130">NOTES</span></span>

## <span data-ttu-id="5b41e-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b41e-131">RELATED LINKS</span></span>
