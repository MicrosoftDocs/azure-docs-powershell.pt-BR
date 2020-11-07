---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: e2cd8cfeadf0c9574cbf39a642133109aa02ec39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955580"
---
# <span data-ttu-id="1fb2a-101">Get-AzEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="1fb2a-101">Get-AzEventGridTopicType</span></span>

## <span data-ttu-id="1fb2a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1fb2a-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb2a-103">Obtém os detalhes sobre os tipos de tópico suportados pela grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb2a-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

## <span data-ttu-id="1fb2a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1fb2a-104">SYNTAX</span></span>

```
Get-AzEventGridTopicType [-Name <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1fb2a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1fb2a-105">DESCRIPTION</span></span>
<span data-ttu-id="1fb2a-106">Obtém os detalhes dos tipos de tópico suportados pela grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb2a-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="1fb2a-107">Se um nome de tipo de tópico for especificado, os detalhes sobre esse tipo de tópico serão retornados.</span><span class="sxs-lookup"><span data-stu-id="1fb2a-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="1fb2a-108">Se um nome de tipo de tópico não for especificado, os detalhes sobre todos os tipos de tópico serão retornados.</span><span class="sxs-lookup"><span data-stu-id="1fb2a-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="1fb2a-109">Se IncludeEventTypes for especificado, as informações sobre os tipos de eventos com suporte em cada tipo de tópico serão incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="1fb2a-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="1fb2a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1fb2a-110">EXAMPLES</span></span>

### <span data-ttu-id="1fb2a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1fb2a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType
```

<span data-ttu-id="1fb2a-112">Obtém uma lista dos tipos de tópico.</span><span class="sxs-lookup"><span data-stu-id="1fb2a-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="1fb2a-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1fb2a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="1fb2a-114">Obtém informações sobre o tipo de tópico StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="1fb2a-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="1fb2a-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="1fb2a-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="1fb2a-116">Obtém informações sobre o tipo de tópico StorageAccounts, incluindo os tipos de eventos com suporte pelo StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="1fb2a-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="1fb2a-117">OS</span><span class="sxs-lookup"><span data-stu-id="1fb2a-117">PARAMETERS</span></span>

### <span data-ttu-id="1fb2a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb2a-118">-DefaultProfile</span></span>
<span data-ttu-id="1fb2a-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1fb2a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1fb2a-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="1fb2a-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="1fb2a-121">Se especificado, a resposta incluirá os tipos de eventos suportados por um tipo de tópico.</span><span class="sxs-lookup"><span data-stu-id="1fb2a-121">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="1fb2a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1fb2a-122">-Name</span></span>
<span data-ttu-id="1fb2a-123">Nome do tipo de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="1fb2a-123">EventGrid Topic Type Name.</span></span>

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

### <span data-ttu-id="1fb2a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb2a-124">CommonParameters</span></span>
<span data-ttu-id="1fb2a-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fb2a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb2a-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1fb2a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb2a-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1fb2a-127">INPUTS</span></span>

### <span data-ttu-id="1fb2a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1fb2a-128">System.String</span></span>

## <span data-ttu-id="1fb2a-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1fb2a-129">OUTPUTS</span></span>

### <span data-ttu-id="1fb2a-130">Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="1fb2a-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="1fb2a-131">Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="1fb2a-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="1fb2a-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1fb2a-132">NOTES</span></span>

## <span data-ttu-id="1fb2a-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1fb2a-133">RELATED LINKS</span></span>
