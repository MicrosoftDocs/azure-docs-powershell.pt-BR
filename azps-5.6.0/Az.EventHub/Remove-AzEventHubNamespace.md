---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: dca9094ac66e889b5a00899f6d48d6317279c1fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885876"
---
# <span data-ttu-id="cf84c-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="cf84c-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="cf84c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf84c-102">SYNOPSIS</span></span>
<span data-ttu-id="cf84c-103">Remove o namespace de Hubs de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="cf84c-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="cf84c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cf84c-104">SYNTAX</span></span>

### <span data-ttu-id="cf84c-105">NamespaceParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cf84c-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf84c-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cf84c-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf84c-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf84c-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf84c-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cf84c-108">DESCRIPTION</span></span>
<span data-ttu-id="cf84c-109">O Remove-AzEventHubNamespace cmdlet remove e exclui o namespace de Hubs de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="cf84c-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="cf84c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf84c-110">EXAMPLES</span></span>

### <span data-ttu-id="cf84c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cf84c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="cf84c-112">Remove o namespace Hubs de Eventos \` MyNamespaceName no grupo \` de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="cf84c-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="cf84c-113">Exemplo 2: InputObject - Usando Variável:</span><span class="sxs-lookup"><span data-stu-id="cf84c-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="cf84c-114">Exemplo 3: InputObject - Usando a canalização:</span><span class="sxs-lookup"><span data-stu-id="cf84c-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="cf84c-115">Exemplo 4: ResourceId - Usando Variável</span><span class="sxs-lookup"><span data-stu-id="cf84c-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="cf84c-116">Exemplo 5: ResourceId - Usando a canalização:</span><span class="sxs-lookup"><span data-stu-id="cf84c-116">Example 5: ResourceId - Using Piping:</span></span>
```powershell
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="cf84c-117">Exemplo 6: ResourceId - Usando cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="cf84c-117">Example 6: ResourceId - Using String:</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="cf84c-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cf84c-118">PARAMETERS</span></span>

### <span data-ttu-id="cf84c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf84c-119">-AsJob</span></span>
<span data-ttu-id="cf84c-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cf84c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf84c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf84c-121">-DefaultProfile</span></span>
<span data-ttu-id="cf84c-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf84c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf84c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf84c-123">-InputObject</span></span>
<span data-ttu-id="cf84c-124">Objeto Namespace EventHubs</span><span class="sxs-lookup"><span data-stu-id="cf84c-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="cf84c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="cf84c-125">-Name</span></span>
<span data-ttu-id="cf84c-126">Nome do Namespace EventHub</span><span class="sxs-lookup"><span data-stu-id="cf84c-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="cf84c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf84c-127">-PassThru</span></span>
<span data-ttu-id="cf84c-128">Especificar isso retornará true se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="cf84c-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="cf84c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf84c-129">-ResourceGroupName</span></span>
<span data-ttu-id="cf84c-130">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="cf84c-130">Resource Group Name</span></span>

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

### <span data-ttu-id="cf84c-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf84c-131">-ResourceId</span></span>
<span data-ttu-id="cf84c-132">ID do Recurso namespace EventHubs</span><span class="sxs-lookup"><span data-stu-id="cf84c-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="cf84c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf84c-133">-Confirm</span></span>
<span data-ttu-id="cf84c-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf84c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf84c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf84c-135">-WhatIf</span></span>
<span data-ttu-id="cf84c-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cf84c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf84c-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cf84c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf84c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf84c-138">CommonParameters</span></span>
<span data-ttu-id="cf84c-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf84c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf84c-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf84c-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf84c-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf84c-141">INPUTS</span></span>

### <span data-ttu-id="cf84c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="cf84c-142">System.String</span></span>

### <span data-ttu-id="cf84c-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="cf84c-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="cf84c-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cf84c-144">OUTPUTS</span></span>

### <span data-ttu-id="cf84c-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="cf84c-145">System.Void</span></span>

## <span data-ttu-id="cf84c-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="cf84c-146">NOTES</span></span>

## <span data-ttu-id="cf84c-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf84c-147">RELATED LINKS</span></span>
