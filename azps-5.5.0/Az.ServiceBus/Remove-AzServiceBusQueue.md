---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
ms.openlocfilehash: c93f0d8a44a67195d2c901dd581505276b7ae2f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117124"
---
# <span data-ttu-id="335a3-101">Remove-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="335a3-101">Remove-AzServiceBusQueue</span></span>

## <span data-ttu-id="335a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="335a3-102">SYNOPSIS</span></span>
<span data-ttu-id="335a3-103">Remove a fila do namespace de Barra de Serviços especificado.</span><span class="sxs-lookup"><span data-stu-id="335a3-103">Removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="335a3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="335a3-104">SYNTAX</span></span>

### <span data-ttu-id="335a3-105">QueuePropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="335a3-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="335a3-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="335a3-106">QueueInputObjectSet</span></span>
```
Remove-AzServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="335a3-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="335a3-107">QueueResourceIdSet</span></span>
```
Remove-AzServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="335a3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="335a3-108">DESCRIPTION</span></span>
<span data-ttu-id="335a3-109">O cmdlet **Remove-AzServiceBusQueue** remove a fila do namespace de Barra de Serviços especificado.</span><span class="sxs-lookup"><span data-stu-id="335a3-109">The **Remove-AzServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="335a3-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="335a3-110">EXAMPLES</span></span>

### <span data-ttu-id="335a3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="335a3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="335a3-112">Remove a fila de Service Bus `SB-Queue_exampl1` do `SB-Example1` namespace.</span><span class="sxs-lookup"><span data-stu-id="335a3-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="335a3-113">Exemplo 2: InputObject - Usando variável:</span><span class="sxs-lookup"><span data-stu-id="335a3-113">Example 2: InputObject - Using variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="335a3-114">Remove a fila de Service Bus fornecida no parâmetro $inputobject para -InputObject</span><span class="sxs-lookup"><span data-stu-id="335a3-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="335a3-115">Exemplo 3: InputObject - Usando a piping:</span><span class="sxs-lookup"><span data-stu-id="335a3-115">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>  Get-AzServiceBusQueue <params> | Remove-AzServiceBusQueue
```

### <span data-ttu-id="335a3-116">Exemplo 4: ResourceId - Usando variável:</span><span class="sxs-lookup"><span data-stu-id="335a3-116">Example 4: ResourceId - Using variable:</span></span>
```powershell
PS c:\> $resourceid = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="335a3-117">Remove a fila de Service Bus fornecida na id arm no $resourceid/cadeia de caracteres para o parâmetro -ResourceId</span><span class="sxs-lookup"><span data-stu-id="335a3-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="335a3-118">Exemplo 5: ResourceId - passando como cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="335a3-118">Example 5: ResourceId - passing as string:</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="335a3-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="335a3-119">PARAMETERS</span></span>

### <span data-ttu-id="335a3-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="335a3-120">-AsJob</span></span>
<span data-ttu-id="335a3-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="335a3-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="335a3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="335a3-122">-DefaultProfile</span></span>
<span data-ttu-id="335a3-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="335a3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="335a3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="335a3-124">-InputObject</span></span>
<span data-ttu-id="335a3-125">Objeto de fila de barramento de serviço</span><span class="sxs-lookup"><span data-stu-id="335a3-125">Service Bus Queue Object</span></span>

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

### <span data-ttu-id="335a3-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="335a3-126">-Name</span></span>
<span data-ttu-id="335a3-127">Nome da Fila</span><span class="sxs-lookup"><span data-stu-id="335a3-127">Queue Name</span></span>

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

### <span data-ttu-id="335a3-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="335a3-128">-Namespace</span></span>
<span data-ttu-id="335a3-129">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="335a3-129">Namespace Name</span></span>

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

### <span data-ttu-id="335a3-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="335a3-130">-PassThru</span></span>
<span data-ttu-id="335a3-131">Especificar isso retornará verdadeiro se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="335a3-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="335a3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="335a3-132">-ResourceGroupName</span></span>
<span data-ttu-id="335a3-133">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="335a3-133">The name of the resource group</span></span>

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

### <span data-ttu-id="335a3-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="335a3-134">-ResourceId</span></span>
<span data-ttu-id="335a3-135">ID do Recurso da Fila de Barra de Serviços</span><span class="sxs-lookup"><span data-stu-id="335a3-135">Service Bus Queue Resource Id</span></span>

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

### <span data-ttu-id="335a3-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="335a3-136">-Confirm</span></span>
<span data-ttu-id="335a3-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="335a3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="335a3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="335a3-138">-WhatIf</span></span>
<span data-ttu-id="335a3-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="335a3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="335a3-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="335a3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="335a3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="335a3-141">CommonParameters</span></span>
<span data-ttu-id="335a3-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="335a3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="335a3-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="335a3-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="335a3-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="335a3-144">INPUTS</span></span>

### <span data-ttu-id="335a3-145">System.String</span><span class="sxs-lookup"><span data-stu-id="335a3-145">System.String</span></span>

### <span data-ttu-id="335a3-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="335a3-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="335a3-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="335a3-147">OUTPUTS</span></span>

### <span data-ttu-id="335a3-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="335a3-148">System.Boolean</span></span>

## <span data-ttu-id="335a3-149">Notas</span><span class="sxs-lookup"><span data-stu-id="335a3-149">NOTES</span></span>

## <span data-ttu-id="335a3-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="335a3-150">RELATED LINKS</span></span>
