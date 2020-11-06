---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: 24041c299f2f242126f265ad232db3e0c5d526b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440183"
---
# <span data-ttu-id="b24b5-101">Get-AzureRmServiceBusTopicKey</span><span class="sxs-lookup"><span data-stu-id="b24b5-101">Get-AzureRmServiceBusTopicKey</span></span>

## <span data-ttu-id="b24b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b24b5-102">SYNOPSIS</span></span>
<span data-ttu-id="b24b5-103">Obtém as cadeias de conexão primária e secundária para o tópico de barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="b24b5-103">Gets the primary and secondary connection strings for the Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b24b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b24b5-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b24b5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b24b5-105">DESCRIPTION</span></span>
<span data-ttu-id="b24b5-106">O cmdlet **Get-AzureRmServiceBusTopicKey** retorna as cadeias de conexão primária e secundária para o tópico de barramento de serviço fornecido.</span><span class="sxs-lookup"><span data-stu-id="b24b5-106">The **Get-AzureRmServiceBusTopicKey** cmdlet returns the primary and secondary connection strings for the given Service Bus topic.</span></span>

## <span data-ttu-id="b24b5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b24b5-107">EXAMPLES</span></span>

### <span data-ttu-id="b24b5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b24b5-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="b24b5-109">Retorna as cadeias de conexão primária e secundária para o tópico de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="b24b5-109">Returns the primary and secondary connection strings for the specified Service Bus topic.</span></span>

## <span data-ttu-id="b24b5-110">OS</span><span class="sxs-lookup"><span data-stu-id="b24b5-110">PARAMETERS</span></span>

### <span data-ttu-id="b24b5-111">-Resource</span><span class="sxs-lookup"><span data-stu-id="b24b5-111">-ResourceGroup</span></span>
<span data-ttu-id="b24b5-112">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b24b5-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="b24b5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b24b5-113">-DefaultProfile</span></span>
<span data-ttu-id="b24b5-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b24b5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b24b5-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b24b5-115">-Name</span></span>
<span data-ttu-id="b24b5-116">Nome do tópico AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="b24b5-116">Topic AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b24b5-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b24b5-117">-Namespace</span></span>
<span data-ttu-id="b24b5-118">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="b24b5-118">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b24b5-119">-Tópico</span><span class="sxs-lookup"><span data-stu-id="b24b5-119">-Topic</span></span>
<span data-ttu-id="b24b5-120">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="b24b5-120">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b24b5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b24b5-121">CommonParameters</span></span>
<span data-ttu-id="b24b5-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b24b5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b24b5-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b24b5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b24b5-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b24b5-124">INPUTS</span></span>

### <span data-ttu-id="b24b5-125">-Resource</span><span class="sxs-lookup"><span data-stu-id="b24b5-125">-ResourceGroup</span></span>
 <span data-ttu-id="b24b5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b24b5-126">System.String</span></span>
 

### <span data-ttu-id="b24b5-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b24b5-127">-NamespaceName</span></span>
 <span data-ttu-id="b24b5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b24b5-128">System.String</span></span>
 

### <span data-ttu-id="b24b5-129">-Topicname</span><span class="sxs-lookup"><span data-stu-id="b24b5-129">-TopicName</span></span>
 <span data-ttu-id="b24b5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b24b5-130">System.String</span></span>
 

### <span data-ttu-id="b24b5-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="b24b5-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="b24b5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b24b5-132">System.String</span></span>

## <span data-ttu-id="b24b5-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b24b5-133">OUTPUTS</span></span>

### <span data-ttu-id="b24b5-134">Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="b24b5-134">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="b24b5-135">PrimaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-a pic_exampl1 SecondaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-a pic_exampl1 PrimaryKey: {PrimaryKey Value} SecondaryKey: {SecondaryKey Value} KeyName: SBTopicAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="b24b5-135">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-To pic_exampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-To pic_exampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBTopicAuthoRule1</span></span>

## <span data-ttu-id="b24b5-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b24b5-136">NOTES</span></span>

## <span data-ttu-id="b24b5-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b24b5-137">RELATED LINKS</span></span>

