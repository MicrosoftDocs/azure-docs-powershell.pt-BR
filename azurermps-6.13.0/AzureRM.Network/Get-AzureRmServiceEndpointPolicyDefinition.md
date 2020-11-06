---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 547b38fd30f09a305c63054b2f27d33db5ae6a86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432761"
---
# <span data-ttu-id="e378d-101">Get-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e378d-101">Get-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="e378d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e378d-102">SYNOPSIS</span></span>
<span data-ttu-id="e378d-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="e378d-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e378d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e378d-104">SYNTAX</span></span>

```
Get-AzureRmServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e378d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e378d-105">DESCRIPTION</span></span>
<span data-ttu-id="e378d-106">O cmdlet **Get-AzureRmServiceEndpointPolicyDefinition** Obtém uma definição de política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="e378d-106">The **Get-AzureRmServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="e378d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e378d-107">EXAMPLES</span></span>

### <span data-ttu-id="e378d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e378d-108">Example 1</span></span>
```
$policydef= Get-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="e378d-109">Esse comando obtém a definição da política de ponto de extremidade do serviço chamada ServiceEndpointPolicyDefinition1 em ServiceEndpointPolicy $Policy a armazena na variável $policydef.</span><span class="sxs-lookup"><span data-stu-id="e378d-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="e378d-110">OS</span><span class="sxs-lookup"><span data-stu-id="e378d-110">PARAMETERS</span></span>

### <span data-ttu-id="e378d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e378d-111">-DefaultProfile</span></span>
<span data-ttu-id="e378d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e378d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e378d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="e378d-113">-Name</span></span>
<span data-ttu-id="e378d-114">O nome da definição da política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="e378d-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="e378d-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e378d-115">-ResourceId</span></span>
<span data-ttu-id="e378d-116">{{Descrição do ResourceId}}</span><span class="sxs-lookup"><span data-stu-id="e378d-116">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e378d-117">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e378d-117">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="e378d-118">Política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="e378d-118">The Service endpoint policy</span></span>

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

### <span data-ttu-id="e378d-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e378d-119">-Confirm</span></span>
<span data-ttu-id="e378d-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e378d-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e378d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e378d-121">-WhatIf</span></span>
<span data-ttu-id="e378d-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e378d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e378d-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e378d-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e378d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e378d-124">CommonParameters</span></span>
<span data-ttu-id="e378d-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e378d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e378d-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e378d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e378d-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e378d-127">INPUTS</span></span>

### <span data-ttu-id="e378d-128">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e378d-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="e378d-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e378d-129">OUTPUTS</span></span>

### <span data-ttu-id="e378d-130">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e378d-130">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="e378d-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e378d-131">NOTES</span></span>

## <span data-ttu-id="e378d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e378d-132">RELATED LINKS</span></span>
