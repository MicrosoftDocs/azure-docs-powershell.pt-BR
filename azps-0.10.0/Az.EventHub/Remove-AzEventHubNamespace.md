---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 38a727c2e632173befe6b5b08756d558a9c9f177
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775865"
---
# <span data-ttu-id="018dc-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="018dc-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="018dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="018dc-102">SYNOPSIS</span></span>
<span data-ttu-id="018dc-103">Remove o namespace especificado dos hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="018dc-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="018dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="018dc-104">SYNTAX</span></span>

### <span data-ttu-id="018dc-105">NamespaceParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="018dc-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="018dc-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="018dc-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="018dc-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="018dc-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="018dc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="018dc-108">DESCRIPTION</span></span>
<span data-ttu-id="018dc-109">O cmdlet Remove-AzEventHubNamespace remove e exclui o namespace de hubs de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="018dc-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="018dc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="018dc-110">EXAMPLES</span></span>

### <span data-ttu-id="018dc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="018dc-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="018dc-112">Remove o namespace de hubs de evento \` Mynamespacename \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="018dc-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="018dc-113">Exemplo 2,1-InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="018dc-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="018dc-114">Exemplo 2,1-InputObject-usando o encanamento:</span><span class="sxs-lookup"><span data-stu-id="018dc-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="018dc-115">Exemplo 3,1-ResourceId-usando variável</span><span class="sxs-lookup"><span data-stu-id="018dc-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="018dc-116">Exemplo 3,2-ResourceId-usando o encanamento:</span><span class="sxs-lookup"><span data-stu-id="018dc-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="018dc-117">Exemplo 3,3-ResourceId-usando cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="018dc-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="018dc-118">OS</span><span class="sxs-lookup"><span data-stu-id="018dc-118">PARAMETERS</span></span>

### <span data-ttu-id="018dc-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="018dc-119">-AsJob</span></span>
<span data-ttu-id="018dc-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="018dc-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="018dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="018dc-121">-DefaultProfile</span></span>
<span data-ttu-id="018dc-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="018dc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="018dc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="018dc-123">-InputObject</span></span>
<span data-ttu-id="018dc-124">Objeto namespace EventHubs</span><span class="sxs-lookup"><span data-stu-id="018dc-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="018dc-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="018dc-125">-Name</span></span>
<span data-ttu-id="018dc-126">Nome do namespace do EventHub</span><span class="sxs-lookup"><span data-stu-id="018dc-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="018dc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="018dc-127">-PassThru</span></span>
<span data-ttu-id="018dc-128">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="018dc-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="018dc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="018dc-129">-ResourceGroupName</span></span>
<span data-ttu-id="018dc-130">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="018dc-130">Resource Group Name</span></span>

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

### <span data-ttu-id="018dc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="018dc-131">-ResourceId</span></span>
<span data-ttu-id="018dc-132">ID do recurso namespace EventHubs</span><span class="sxs-lookup"><span data-stu-id="018dc-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="018dc-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="018dc-133">-Confirm</span></span>
<span data-ttu-id="018dc-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="018dc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="018dc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="018dc-135">-WhatIf</span></span>
<span data-ttu-id="018dc-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="018dc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="018dc-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="018dc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="018dc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="018dc-138">CommonParameters</span></span>
<span data-ttu-id="018dc-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="018dc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="018dc-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="018dc-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="018dc-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="018dc-141">INPUTS</span></span>

### <span data-ttu-id="018dc-142">System. String</span><span class="sxs-lookup"><span data-stu-id="018dc-142">System.String</span></span>

### <span data-ttu-id="018dc-143">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="018dc-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="018dc-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="018dc-144">OUTPUTS</span></span>

### <span data-ttu-id="018dc-145">System. void</span><span class="sxs-lookup"><span data-stu-id="018dc-145">System.Void</span></span>

## <span data-ttu-id="018dc-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="018dc-146">NOTES</span></span>

## <span data-ttu-id="018dc-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="018dc-147">RELATED LINKS</span></span>
