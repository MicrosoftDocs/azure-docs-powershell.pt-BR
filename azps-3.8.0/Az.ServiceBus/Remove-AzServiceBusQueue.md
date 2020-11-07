---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
ms.openlocfilehash: 6a2ba59acb8148cc3640582b57772a68014177ef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941292"
---
# <span data-ttu-id="0357b-101">Remove-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="0357b-101">Remove-AzServiceBusQueue</span></span>

## <span data-ttu-id="0357b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0357b-102">SYNOPSIS</span></span>
<span data-ttu-id="0357b-103">Remove a fila do namespace especificado de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="0357b-103">Removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="0357b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0357b-104">SYNTAX</span></span>

### <span data-ttu-id="0357b-105">QueuePropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0357b-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0357b-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0357b-106">QueueInputObjectSet</span></span>
```
Remove-AzServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0357b-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0357b-107">QueueResourceIdSet</span></span>
```
Remove-AzServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0357b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0357b-108">DESCRIPTION</span></span>
<span data-ttu-id="0357b-109">O cmdlet **Remove-AzServiceBusQueue** remove a fila do namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="0357b-109">The **Remove-AzServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="0357b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0357b-110">EXAMPLES</span></span>

### <span data-ttu-id="0357b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0357b-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="0357b-112">Remove a fila de barramento do serviço `SB-Queue_exampl1` do namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="0357b-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="0357b-113">Exemplo 2,1-InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="0357b-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="0357b-114">Remove a fila do barramento do serviço fornecida no parâmetro $inputobject para-InputObject</span><span class="sxs-lookup"><span data-stu-id="0357b-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="0357b-115">Exemplo 2,1-InputObject-usando o encanamento:</span><span class="sxs-lookup"><span data-stu-id="0357b-115">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\>  Get-AzServiceBusQueue <params> | Remove-AzServiceBusQueue
```

### <span data-ttu-id="0357b-116">Exemplo 3,1-ResourceId-usando variável:</span><span class="sxs-lookup"><span data-stu-id="0357b-116">Example 3.1 - ResourceId - Using variable:</span></span>
```
PS c:\> $resourceid = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="0357b-117">Remove a fila do barramento do serviço fornecida na ID do braço no parâmetro $resourceid/String para-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0357b-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="0357b-118">Exemplo 3,2-ResourceId-passando como cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="0357b-118">Example 3.2 - ResourceId - passing as string:</span></span>
```
PS C:\> Remove-AzServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="0357b-119">OS</span><span class="sxs-lookup"><span data-stu-id="0357b-119">PARAMETERS</span></span>

### <span data-ttu-id="0357b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0357b-120">-AsJob</span></span>
<span data-ttu-id="0357b-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0357b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0357b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0357b-122">-DefaultProfile</span></span>
<span data-ttu-id="0357b-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0357b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0357b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0357b-124">-InputObject</span></span>
<span data-ttu-id="0357b-125">Objeto fila do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="0357b-125">Service Bus Queue Object</span></span>

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

### <span data-ttu-id="0357b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="0357b-126">-Name</span></span>
<span data-ttu-id="0357b-127">Nome da fila</span><span class="sxs-lookup"><span data-stu-id="0357b-127">Queue Name</span></span>

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

### <span data-ttu-id="0357b-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0357b-128">-Namespace</span></span>
<span data-ttu-id="0357b-129">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="0357b-129">Namespace Name</span></span>

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

### <span data-ttu-id="0357b-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0357b-130">-PassThru</span></span>
<span data-ttu-id="0357b-131">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0357b-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="0357b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0357b-132">-ResourceGroupName</span></span>
<span data-ttu-id="0357b-133">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0357b-133">The name of the resource group</span></span>

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

### <span data-ttu-id="0357b-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0357b-134">-ResourceId</span></span>
<span data-ttu-id="0357b-135">ID do recurso da fila do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="0357b-135">Service Bus Queue Resource Id</span></span>

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

### <span data-ttu-id="0357b-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0357b-136">-Confirm</span></span>
<span data-ttu-id="0357b-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0357b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0357b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0357b-138">-WhatIf</span></span>
<span data-ttu-id="0357b-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0357b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0357b-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0357b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0357b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0357b-141">CommonParameters</span></span>
<span data-ttu-id="0357b-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0357b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0357b-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0357b-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0357b-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0357b-144">INPUTS</span></span>

### <span data-ttu-id="0357b-145">System. String</span><span class="sxs-lookup"><span data-stu-id="0357b-145">System.String</span></span>

### <span data-ttu-id="0357b-146">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="0357b-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="0357b-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0357b-147">OUTPUTS</span></span>

### <span data-ttu-id="0357b-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0357b-148">System.Boolean</span></span>

## <span data-ttu-id="0357b-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0357b-149">NOTES</span></span>

## <span data-ttu-id="0357b-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0357b-150">RELATED LINKS</span></span>
