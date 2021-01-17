---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
ms.openlocfilehash: 75da2231dae7ea0dc587d48ca832b7631fc24986
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433108"
---
# <span data-ttu-id="235fd-101">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="235fd-101">Remove-AzServiceBusTopic</span></span>

## <span data-ttu-id="235fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="235fd-102">SYNOPSIS</span></span>
<span data-ttu-id="235fd-103">Remove o tópico do namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="235fd-103">Removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="235fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="235fd-104">SYNTAX</span></span>

### <span data-ttu-id="235fd-105">TopicPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="235fd-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="235fd-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="235fd-106">TopicInputObjectSet</span></span>
```
Remove-AzServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="235fd-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="235fd-107">TopicResourceIdSet</span></span>
```
Remove-AzServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="235fd-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="235fd-108">DESCRIPTION</span></span>
<span data-ttu-id="235fd-109">O cmdlet **Remove-AzServiceBusTopic** remove o tópico do namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="235fd-109">The **Remove-AzServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="235fd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="235fd-110">EXAMPLES</span></span>

### <span data-ttu-id="235fd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="235fd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="235fd-112">Remove o tópico `SB-Topic_exampl1` do namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="235fd-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="235fd-113">Exemplo 2: InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="235fd-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusTopic <parmas>
PS C:\> Remove-AzServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="235fd-114">Exemplo 3: InputObject-usando o encanamento:</span><span class="sxs-lookup"><span data-stu-id="235fd-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusTopic <parmas> | Remove-AzServiceBusTopic
```

### <span data-ttu-id="235fd-115">Exemplo 4: ResourceId usando variável:</span><span class="sxs-lookup"><span data-stu-id="235fd-115">Example 4: ResourceId Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusTopic <params>
PS C:\> Remove-AzServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="235fd-116">Exemplo 5: ResourceId usando valor de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="235fd-116">Example 5: ResourceId Using String value</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="235fd-117">OS</span><span class="sxs-lookup"><span data-stu-id="235fd-117">PARAMETERS</span></span>

### <span data-ttu-id="235fd-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="235fd-118">-AsJob</span></span>
<span data-ttu-id="235fd-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="235fd-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="235fd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="235fd-120">-DefaultProfile</span></span>
<span data-ttu-id="235fd-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="235fd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="235fd-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="235fd-122">-InputObject</span></span>
<span data-ttu-id="235fd-123">Objeto de tópico de barramento de serviço</span><span class="sxs-lookup"><span data-stu-id="235fd-123">Service Bus Topic Object</span></span>

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

### <span data-ttu-id="235fd-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="235fd-124">-Name</span></span>
<span data-ttu-id="235fd-125">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="235fd-125">Topic Name</span></span>

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

### <span data-ttu-id="235fd-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="235fd-126">-Namespace</span></span>
<span data-ttu-id="235fd-127">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="235fd-127">Namespace Name</span></span>

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

### <span data-ttu-id="235fd-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="235fd-128">-PassThru</span></span>
<span data-ttu-id="235fd-129">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="235fd-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="235fd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="235fd-130">-ResourceGroupName</span></span>
<span data-ttu-id="235fd-131">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="235fd-131">The name of the resource group</span></span>

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

### <span data-ttu-id="235fd-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="235fd-132">-ResourceId</span></span>
<span data-ttu-id="235fd-133">ID do recurso do tópico do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="235fd-133">Service Bus Topic Resource Id</span></span>

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

### <span data-ttu-id="235fd-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="235fd-134">-Confirm</span></span>
<span data-ttu-id="235fd-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="235fd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="235fd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="235fd-136">-WhatIf</span></span>
<span data-ttu-id="235fd-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="235fd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="235fd-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="235fd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="235fd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="235fd-139">CommonParameters</span></span>
<span data-ttu-id="235fd-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="235fd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="235fd-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="235fd-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="235fd-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="235fd-142">INPUTS</span></span>

### <span data-ttu-id="235fd-143">System. String</span><span class="sxs-lookup"><span data-stu-id="235fd-143">System.String</span></span>

### <span data-ttu-id="235fd-144">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="235fd-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="235fd-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="235fd-145">OUTPUTS</span></span>

### <span data-ttu-id="235fd-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="235fd-146">System.Boolean</span></span>

## <span data-ttu-id="235fd-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="235fd-147">NOTES</span></span>

## <span data-ttu-id="235fd-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="235fd-148">RELATED LINKS</span></span>
