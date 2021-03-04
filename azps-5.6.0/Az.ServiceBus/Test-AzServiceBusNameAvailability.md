---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: b97acb269ee38dc937c5deffb0b3e054b0222c4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886582"
---
# <span data-ttu-id="d62ad-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="d62ad-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="d62ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d62ad-102">SYNOPSIS</span></span>
<span data-ttu-id="d62ad-103">Verifica a disponibilidade do nome da fila ou tópico determinado</span><span class="sxs-lookup"><span data-stu-id="d62ad-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="d62ad-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d62ad-104">SYNTAX</span></span>

### <span data-ttu-id="d62ad-105">QueueCheckNameAvailabilitySet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d62ad-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d62ad-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d62ad-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d62ad-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d62ad-107">DESCRIPTION</span></span>
<span data-ttu-id="d62ad-108">O **Cmdlet Test-AzServiceBusNameAvailability** Check Availability of the provided Name of Queue or Topic</span><span class="sxs-lookup"><span data-stu-id="d62ad-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="d62ad-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d62ad-109">EXAMPLES</span></span>

### <span data-ttu-id="d62ad-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d62ad-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="d62ad-111">Retorna True se o nome $nameQueue for Availabile ou retornar False se for fornecido $nameQueue nome em não disponível</span><span class="sxs-lookup"><span data-stu-id="d62ad-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="d62ad-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d62ad-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="d62ad-113">Retorna True se o nome $nameTopic for Availabile ou retornar False se o nome $nameTopic fornecido não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="d62ad-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="d62ad-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d62ad-114">PARAMETERS</span></span>

### <span data-ttu-id="d62ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d62ad-115">-DefaultProfile</span></span>
<span data-ttu-id="d62ad-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d62ad-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d62ad-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d62ad-117">-Name</span></span>
<span data-ttu-id="d62ad-118">Nome da Fila para verificar a Disponibilidade de Nome</span><span class="sxs-lookup"><span data-stu-id="d62ad-118">Queue Name to check the Name Availability</span></span>

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

### <span data-ttu-id="d62ad-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d62ad-119">-Namespace</span></span>
<span data-ttu-id="d62ad-120">Nome do Namespace servicebus</span><span class="sxs-lookup"><span data-stu-id="d62ad-120">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="d62ad-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="d62ad-121">-Queue</span></span>
<span data-ttu-id="d62ad-122">Para verificar a disponibilidade de nome para o nome da fila</span><span class="sxs-lookup"><span data-stu-id="d62ad-122">To Check Name Availability for Queue Name</span></span>

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

### <span data-ttu-id="d62ad-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d62ad-123">-ResourceGroupName</span></span>
<span data-ttu-id="d62ad-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d62ad-124">Resource Group Name</span></span>

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

### <span data-ttu-id="d62ad-125">-Topic</span><span class="sxs-lookup"><span data-stu-id="d62ad-125">-Topic</span></span>
<span data-ttu-id="d62ad-126">Para verificar a disponibilidade de nome para o nome do tópico</span><span class="sxs-lookup"><span data-stu-id="d62ad-126">To Check Name Availability for Topic Name</span></span>

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

### <span data-ttu-id="d62ad-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d62ad-127">CommonParameters</span></span>
<span data-ttu-id="d62ad-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d62ad-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d62ad-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d62ad-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d62ad-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d62ad-130">INPUTS</span></span>

### <span data-ttu-id="d62ad-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d62ad-131">System.String</span></span>

## <span data-ttu-id="d62ad-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d62ad-132">OUTPUTS</span></span>

### <span data-ttu-id="d62ad-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d62ad-133">System.Boolean</span></span>

## <span data-ttu-id="d62ad-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="d62ad-134">NOTES</span></span>

## <span data-ttu-id="d62ad-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d62ad-135">RELATED LINKS</span></span>
