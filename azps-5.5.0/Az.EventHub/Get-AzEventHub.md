---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: ca2afaec702e27b4c20201cbd69984ec3827ded2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100126973"
---
# <span data-ttu-id="d1efd-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="d1efd-101">Get-AzEventHub</span></span>

## <span data-ttu-id="d1efd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1efd-102">SYNOPSIS</span></span>
<span data-ttu-id="d1efd-103">Obtém os detalhes de um único Hub de Eventos ou obtém uma lista de Hubs de Eventos.</span><span class="sxs-lookup"><span data-stu-id="d1efd-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="d1efd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1efd-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1efd-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1efd-105">DESCRIPTION</span></span>
<span data-ttu-id="d1efd-106">O Get-AzEventHub cmdlet retorna os detalhes de um Hub de Eventos ou uma lista de todos os Hubs de Eventos no namespace atual.</span><span class="sxs-lookup"><span data-stu-id="d1efd-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="d1efd-107">Se o nome do Hub de Eventos for fornecido, os detalhes de um único Hub de Eventos serão retornados.</span><span class="sxs-lookup"><span data-stu-id="d1efd-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="d1efd-108">Se um nome do Hub de Eventos não for fornecido, uma lista de todos os Hubs de Eventos no namespace especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="d1efd-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="d1efd-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d1efd-109">EXAMPLES</span></span>

### <span data-ttu-id="d1efd-110">Exemplo 1: EventHub especificado</span><span class="sxs-lookup"><span data-stu-id="d1efd-110">Example 1: specified EventHub</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="d1efd-111">Retorna os detalhes do Hub de Eventos \` MyEventHubName. \`</span><span class="sxs-lookup"><span data-stu-id="d1efd-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="d1efd-112">Exemplo 2: Lista de EventHub no Namespace especificado</span><span class="sxs-lookup"><span data-stu-id="d1efd-112">Example 2: List of EventHub in specified Namespace</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="d1efd-113">Retorna uma lista de Hubs de Eventos no namespace \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="d1efd-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="d1efd-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1efd-114">PARAMETERS</span></span>

### <span data-ttu-id="d1efd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1efd-115">-DefaultProfile</span></span>
<span data-ttu-id="d1efd-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1efd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1efd-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d1efd-117">-MaxCount</span></span>
<span data-ttu-id="d1efd-118">Determine o número máximo de EventHubs a retornar.</span><span class="sxs-lookup"><span data-stu-id="d1efd-118">Determine the maximum number of EventHubs to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1efd-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1efd-119">-Name</span></span>
<span data-ttu-id="d1efd-120">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="d1efd-120">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1efd-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d1efd-121">-Namespace</span></span>
<span data-ttu-id="d1efd-122">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="d1efd-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1efd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1efd-123">-ResourceGroupName</span></span>
<span data-ttu-id="d1efd-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d1efd-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1efd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1efd-125">CommonParameters</span></span>
<span data-ttu-id="d1efd-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1efd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1efd-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1efd-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1efd-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="d1efd-128">INPUTS</span></span>

### <span data-ttu-id="d1efd-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d1efd-129">System.String</span></span>

## <span data-ttu-id="d1efd-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="d1efd-130">OUTPUTS</span></span>

### <span data-ttu-id="d1efd-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="d1efd-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="d1efd-132">Notas</span><span class="sxs-lookup"><span data-stu-id="d1efd-132">NOTES</span></span>

## <span data-ttu-id="d1efd-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1efd-133">RELATED LINKS</span></span>
