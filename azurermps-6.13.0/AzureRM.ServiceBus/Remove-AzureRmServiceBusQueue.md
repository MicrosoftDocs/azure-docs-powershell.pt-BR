---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: ba59f19183cf49802240d7631b99b3e69a9bc6f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430864"
---
# <span data-ttu-id="c7f26-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="c7f26-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="c7f26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7f26-102">SYNOPSIS</span></span>
<span data-ttu-id="c7f26-103">Remove a fila do namespace especificado de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="c7f26-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7f26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7f26-104">SYNTAX</span></span>

### <span data-ttu-id="c7f26-105">QueuePropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c7f26-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7f26-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c7f26-106">QueueInputObjectSet</span></span>
```
Remove-AzureRmServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7f26-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c7f26-107">QueueResourceIdSet</span></span>
```
Remove-AzureRmServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7f26-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7f26-108">DESCRIPTION</span></span>
<span data-ttu-id="c7f26-109">O cmdlet **Remove-AzureRmServiceBusQueue** remove a fila do namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="c7f26-109">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="c7f26-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7f26-110">EXAMPLES</span></span>

### <span data-ttu-id="c7f26-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c7f26-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="c7f26-112">Remove a fila de barramento do serviço `SB-Queue_exampl1` do namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="c7f26-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="c7f26-113">Exemplo 2,1-InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="c7f26-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusQueue <params>
PS C:\> Remove-AzureRmServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="c7f26-114">Remove a fila do barramento do serviço fornecida no parâmetro $inputobject para-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7f26-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="c7f26-115">Exemplo 2,1-InputObject-usando o encanamento:</span><span class="sxs-lookup"><span data-stu-id="c7f26-115">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\>  Get-AzureRmServiceBusQueue <params> | Remove-AzureRmServiceBusQueue
```

### <span data-ttu-id="c7f26-116">Exemplo 3,1-ResourceId-usando variável:</span><span class="sxs-lookup"><span data-stu-id="c7f26-116">Example 3.1 - ResourceId - Using variable:</span></span>
```
PS c:\> $resourceid = Get-AzureRmServiceBusQueue <params>
PS C:\> Remove-AzureRmServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="c7f26-117">Remove a fila do barramento do serviço fornecida na ID do braço no parâmetro $resourceid/String para-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7f26-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="c7f26-118">Exemplo 3,2-ResourceId-passign as String:</span><span class="sxs-lookup"><span data-stu-id="c7f26-118">Example 3.2 - ResourceId - passign as string:</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="c7f26-119">OS</span><span class="sxs-lookup"><span data-stu-id="c7f26-119">PARAMETERS</span></span>

### <span data-ttu-id="c7f26-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7f26-120">-AsJob</span></span>
<span data-ttu-id="c7f26-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c7f26-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7f26-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7f26-122">-DefaultProfile</span></span>
<span data-ttu-id="c7f26-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c7f26-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7f26-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7f26-124">-InputObject</span></span>
<span data-ttu-id="c7f26-125">Objeto fila do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="c7f26-125">Service Bus Queue Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes
Parameter Sets: QueueInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7f26-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7f26-126">-Name</span></span>
<span data-ttu-id="c7f26-127">Nome da fila</span><span class="sxs-lookup"><span data-stu-id="c7f26-127">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7f26-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c7f26-128">-Namespace</span></span>
<span data-ttu-id="c7f26-129">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="c7f26-129">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7f26-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7f26-130">-PassThru</span></span>
<span data-ttu-id="c7f26-131">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c7f26-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c7f26-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7f26-132">-ResourceGroupName</span></span>
<span data-ttu-id="c7f26-133">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c7f26-133">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7f26-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7f26-134">-ResourceId</span></span>
<span data-ttu-id="c7f26-135">ID do recurso da fila do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="c7f26-135">Service Bus Queue Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: QueueResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7f26-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c7f26-136">-Confirm</span></span>
<span data-ttu-id="c7f26-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7f26-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7f26-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7f26-138">-WhatIf</span></span>
<span data-ttu-id="c7f26-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c7f26-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7f26-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c7f26-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7f26-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7f26-141">CommonParameters</span></span>
<span data-ttu-id="c7f26-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7f26-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7f26-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7f26-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7f26-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7f26-144">INPUTS</span></span>

### <span data-ttu-id="c7f26-145">System. String</span><span class="sxs-lookup"><span data-stu-id="c7f26-145">System.String</span></span>

### <span data-ttu-id="c7f26-146">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="c7f26-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>
<span data-ttu-id="c7f26-147">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c7f26-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c7f26-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7f26-148">OUTPUTS</span></span>

### <span data-ttu-id="c7f26-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c7f26-149">System.Boolean</span></span>

## <span data-ttu-id="c7f26-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7f26-150">NOTES</span></span>

## <span data-ttu-id="c7f26-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7f26-151">RELATED LINKS</span></span>
