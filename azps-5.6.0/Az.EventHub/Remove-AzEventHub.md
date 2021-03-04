---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: 2d3f2ee9a4dc55dd709be3113770df402434c911
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890634"
---
# <span data-ttu-id="6e7f9-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="6e7f9-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="6e7f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e7f9-102">SYNOPSIS</span></span>
<span data-ttu-id="6e7f9-103">Remove o Hub de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="6e7f9-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="6e7f9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6e7f9-104">SYNTAX</span></span>

### <span data-ttu-id="6e7f9-105">EventhubDefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6e7f9-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e7f9-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6e7f9-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e7f9-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e7f9-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e7f9-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6e7f9-108">DESCRIPTION</span></span>
<span data-ttu-id="6e7f9-109">O Remove-AzEventHub cmdlet remove e exclui o Hub de Eventos especificado do namespace determinado.</span><span class="sxs-lookup"><span data-stu-id="6e7f9-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="6e7f9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e7f9-110">EXAMPLES</span></span>

### <span data-ttu-id="6e7f9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6e7f9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="6e7f9-112">Remove o Hub de Eventos \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="6e7f9-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="6e7f9-113">Exemplo 2: InputObject - Usando Variável:</span><span class="sxs-lookup"><span data-stu-id="6e7f9-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="6e7f9-114">Exemplo 3: InputObject usando a canalização:</span><span class="sxs-lookup"><span data-stu-id="6e7f9-114">Example 3: InputObject Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="6e7f9-115">Exemplo 4: ResourceId - Usando Variável:</span><span class="sxs-lookup"><span data-stu-id="6e7f9-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="6e7f9-116">Exemplo 5: ResourceId - Usando cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="6e7f9-116">Example 5: ResourceId - Using string:</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="6e7f9-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6e7f9-117">PARAMETERS</span></span>

### <span data-ttu-id="6e7f9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e7f9-118">-AsJob</span></span>
<span data-ttu-id="6e7f9-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6e7f9-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e7f9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e7f9-120">-DefaultProfile</span></span>
<span data-ttu-id="6e7f9-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e7f9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e7f9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e7f9-122">-InputObject</span></span>
<span data-ttu-id="6e7f9-123">Objeto Eventhub</span><span class="sxs-lookup"><span data-stu-id="6e7f9-123">Eventhub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7f9-124">-Name</span><span class="sxs-lookup"><span data-stu-id="6e7f9-124">-Name</span></span>
<span data-ttu-id="6e7f9-125">Nome eventHub</span><span class="sxs-lookup"><span data-stu-id="6e7f9-125">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7f9-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6e7f9-126">-Namespace</span></span>
<span data-ttu-id="6e7f9-127">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="6e7f9-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7f9-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e7f9-128">-PassThru</span></span>
<span data-ttu-id="6e7f9-129">Especificar isso retornará true se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6e7f9-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="6e7f9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e7f9-130">-ResourceGroupName</span></span>
<span data-ttu-id="6e7f9-131">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="6e7f9-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7f9-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e7f9-132">-ResourceId</span></span>
<span data-ttu-id="6e7f9-133">ID de Recurso Eventhub</span><span class="sxs-lookup"><span data-stu-id="6e7f9-133">Eventhub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7f9-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e7f9-134">-Confirm</span></span>
<span data-ttu-id="6e7f9-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e7f9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e7f9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e7f9-136">-WhatIf</span></span>
<span data-ttu-id="6e7f9-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6e7f9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e7f9-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6e7f9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e7f9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e7f9-139">CommonParameters</span></span>
<span data-ttu-id="6e7f9-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e7f9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e7f9-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e7f9-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e7f9-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e7f9-142">INPUTS</span></span>

### <span data-ttu-id="6e7f9-143">System.String</span><span class="sxs-lookup"><span data-stu-id="6e7f9-143">System.String</span></span>

### <span data-ttu-id="6e7f9-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="6e7f9-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="6e7f9-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6e7f9-145">OUTPUTS</span></span>

### <span data-ttu-id="6e7f9-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6e7f9-146">System.Boolean</span></span>

## <span data-ttu-id="6e7f9-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="6e7f9-147">NOTES</span></span>

## <span data-ttu-id="6e7f9-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e7f9-148">RELATED LINKS</span></span>
