---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
ms.openlocfilehash: 6df8d5539bf340df5e00ad69ac557bc2cbb8ccaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430302"
---
# <span data-ttu-id="acf2f-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="acf2f-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="acf2f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="acf2f-102">SYNOPSIS</span></span>
<span data-ttu-id="acf2f-103">Remove o namespace especificado dos hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="acf2f-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acf2f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="acf2f-104">SYNTAX</span></span>

### <span data-ttu-id="acf2f-105">NamespaceParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="acf2f-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acf2f-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="acf2f-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acf2f-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="acf2f-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acf2f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="acf2f-108">DESCRIPTION</span></span>
<span data-ttu-id="acf2f-109">O cmdlet Remove-AzureRmEventHubNamespace remove e exclui o namespace de hubs de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="acf2f-109">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="acf2f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="acf2f-110">EXAMPLES</span></span>

### <span data-ttu-id="acf2f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="acf2f-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="acf2f-112">Remove o namespace de hubs de evento \` Mynamespacename \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="acf2f-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="acf2f-113">Exemplo 2,1-InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="acf2f-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzureRmEventHubNamespace <params> 
PS C:\> Remove-AzureRmEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="acf2f-114">Exemplo 2,1-InputObject-usando o encanamento:</span><span class="sxs-lookup"><span data-stu-id="acf2f-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace <params> | Remove-AzureRmEventHubNamespace
```

### <span data-ttu-id="acf2f-115">Exemplo 3,1-ResourceId-usando variável</span><span class="sxs-lookup"><span data-stu-id="acf2f-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHubNamespace <params>
PS C:\> Remove-AzureRmEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="acf2f-116">Exemplo 3,2-ResourceId-usando o encanamento:</span><span class="sxs-lookup"><span data-stu-id="acf2f-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzureRmResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzureRmEventHubNamespace
```

### <span data-ttu-id="acf2f-117">Exemplo 3,3-ResourceId-usando cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="acf2f-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="acf2f-118">OS</span><span class="sxs-lookup"><span data-stu-id="acf2f-118">PARAMETERS</span></span>

### <span data-ttu-id="acf2f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="acf2f-119">-AsJob</span></span>
<span data-ttu-id="acf2f-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="acf2f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="acf2f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf2f-121">-DefaultProfile</span></span>
<span data-ttu-id="acf2f-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="acf2f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acf2f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acf2f-123">-InputObject</span></span>
<span data-ttu-id="acf2f-124">Objeto namespace EventHubs</span><span class="sxs-lookup"><span data-stu-id="acf2f-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="acf2f-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="acf2f-125">-Name</span></span>
<span data-ttu-id="acf2f-126">Nome do namespace do EventHub</span><span class="sxs-lookup"><span data-stu-id="acf2f-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="acf2f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="acf2f-127">-PassThru</span></span>
<span data-ttu-id="acf2f-128">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="acf2f-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="acf2f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acf2f-129">-ResourceGroupName</span></span>
<span data-ttu-id="acf2f-130">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="acf2f-130">Resource Group Name</span></span>

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

### <span data-ttu-id="acf2f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acf2f-131">-ResourceId</span></span>
<span data-ttu-id="acf2f-132">ID do recurso namespace EventHubs</span><span class="sxs-lookup"><span data-stu-id="acf2f-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="acf2f-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="acf2f-133">-Confirm</span></span>
<span data-ttu-id="acf2f-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acf2f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acf2f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acf2f-135">-WhatIf</span></span>
<span data-ttu-id="acf2f-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="acf2f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acf2f-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="acf2f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acf2f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf2f-138">CommonParameters</span></span>
<span data-ttu-id="acf2f-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acf2f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf2f-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acf2f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf2f-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="acf2f-141">INPUTS</span></span>

### <span data-ttu-id="acf2f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="acf2f-142">System.String</span></span>

### <span data-ttu-id="acf2f-143">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="acf2f-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="acf2f-144">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="acf2f-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="acf2f-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="acf2f-145">OUTPUTS</span></span>

### <span data-ttu-id="acf2f-146">System. void</span><span class="sxs-lookup"><span data-stu-id="acf2f-146">System.Void</span></span>

## <span data-ttu-id="acf2f-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="acf2f-147">NOTES</span></span>

## <span data-ttu-id="acf2f-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="acf2f-148">RELATED LINKS</span></span>
