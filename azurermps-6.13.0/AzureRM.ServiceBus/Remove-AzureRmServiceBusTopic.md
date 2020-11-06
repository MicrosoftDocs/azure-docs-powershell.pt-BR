---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
ms.openlocfilehash: 8434893dd3661bbfb1f78a4973dc206f44e9f400
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427158"
---
# <span data-ttu-id="661e4-101">Remove-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="661e4-101">Remove-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="661e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="661e4-102">SYNOPSIS</span></span>
<span data-ttu-id="661e4-103">Remove o tópico do namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="661e4-103">Removes the topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="661e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="661e4-104">SYNTAX</span></span>

### <span data-ttu-id="661e4-105">TopicPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="661e4-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="661e4-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="661e4-106">TopicInputObjectSet</span></span>
```
Remove-AzureRmServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="661e4-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="661e4-107">TopicResourceIdSet</span></span>
```
Remove-AzureRmServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="661e4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="661e4-108">DESCRIPTION</span></span>
<span data-ttu-id="661e4-109">O cmdlet **Remove-AzureRmServiceBusTopic** remove o tópico do namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="661e4-109">The **Remove-AzureRmServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="661e4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="661e4-110">EXAMPLES</span></span>

### <span data-ttu-id="661e4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="661e4-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="661e4-112">Remove o tópico `SB-Topic_exampl1` do namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="661e4-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="661e4-113">Exemplo 2,1-InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="661e4-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusTopic <parmas>
PS C:\> Remove-AzureRmServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="661e4-114">Exemplo 2,2-InputObject-usando o encanamento:</span><span class="sxs-lookup"><span data-stu-id="661e4-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic <parmas> | Remove-AzureRmServiceBusTopic
```

### <span data-ttu-id="661e4-115">Exemplo 3,1-ResourceId usando variável:</span><span class="sxs-lookup"><span data-stu-id="661e4-115">Example 3.1 - ResourceId Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzureRmServiceBusTopic <params>
PS C:\> Remove-AzureRmServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="661e4-116">Exemplo 3,2-ResourceId usando valor de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="661e4-116">Example 3.2 - ResourceId Using String value</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="661e4-117">OS</span><span class="sxs-lookup"><span data-stu-id="661e4-117">PARAMETERS</span></span>

### <span data-ttu-id="661e4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="661e4-118">-AsJob</span></span>
<span data-ttu-id="661e4-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="661e4-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="661e4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="661e4-120">-DefaultProfile</span></span>
<span data-ttu-id="661e4-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="661e4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="661e4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="661e4-122">-InputObject</span></span>
<span data-ttu-id="661e4-123">Objeto de tópico de barramento de serviço</span><span class="sxs-lookup"><span data-stu-id="661e4-123">Service Bus Topic Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: TopicInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="661e4-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="661e4-124">-Name</span></span>
<span data-ttu-id="661e4-125">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="661e4-125">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="661e4-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="661e4-126">-Namespace</span></span>
<span data-ttu-id="661e4-127">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="661e4-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="661e4-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="661e4-128">-PassThru</span></span>
<span data-ttu-id="661e4-129">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="661e4-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="661e4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="661e4-130">-ResourceGroupName</span></span>
<span data-ttu-id="661e4-131">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="661e4-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="661e4-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="661e4-132">-ResourceId</span></span>
<span data-ttu-id="661e4-133">ID do recurso do tópico do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="661e4-133">Service Bus Topic Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: TopicResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="661e4-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="661e4-134">-Confirm</span></span>
<span data-ttu-id="661e4-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="661e4-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="661e4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="661e4-136">-WhatIf</span></span>
<span data-ttu-id="661e4-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="661e4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="661e4-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="661e4-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="661e4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="661e4-139">CommonParameters</span></span>
<span data-ttu-id="661e4-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="661e4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="661e4-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="661e4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="661e4-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="661e4-142">INPUTS</span></span>

### <span data-ttu-id="661e4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="661e4-143">System.String</span></span>

### <span data-ttu-id="661e4-144">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="661e4-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>
<span data-ttu-id="661e4-145">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="661e4-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="661e4-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="661e4-146">OUTPUTS</span></span>

### <span data-ttu-id="661e4-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="661e4-147">System.Boolean</span></span>

## <span data-ttu-id="661e4-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="661e4-148">NOTES</span></span>

## <span data-ttu-id="661e4-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="661e4-149">RELATED LINKS</span></span>
