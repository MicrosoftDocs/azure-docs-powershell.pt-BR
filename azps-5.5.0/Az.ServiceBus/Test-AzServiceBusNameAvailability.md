---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: adaf7485b0af16821a1f4adec7919422bef07f90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116384"
---
# <span data-ttu-id="21066-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="21066-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="21066-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21066-102">SYNOPSIS</span></span>
<span data-ttu-id="21066-103">Verifica a Disponibilidade do nome de tópico ou fila determinado</span><span class="sxs-lookup"><span data-stu-id="21066-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="21066-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21066-104">SYNTAX</span></span>

### <span data-ttu-id="21066-105">QueueCheckNameAvailabilitySet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="21066-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21066-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="21066-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21066-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="21066-107">DESCRIPTION</span></span>
<span data-ttu-id="21066-108">O **Cmdlet test-AzServiceBusNameAvailability** Check Availability of the provided Name of Queue or Topic</span><span class="sxs-lookup"><span data-stu-id="21066-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="21066-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="21066-109">EXAMPLES</span></span>

### <span data-ttu-id="21066-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="21066-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="21066-111">Retornará True se o nome $nameQueue fornecido for Availabile ou retornar Falso se o nome $nameQueue fornecido não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="21066-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="21066-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="21066-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="21066-113">Retornará True se o nome $nameTopic fornecido for Availabile ou retornar Falso se o nome $nameTopic fornecido não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="21066-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="21066-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21066-114">PARAMETERS</span></span>

### <span data-ttu-id="21066-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21066-115">-DefaultProfile</span></span>
<span data-ttu-id="21066-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="21066-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21066-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="21066-117">-Name</span></span>
<span data-ttu-id="21066-118">Nome da Fila para verificar a Disponibilidade do Nome</span><span class="sxs-lookup"><span data-stu-id="21066-118">Queue Name to check the Name Availability</span></span>

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

### <span data-ttu-id="21066-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="21066-119">-Namespace</span></span>
<span data-ttu-id="21066-120">Nome do Namespace do Servicebus</span><span class="sxs-lookup"><span data-stu-id="21066-120">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="21066-121">-Fila</span><span class="sxs-lookup"><span data-stu-id="21066-121">-Queue</span></span>
<span data-ttu-id="21066-122">Para verificar a disponibilidade do nome do nome da fila</span><span class="sxs-lookup"><span data-stu-id="21066-122">To Check Name Availability for Queue Name</span></span>

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

### <span data-ttu-id="21066-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21066-123">-ResourceGroupName</span></span>
<span data-ttu-id="21066-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="21066-124">Resource Group Name</span></span>

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

### <span data-ttu-id="21066-125">-Tópico</span><span class="sxs-lookup"><span data-stu-id="21066-125">-Topic</span></span>
<span data-ttu-id="21066-126">Para verificar a disponibilidade do nome do nome do tópico</span><span class="sxs-lookup"><span data-stu-id="21066-126">To Check Name Availability for Topic Name</span></span>

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

### <span data-ttu-id="21066-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21066-127">CommonParameters</span></span>
<span data-ttu-id="21066-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21066-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="21066-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21066-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21066-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="21066-130">INPUTS</span></span>

### <span data-ttu-id="21066-131">System.String</span><span class="sxs-lookup"><span data-stu-id="21066-131">System.String</span></span>

## <span data-ttu-id="21066-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="21066-132">OUTPUTS</span></span>

### <span data-ttu-id="21066-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="21066-133">System.Boolean</span></span>

## <span data-ttu-id="21066-134">Notas</span><span class="sxs-lookup"><span data-stu-id="21066-134">NOTES</span></span>

## <span data-ttu-id="21066-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21066-135">RELATED LINKS</span></span>
