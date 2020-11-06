---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
ms.openlocfilehash: 27d35f0c5b0e947624827d01d1182a09912cb9fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599155"
---
# <span data-ttu-id="c227a-101">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="c227a-101">Remove-AzServiceBusTopic</span></span>

## <span data-ttu-id="c227a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c227a-102">SYNOPSIS</span></span>
<span data-ttu-id="c227a-103">Remove o tópico do namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="c227a-103">Removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="c227a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c227a-104">SYNTAX</span></span>

### <span data-ttu-id="c227a-105">TopicPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c227a-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c227a-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c227a-106">TopicInputObjectSet</span></span>
```
Remove-AzServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c227a-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c227a-107">TopicResourceIdSet</span></span>
```
Remove-AzServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c227a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c227a-108">DESCRIPTION</span></span>
<span data-ttu-id="c227a-109">O cmdlet **Remove-AzServiceBusTopic** remove o tópico do namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="c227a-109">The **Remove-AzServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="c227a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c227a-110">EXAMPLES</span></span>

### <span data-ttu-id="c227a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c227a-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="c227a-112">Remove o tópico `SB-Topic_exampl1` do namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="c227a-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="c227a-113">Exemplo 2,1-InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="c227a-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusTopic <parmas>
PS C:\> Remove-AzServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="c227a-114">Exemplo 2,2-InputObject-usando o encanamento:</span><span class="sxs-lookup"><span data-stu-id="c227a-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusTopic <parmas> | Remove-AzServiceBusTopic
```

### <span data-ttu-id="c227a-115">Exemplo 3,1-ResourceId usando variável:</span><span class="sxs-lookup"><span data-stu-id="c227a-115">Example 3.1 - ResourceId Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzServiceBusTopic <params>
PS C:\> Remove-AzServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="c227a-116">Exemplo 3,2-ResourceId usando valor de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="c227a-116">Example 3.2 - ResourceId Using String value</span></span>
```
PS C:\> Remove-AzServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="c227a-117">OS</span><span class="sxs-lookup"><span data-stu-id="c227a-117">PARAMETERS</span></span>

### <span data-ttu-id="c227a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c227a-118">-AsJob</span></span>
<span data-ttu-id="c227a-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c227a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c227a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c227a-120">-DefaultProfile</span></span>
<span data-ttu-id="c227a-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c227a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c227a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c227a-122">-InputObject</span></span>
<span data-ttu-id="c227a-123">Objeto de tópico de barramento de serviço</span><span class="sxs-lookup"><span data-stu-id="c227a-123">Service Bus Topic Object</span></span>

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

### <span data-ttu-id="c227a-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c227a-124">-Name</span></span>
<span data-ttu-id="c227a-125">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="c227a-125">Topic Name</span></span>

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

### <span data-ttu-id="c227a-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c227a-126">-Namespace</span></span>
<span data-ttu-id="c227a-127">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="c227a-127">Namespace Name</span></span>

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

### <span data-ttu-id="c227a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c227a-128">-PassThru</span></span>
<span data-ttu-id="c227a-129">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c227a-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c227a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c227a-130">-ResourceGroupName</span></span>
<span data-ttu-id="c227a-131">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c227a-131">The name of the resource group</span></span>

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

### <span data-ttu-id="c227a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c227a-132">-ResourceId</span></span>
<span data-ttu-id="c227a-133">ID do recurso do tópico do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="c227a-133">Service Bus Topic Resource Id</span></span>

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

### <span data-ttu-id="c227a-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c227a-134">-Confirm</span></span>
<span data-ttu-id="c227a-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c227a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c227a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c227a-136">-WhatIf</span></span>
<span data-ttu-id="c227a-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c227a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c227a-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c227a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c227a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c227a-139">CommonParameters</span></span>
<span data-ttu-id="c227a-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c227a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c227a-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c227a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c227a-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c227a-142">INPUTS</span></span>

### <span data-ttu-id="c227a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c227a-143">System.String</span></span>

### <span data-ttu-id="c227a-144">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="c227a-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="c227a-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c227a-145">OUTPUTS</span></span>

### <span data-ttu-id="c227a-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c227a-146">System.Boolean</span></span>

## <span data-ttu-id="c227a-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c227a-147">NOTES</span></span>

## <span data-ttu-id="c227a-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c227a-148">RELATED LINKS</span></span>
