---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: 7f6a7225742356e0410d3cc49aef60e50e1954a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888649"
---
# <span data-ttu-id="f73d2-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="f73d2-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="f73d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f73d2-102">SYNOPSIS</span></span>
<span data-ttu-id="f73d2-103">Remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="f73d2-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="f73d2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f73d2-104">SYNTAX</span></span>

### <span data-ttu-id="f73d2-105">NamespacePropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f73d2-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f73d2-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f73d2-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f73d2-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f73d2-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f73d2-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f73d2-108">DESCRIPTION</span></span>
<span data-ttu-id="f73d2-109">O cmdlet **Remove-AzServiceBusNamespace** remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="f73d2-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="f73d2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f73d2-110">EXAMPLES</span></span>

### <span data-ttu-id="f73d2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f73d2-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="f73d2-112">Remove o namespace de Barramento `SB-Example1` de Serviço do grupo de recursos `Default-ServiceBus-WestUS` especificado.</span><span class="sxs-lookup"><span data-stu-id="f73d2-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="f73d2-113">Exemplo 2.1 - InputObject - Usando variável:</span><span class="sxs-lookup"><span data-stu-id="f73d2-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="f73d2-114">Remove o namespace de Barramento de Serviço fornecido por meio do $inputobject.</span><span class="sxs-lookup"><span data-stu-id="f73d2-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="f73d2-115">Exemplo 2.2 - InputObject - Usando a canalização:</span><span class="sxs-lookup"><span data-stu-id="f73d2-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="f73d2-116">Remove o namespace de Barramento de Serviço usando Piping.</span><span class="sxs-lookup"><span data-stu-id="f73d2-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="f73d2-117">Exemplo 3 - ResourceId</span><span class="sxs-lookup"><span data-stu-id="f73d2-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="f73d2-118">Remove o namespace de Barramento de Serviço fornecido ARM id no $resourceid para -ResourceId ou por meio de canalização.</span><span class="sxs-lookup"><span data-stu-id="f73d2-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="f73d2-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f73d2-119">PARAMETERS</span></span>

### <span data-ttu-id="f73d2-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f73d2-120">-AsJob</span></span>
<span data-ttu-id="f73d2-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f73d2-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f73d2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f73d2-122">-DefaultProfile</span></span>
<span data-ttu-id="f73d2-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f73d2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f73d2-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f73d2-124">-InputObject</span></span>
<span data-ttu-id="f73d2-125">Objeto Namespace do Barramento de Serviço</span><span class="sxs-lookup"><span data-stu-id="f73d2-125">Service Bus Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f73d2-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f73d2-126">-Name</span></span>
<span data-ttu-id="f73d2-127">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="f73d2-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f73d2-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f73d2-128">-PassThru</span></span>
<span data-ttu-id="f73d2-129">Especificar isso retornará true se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f73d2-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f73d2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f73d2-130">-ResourceGroupName</span></span>
<span data-ttu-id="f73d2-131">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f73d2-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f73d2-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f73d2-132">-ResourceId</span></span>
<span data-ttu-id="f73d2-133">ID do Recurso de Namespace de Barramento de Serviço</span><span class="sxs-lookup"><span data-stu-id="f73d2-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="f73d2-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f73d2-134">-Confirm</span></span>
<span data-ttu-id="f73d2-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f73d2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f73d2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f73d2-136">-WhatIf</span></span>
<span data-ttu-id="f73d2-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f73d2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f73d2-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f73d2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f73d2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f73d2-139">CommonParameters</span></span>
<span data-ttu-id="f73d2-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f73d2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f73d2-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f73d2-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f73d2-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f73d2-142">INPUTS</span></span>

### <span data-ttu-id="f73d2-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f73d2-143">System.String</span></span>

### <span data-ttu-id="f73d2-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f73d2-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="f73d2-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f73d2-145">OUTPUTS</span></span>

### <span data-ttu-id="f73d2-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f73d2-146">System.Boolean</span></span>

## <span data-ttu-id="f73d2-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="f73d2-147">NOTES</span></span>

## <span data-ttu-id="f73d2-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f73d2-148">RELATED LINKS</span></span>
