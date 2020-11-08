---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: daa63859c9649d9467f750f77d5b0e466d03ff56
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112236"
---
# <span data-ttu-id="28c0c-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="28c0c-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="28c0c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28c0c-102">SYNOPSIS</span></span>
<span data-ttu-id="28c0c-103">Remove o Hub de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="28c0c-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="28c0c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28c0c-104">SYNTAX</span></span>

### <span data-ttu-id="28c0c-105">EventhubDefaultSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="28c0c-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28c0c-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="28c0c-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28c0c-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28c0c-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28c0c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="28c0c-108">DESCRIPTION</span></span>
<span data-ttu-id="28c0c-109">O cmdlet Remove-AzEventHub remove e exclui o Hub de eventos especificado do namespace fornecido.</span><span class="sxs-lookup"><span data-stu-id="28c0c-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="28c0c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28c0c-110">EXAMPLES</span></span>

### <span data-ttu-id="28c0c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="28c0c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="28c0c-112">Remove o Hub de eventos \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="28c0c-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="28c0c-113">Exemplo 2: InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="28c0c-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="28c0c-114">Exemplo 3: InputObject usando o encanamento:</span><span class="sxs-lookup"><span data-stu-id="28c0c-114">Example 3: InputObject Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="28c0c-115">Exemplo 4: ResourceId-usando a variável:</span><span class="sxs-lookup"><span data-stu-id="28c0c-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="28c0c-116">Exemplo 5: ResourceId-usando cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="28c0c-116">Example 5: ResourceId - Using string:</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="28c0c-117">OS</span><span class="sxs-lookup"><span data-stu-id="28c0c-117">PARAMETERS</span></span>

### <span data-ttu-id="28c0c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28c0c-118">-AsJob</span></span>
<span data-ttu-id="28c0c-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="28c0c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28c0c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28c0c-120">-DefaultProfile</span></span>
<span data-ttu-id="28c0c-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28c0c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28c0c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28c0c-122">-InputObject</span></span>
<span data-ttu-id="28c0c-123">Objeto do Eventhub</span><span class="sxs-lookup"><span data-stu-id="28c0c-123">Eventhub Object</span></span>

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

### <span data-ttu-id="28c0c-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="28c0c-124">-Name</span></span>
<span data-ttu-id="28c0c-125">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="28c0c-125">EventHub Name</span></span>

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

### <span data-ttu-id="28c0c-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="28c0c-126">-Namespace</span></span>
<span data-ttu-id="28c0c-127">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="28c0c-127">Namespace Name</span></span>

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

### <span data-ttu-id="28c0c-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28c0c-128">-PassThru</span></span>
<span data-ttu-id="28c0c-129">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="28c0c-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="28c0c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28c0c-130">-ResourceGroupName</span></span>
<span data-ttu-id="28c0c-131">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="28c0c-131">Resource Group Name</span></span>

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

### <span data-ttu-id="28c0c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28c0c-132">-ResourceId</span></span>
<span data-ttu-id="28c0c-133">ID do recurso do Eventhub</span><span class="sxs-lookup"><span data-stu-id="28c0c-133">Eventhub Resource Id</span></span>

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

### <span data-ttu-id="28c0c-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="28c0c-134">-Confirm</span></span>
<span data-ttu-id="28c0c-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28c0c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28c0c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28c0c-136">-WhatIf</span></span>
<span data-ttu-id="28c0c-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="28c0c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28c0c-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="28c0c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28c0c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28c0c-139">CommonParameters</span></span>
<span data-ttu-id="28c0c-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28c0c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28c0c-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28c0c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28c0c-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="28c0c-142">INPUTS</span></span>

### <span data-ttu-id="28c0c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="28c0c-143">System.String</span></span>

### <span data-ttu-id="28c0c-144">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="28c0c-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="28c0c-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="28c0c-145">OUTPUTS</span></span>

### <span data-ttu-id="28c0c-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="28c0c-146">System.Boolean</span></span>

## <span data-ttu-id="28c0c-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="28c0c-147">NOTES</span></span>

## <span data-ttu-id="28c0c-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28c0c-148">RELATED LINKS</span></span>
