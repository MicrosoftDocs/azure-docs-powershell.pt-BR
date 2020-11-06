---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 4d5ddbc4dff2922b90bc6d1117ff32473afd9042
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600828"
---
# <span data-ttu-id="ae215-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="ae215-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="ae215-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae215-102">SYNOPSIS</span></span>
<span data-ttu-id="ae215-103">Remove o namespace especificado dos hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="ae215-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="ae215-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae215-104">SYNTAX</span></span>

### <span data-ttu-id="ae215-105">NamespaceParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ae215-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae215-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ae215-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae215-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae215-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae215-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae215-108">DESCRIPTION</span></span>
<span data-ttu-id="ae215-109">O cmdlet Remove-AzEventHubNamespace remove e exclui o namespace de hubs de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="ae215-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="ae215-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae215-110">EXAMPLES</span></span>

### <span data-ttu-id="ae215-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ae215-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="ae215-112">Remove o namespace de hubs de evento \` Mynamespacename \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="ae215-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ae215-113">Exemplo 2,1-InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="ae215-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="ae215-114">Exemplo 2,1-InputObject-usando o encanamento:</span><span class="sxs-lookup"><span data-stu-id="ae215-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="ae215-115">Exemplo 3,1-ResourceId-usando variável</span><span class="sxs-lookup"><span data-stu-id="ae215-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="ae215-116">Exemplo 3,2-ResourceId-usando o encanamento:</span><span class="sxs-lookup"><span data-stu-id="ae215-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="ae215-117">Exemplo 3,3-ResourceId-usando cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="ae215-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="ae215-118">OS</span><span class="sxs-lookup"><span data-stu-id="ae215-118">PARAMETERS</span></span>

### <span data-ttu-id="ae215-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae215-119">-AsJob</span></span>
<span data-ttu-id="ae215-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ae215-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae215-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae215-121">-DefaultProfile</span></span>
<span data-ttu-id="ae215-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae215-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae215-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae215-123">-InputObject</span></span>
<span data-ttu-id="ae215-124">Objeto namespace EventHubs</span><span class="sxs-lookup"><span data-stu-id="ae215-124">EventHubs Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae215-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae215-125">-Name</span></span>
<span data-ttu-id="ae215-126">Nome do namespace do EventHub</span><span class="sxs-lookup"><span data-stu-id="ae215-126">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae215-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae215-127">-PassThru</span></span>
<span data-ttu-id="ae215-128">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ae215-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="ae215-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae215-129">-ResourceGroupName</span></span>
<span data-ttu-id="ae215-130">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ae215-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae215-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae215-131">-ResourceId</span></span>
<span data-ttu-id="ae215-132">ID do recurso namespace EventHubs</span><span class="sxs-lookup"><span data-stu-id="ae215-132">EventHubs Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae215-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ae215-133">-Confirm</span></span>
<span data-ttu-id="ae215-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae215-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae215-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae215-135">-WhatIf</span></span>
<span data-ttu-id="ae215-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae215-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae215-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae215-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae215-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae215-138">CommonParameters</span></span>
<span data-ttu-id="ae215-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae215-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae215-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae215-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae215-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae215-141">INPUTS</span></span>

### <span data-ttu-id="ae215-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ae215-142">System.String</span></span>

### <span data-ttu-id="ae215-143">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ae215-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="ae215-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae215-144">OUTPUTS</span></span>

### <span data-ttu-id="ae215-145">System. void</span><span class="sxs-lookup"><span data-stu-id="ae215-145">System.Void</span></span>

## <span data-ttu-id="ae215-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae215-146">NOTES</span></span>

## <span data-ttu-id="ae215-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae215-147">RELATED LINKS</span></span>
