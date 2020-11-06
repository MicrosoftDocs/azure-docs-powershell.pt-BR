---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
ms.openlocfilehash: bc272648920e29ed2e735ca08b9fa78563a9f9d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603062"
---
# <span data-ttu-id="b97e9-101">Get-AzureRmEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="b97e9-101">Get-AzureRmEventGridTopicType</span></span>

## <span data-ttu-id="b97e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b97e9-102">SYNOPSIS</span></span>
<span data-ttu-id="b97e9-103">Obtém os detalhes sobre os tipos de tópico suportados pela grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b97e9-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b97e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b97e9-104">SYNTAX</span></span>

```
Get-AzureRmEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b97e9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b97e9-105">DESCRIPTION</span></span>
<span data-ttu-id="b97e9-106">Obtém os detalhes dos tipos de tópico suportados pela grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b97e9-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="b97e9-107">Se um nome de tipo de tópico for especificado, os detalhes sobre esse tipo de tópico serão retornados.</span><span class="sxs-lookup"><span data-stu-id="b97e9-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="b97e9-108">Se um nome de tipo de tópico não for especificado, os detalhes sobre todos os tipos de tópico serão retornados.</span><span class="sxs-lookup"><span data-stu-id="b97e9-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="b97e9-109">Se IncludeEventTypes for especificado, as informações sobre os tipos de eventos com suporte em cada tipo de tópico serão incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="b97e9-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="b97e9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b97e9-110">EXAMPLES</span></span>

### <span data-ttu-id="b97e9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b97e9-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType
```

<span data-ttu-id="b97e9-112">Obtém uma lista dos tipos de tópico.</span><span class="sxs-lookup"><span data-stu-id="b97e9-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="b97e9-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b97e9-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="b97e9-114">Obtém informações sobre o tipo de tópico StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="b97e9-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="b97e9-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b97e9-115">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="b97e9-116">Obtém informações sobre o tipo de tópico StorageAccounts, incluindo os tipos de eventos com suporte pelo StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="b97e9-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="b97e9-117">OS</span><span class="sxs-lookup"><span data-stu-id="b97e9-117">PARAMETERS</span></span>

### <span data-ttu-id="b97e9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b97e9-118">-DefaultProfile</span></span>
<span data-ttu-id="b97e9-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b97e9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b97e9-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="b97e9-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="b97e9-121">Se especificado, a resposta incluirá os tipos de eventos suportados por um tipo de tópico.</span><span class="sxs-lookup"><span data-stu-id="b97e9-121">If specified, the response will include the event types supported by a topic type.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97e9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b97e9-122">-Name</span></span>
<span data-ttu-id="b97e9-123">Nome do tipo de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="b97e9-123">EventGrid Topic Type Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b97e9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b97e9-124">CommonParameters</span></span>
<span data-ttu-id="b97e9-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b97e9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b97e9-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b97e9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b97e9-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b97e9-127">INPUTS</span></span>

### <span data-ttu-id="b97e9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b97e9-128">System.String</span></span>
<span data-ttu-id="b97e9-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b97e9-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b97e9-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b97e9-130">OUTPUTS</span></span>

### <span data-ttu-id="b97e9-131">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfoListInstance, Microsoft. Azure. Commands. EventGrid, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b97e9-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="b97e9-132">Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="b97e9-132">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="b97e9-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b97e9-133">NOTES</span></span>

## <span data-ttu-id="b97e9-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b97e9-134">RELATED LINKS</span></span>

