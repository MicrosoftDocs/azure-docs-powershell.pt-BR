---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 29f2b961637a398470f6455d0d2330ce5fd863a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116809"
---
# <span data-ttu-id="9f5c0-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="9f5c0-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="9f5c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f5c0-102">SYNOPSIS</span></span>
<span data-ttu-id="9f5c0-103">Remove o namespace de Hubs de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="9f5c0-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="9f5c0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f5c0-104">SYNTAX</span></span>

### <span data-ttu-id="9f5c0-105">NamespaceParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9f5c0-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f5c0-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9f5c0-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f5c0-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f5c0-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f5c0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f5c0-108">DESCRIPTION</span></span>
<span data-ttu-id="9f5c0-109">O Remove-AzEventHubNamespace cmdlet remove e exclui o namespace de Hubs de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="9f5c0-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="9f5c0-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9f5c0-110">EXAMPLES</span></span>

### <span data-ttu-id="9f5c0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9f5c0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="9f5c0-112">Remove o namespace myNamespaceName dos Hubs de Evento no grupo de \` \` recursos \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="9f5c0-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="9f5c0-113">Exemplo 2: InputObject - Usando Variável:</span><span class="sxs-lookup"><span data-stu-id="9f5c0-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="9f5c0-114">Exemplo 3: InputObject - Usando a piping:</span><span class="sxs-lookup"><span data-stu-id="9f5c0-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="9f5c0-115">Exemplo 4: ResourceId - Usando Variável</span><span class="sxs-lookup"><span data-stu-id="9f5c0-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="9f5c0-116">Exemplo 5: ResourceId - Usando a piping:</span><span class="sxs-lookup"><span data-stu-id="9f5c0-116">Example 5: ResourceId - Using Piping:</span></span>
```powershell
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="9f5c0-117">Exemplo 6: ResourceId - Usando cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="9f5c0-117">Example 6: ResourceId - Using String:</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="9f5c0-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f5c0-118">PARAMETERS</span></span>

### <span data-ttu-id="9f5c0-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f5c0-119">-AsJob</span></span>
<span data-ttu-id="9f5c0-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9f5c0-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f5c0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f5c0-121">-DefaultProfile</span></span>
<span data-ttu-id="9f5c0-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f5c0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f5c0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f5c0-123">-InputObject</span></span>
<span data-ttu-id="9f5c0-124">Objeto Namespace eventHubs</span><span class="sxs-lookup"><span data-stu-id="9f5c0-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="9f5c0-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f5c0-125">-Name</span></span>
<span data-ttu-id="9f5c0-126">Nome do Namespace do EventHub</span><span class="sxs-lookup"><span data-stu-id="9f5c0-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="9f5c0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f5c0-127">-PassThru</span></span>
<span data-ttu-id="9f5c0-128">Especificar isso retornará verdadeiro se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="9f5c0-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="9f5c0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f5c0-129">-ResourceGroupName</span></span>
<span data-ttu-id="9f5c0-130">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="9f5c0-130">Resource Group Name</span></span>

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

### <span data-ttu-id="9f5c0-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f5c0-131">-ResourceId</span></span>
<span data-ttu-id="9f5c0-132">ID do Recurso EventHubs Namespace</span><span class="sxs-lookup"><span data-stu-id="9f5c0-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="9f5c0-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9f5c0-133">-Confirm</span></span>
<span data-ttu-id="9f5c0-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f5c0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f5c0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f5c0-135">-WhatIf</span></span>
<span data-ttu-id="9f5c0-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9f5c0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f5c0-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9f5c0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f5c0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f5c0-138">CommonParameters</span></span>
<span data-ttu-id="9f5c0-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f5c0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f5c0-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f5c0-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f5c0-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="9f5c0-141">INPUTS</span></span>

### <span data-ttu-id="9f5c0-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9f5c0-142">System.String</span></span>

### <span data-ttu-id="9f5c0-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="9f5c0-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="9f5c0-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="9f5c0-144">OUTPUTS</span></span>

### <span data-ttu-id="9f5c0-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="9f5c0-145">System.Void</span></span>

## <span data-ttu-id="9f5c0-146">Notas</span><span class="sxs-lookup"><span data-stu-id="9f5c0-146">NOTES</span></span>

## <span data-ttu-id="9f5c0-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f5c0-147">RELATED LINKS</span></span>
