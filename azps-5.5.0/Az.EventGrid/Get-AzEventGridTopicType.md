---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: e2cd8cfeadf0c9574cbf39a642133109aa02ec39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115321"
---
# <span data-ttu-id="54753-101">Get-AzEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="54753-101">Get-AzEventGridTopicType</span></span>

## <span data-ttu-id="54753-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54753-102">SYNOPSIS</span></span>
<span data-ttu-id="54753-103">Obtém os detalhes sobre os tipos de tópico com suporte na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="54753-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

## <span data-ttu-id="54753-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54753-104">SYNTAX</span></span>

```
Get-AzEventGridTopicType [-Name <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54753-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="54753-105">DESCRIPTION</span></span>
<span data-ttu-id="54753-106">Obtém os detalhes dos tipos de tópico com suporte na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="54753-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="54753-107">Se um nome de tipo de tópico for especificado, os detalhes sobre esse tipo de tópico serão retornados.</span><span class="sxs-lookup"><span data-stu-id="54753-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="54753-108">Se um nome de tipo de tópico não for especificado, detalhes sobre todos os tipos de tópico serão retornados.</span><span class="sxs-lookup"><span data-stu-id="54753-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="54753-109">Se IncludeEventTypes for especificado, as informações sobre tipos de evento com suporte em cada tipo de tópico serão incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="54753-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="54753-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="54753-110">EXAMPLES</span></span>

### <span data-ttu-id="54753-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="54753-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType
```

<span data-ttu-id="54753-112">Obtém uma lista dos tipos de tópico.</span><span class="sxs-lookup"><span data-stu-id="54753-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="54753-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="54753-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="54753-114">Obtém informações sobre o tipo de tópico StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="54753-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="54753-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="54753-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="54753-116">Obtém informações sobre o tipo de tópico StorageAccounts, incluindo os tipos de evento suportados por StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="54753-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="54753-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54753-117">PARAMETERS</span></span>

### <span data-ttu-id="54753-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54753-118">-DefaultProfile</span></span>
<span data-ttu-id="54753-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="54753-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54753-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="54753-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="54753-121">Se especificado, a resposta incluirá os tipos de evento suportados por um tipo de tópico.</span><span class="sxs-lookup"><span data-stu-id="54753-121">If specified, the response will include the event types supported by a topic type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54753-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="54753-122">-Name</span></span>
<span data-ttu-id="54753-123">Nome do tipo de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="54753-123">EventGrid Topic Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54753-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54753-124">CommonParameters</span></span>
<span data-ttu-id="54753-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54753-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54753-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54753-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54753-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="54753-127">INPUTS</span></span>

### <span data-ttu-id="54753-128">System.String</span><span class="sxs-lookup"><span data-stu-id="54753-128">System.String</span></span>

## <span data-ttu-id="54753-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="54753-129">OUTPUTS</span></span>

### <span data-ttu-id="54753-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="54753-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="54753-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="54753-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="54753-132">Notas</span><span class="sxs-lookup"><span data-stu-id="54753-132">NOTES</span></span>

## <span data-ttu-id="54753-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54753-133">RELATED LINKS</span></span>
