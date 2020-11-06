---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurerminterfaceendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmInterfaceEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmInterfaceEndpoint.md
ms.openlocfilehash: 8759546c9d7161f2bea139845c7d291c6d7832b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430177"
---
# <span data-ttu-id="b03dc-101">Get-AzureRmInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b03dc-101">Get-AzureRmInterfaceEndpoint</span></span>

## <span data-ttu-id="b03dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b03dc-102">SYNOPSIS</span></span>
<span data-ttu-id="b03dc-103">O cmdlet Get-AzureRmInterfaceEndpoint Obtém um ponto de extremidade de interface.</span><span class="sxs-lookup"><span data-stu-id="b03dc-103">The Get-AzureRmInterfaceEndpoint cmdlet gets a Interface Endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b03dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b03dc-104">SYNTAX</span></span>

### <span data-ttu-id="b03dc-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b03dc-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmInterfaceEndpoint [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b03dc-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b03dc-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmInterfaceEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b03dc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b03dc-107">DESCRIPTION</span></span>
<span data-ttu-id="b03dc-108">O cmdlet **Get-AzureRmInterfaceEndpoint** Obtém um ponto de extremidade de interface.</span><span class="sxs-lookup"><span data-stu-id="b03dc-108">The **Get-AzureRmInterfaceEndpoint** cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="b03dc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b03dc-109">EXAMPLES</span></span>

### <span data-ttu-id="b03dc-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b03dc-110">Example 1</span></span>
```
$interfaceendpoint = Get-AzureRmInterfaceEndpoint -Name "InterfaceEndpoint1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b03dc-111">Esse comando obtém o ponto de extremidade da interface chamado InterfaceEndpoint1 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $interfaceendpoint.</span><span class="sxs-lookup"><span data-stu-id="b03dc-111">This command gets the interface endpoint named InterfaceEndpoint1 that belongs to the resource group named ResourceGroup01 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="b03dc-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b03dc-112">Example 2</span></span>
```
$interfaceendpoint = Get-AzureRmInterfaceEndpoint -ResourceId "/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10"

```

<span data-ttu-id="b03dc-113">Esse comando obtém o ponto de extremidade da interface com ResourceId/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 e o armazena na variável $interfaceendpoint.</span><span class="sxs-lookup"><span data-stu-id="b03dc-113">This command gets the interface endpoint with resourceId  /subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 and stores it in the $interfaceendpoint variable.</span></span>


## <span data-ttu-id="b03dc-114">OS</span><span class="sxs-lookup"><span data-stu-id="b03dc-114">PARAMETERS</span></span>

### <span data-ttu-id="b03dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b03dc-115">-DefaultProfile</span></span>
<span data-ttu-id="b03dc-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b03dc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b03dc-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b03dc-117">-Name</span></span>
<span data-ttu-id="b03dc-118">O nome do ponto de extremidade da interface</span><span class="sxs-lookup"><span data-stu-id="b03dc-118">The name of the interface endpoint</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03dc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b03dc-119">-ResourceGroupName</span></span>
<span data-ttu-id="b03dc-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b03dc-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b03dc-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b03dc-121">-ResourceId</span></span>
<span data-ttu-id="b03dc-122">{{Descrição do ResourceId}}</span><span class="sxs-lookup"><span data-stu-id="b03dc-122">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b03dc-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b03dc-123">-Confirm</span></span>
<span data-ttu-id="b03dc-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b03dc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b03dc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b03dc-125">-WhatIf</span></span>
<span data-ttu-id="b03dc-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b03dc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b03dc-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b03dc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b03dc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b03dc-128">CommonParameters</span></span>
<span data-ttu-id="b03dc-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b03dc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b03dc-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b03dc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b03dc-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b03dc-131">INPUTS</span></span>

### <span data-ttu-id="b03dc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b03dc-132">System.String</span></span>


## <span data-ttu-id="b03dc-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b03dc-133">OUTPUTS</span></span>

### <span data-ttu-id="b03dc-134">Microsoft. Azure. Commands. Network. Models. PSInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b03dc-134">Microsoft.Azure.Commands.Network.Models.PSInterfaceEndpoint</span></span>


## <span data-ttu-id="b03dc-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b03dc-135">NOTES</span></span>

## <span data-ttu-id="b03dc-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b03dc-136">RELATED LINKS</span></span>
