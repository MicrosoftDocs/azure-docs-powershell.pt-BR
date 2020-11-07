---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: adaf7485b0af16821a1f4adec7919422bef07f90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940882"
---
# <span data-ttu-id="1f36e-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="1f36e-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="1f36e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f36e-102">SYNOPSIS</span></span>
<span data-ttu-id="1f36e-103">Verifica a disponibilidade da determinada fila ou nome do tópico</span><span class="sxs-lookup"><span data-stu-id="1f36e-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="1f36e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f36e-104">SYNTAX</span></span>

### <span data-ttu-id="1f36e-105">QueueCheckNameAvailabilitySet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1f36e-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f36e-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1f36e-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f36e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f36e-107">DESCRIPTION</span></span>
<span data-ttu-id="1f36e-108">O cmdlet **Test-AzServiceBusNameAvailability** verifica a disponibilidade do nome fornecido da fila ou tópico</span><span class="sxs-lookup"><span data-stu-id="1f36e-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="1f36e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f36e-109">EXAMPLES</span></span>

### <span data-ttu-id="1f36e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1f36e-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="1f36e-111">Retorna true se o nome $nameQueue fornecido for Availabile ou retornará false se fornecido $nameQueue nome não disponível</span><span class="sxs-lookup"><span data-stu-id="1f36e-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="1f36e-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1f36e-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="1f36e-113">Retorna true se o nome $nameTopic fornecido for Availabile ou retornará false se fornecido $nameTopic nome não disponível</span><span class="sxs-lookup"><span data-stu-id="1f36e-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="1f36e-114">OS</span><span class="sxs-lookup"><span data-stu-id="1f36e-114">PARAMETERS</span></span>

### <span data-ttu-id="1f36e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f36e-115">-DefaultProfile</span></span>
<span data-ttu-id="1f36e-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f36e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f36e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f36e-117">-Name</span></span>
<span data-ttu-id="1f36e-118">Nome da fila para verificar a disponibilidade do nome</span><span class="sxs-lookup"><span data-stu-id="1f36e-118">Queue Name to check the Name Availability</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f36e-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1f36e-119">-Namespace</span></span>
<span data-ttu-id="1f36e-120">Nome do namespace do ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1f36e-120">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f36e-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="1f36e-121">-Queue</span></span>
<span data-ttu-id="1f36e-122">Para verificar a disponibilidade do nome do nome da fila</span><span class="sxs-lookup"><span data-stu-id="1f36e-122">To Check Name Availability for Queue Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: QueueCheckNameAvailabilitySet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f36e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f36e-123">-ResourceGroupName</span></span>
<span data-ttu-id="1f36e-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1f36e-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f36e-125">-Tópico</span><span class="sxs-lookup"><span data-stu-id="1f36e-125">-Topic</span></span>
<span data-ttu-id="1f36e-126">Para verificar a disponibilidade do nome para o nome do tópico</span><span class="sxs-lookup"><span data-stu-id="1f36e-126">To Check Name Availability for Topic Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TopicCheckNameAvailabilitySet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f36e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f36e-127">CommonParameters</span></span>
<span data-ttu-id="1f36e-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f36e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1f36e-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f36e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f36e-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f36e-130">INPUTS</span></span>

### <span data-ttu-id="1f36e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1f36e-131">System.String</span></span>

## <span data-ttu-id="1f36e-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f36e-132">OUTPUTS</span></span>

### <span data-ttu-id="1f36e-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1f36e-133">System.Boolean</span></span>

## <span data-ttu-id="1f36e-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f36e-134">NOTES</span></span>

## <span data-ttu-id="1f36e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f36e-135">RELATED LINKS</span></span>
