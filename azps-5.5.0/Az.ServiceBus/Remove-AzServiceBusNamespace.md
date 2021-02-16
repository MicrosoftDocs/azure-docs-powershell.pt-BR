---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: 49b6a29410bd6c670e74b072a48b6f2a79e8fd0f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113994"
---
# <span data-ttu-id="05108-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="05108-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="05108-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="05108-102">SYNOPSIS</span></span>
<span data-ttu-id="05108-103">Remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="05108-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="05108-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05108-104">SYNTAX</span></span>

### <span data-ttu-id="05108-105">NamespacePropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="05108-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05108-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="05108-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05108-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05108-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05108-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="05108-108">DESCRIPTION</span></span>
<span data-ttu-id="05108-109">O cmdlet **Remove-AzServiceBusNamespace** remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="05108-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="05108-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="05108-110">EXAMPLES</span></span>

### <span data-ttu-id="05108-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="05108-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="05108-112">Remove o namespace da Barra de Serviços `SB-Example1` do grupo de recursos `Default-ServiceBus-WestUS` especificado.</span><span class="sxs-lookup"><span data-stu-id="05108-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="05108-113">Exemplo 2.1 - InputObject - Usando variável:</span><span class="sxs-lookup"><span data-stu-id="05108-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="05108-114">Remove o namespace de Service Bus fornecido por meio do $inputobject.</span><span class="sxs-lookup"><span data-stu-id="05108-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="05108-115">Exemplo 2.2 - InputObject - Usando a piping:</span><span class="sxs-lookup"><span data-stu-id="05108-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="05108-116">Remove o namespace da Barra de Serviços usando a Piping.</span><span class="sxs-lookup"><span data-stu-id="05108-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="05108-117">Exemplo 3 - ResourceId</span><span class="sxs-lookup"><span data-stu-id="05108-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="05108-118">Remove o namespace de Barra de Serviço fornecido por meio da ID arm $resourceid parâmetro -ResourceId ou por meio de piping.</span><span class="sxs-lookup"><span data-stu-id="05108-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="05108-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05108-119">PARAMETERS</span></span>

### <span data-ttu-id="05108-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05108-120">-AsJob</span></span>
<span data-ttu-id="05108-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="05108-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05108-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05108-122">-DefaultProfile</span></span>
<span data-ttu-id="05108-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="05108-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05108-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05108-124">-InputObject</span></span>
<span data-ttu-id="05108-125">Objeto Namespace da Barra de Serviços</span><span class="sxs-lookup"><span data-stu-id="05108-125">Service Bus Namespace Object</span></span>

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

### <span data-ttu-id="05108-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="05108-126">-Name</span></span>
<span data-ttu-id="05108-127">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="05108-127">Namespace Name.</span></span>

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

### <span data-ttu-id="05108-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05108-128">-PassThru</span></span>
<span data-ttu-id="05108-129">Especificar isso retornará verdadeiro se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="05108-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="05108-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05108-130">-ResourceGroupName</span></span>
<span data-ttu-id="05108-131">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="05108-131">The name of the resource group</span></span>

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

### <span data-ttu-id="05108-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05108-132">-ResourceId</span></span>
<span data-ttu-id="05108-133">ID do Recurso Namespace do Barramento de Serviço</span><span class="sxs-lookup"><span data-stu-id="05108-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="05108-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="05108-134">-Confirm</span></span>
<span data-ttu-id="05108-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05108-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05108-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05108-136">-WhatIf</span></span>
<span data-ttu-id="05108-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="05108-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05108-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="05108-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05108-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05108-139">CommonParameters</span></span>
<span data-ttu-id="05108-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05108-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05108-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05108-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05108-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="05108-142">INPUTS</span></span>

### <span data-ttu-id="05108-143">System.String</span><span class="sxs-lookup"><span data-stu-id="05108-143">System.String</span></span>

### <span data-ttu-id="05108-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="05108-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="05108-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="05108-145">OUTPUTS</span></span>

### <span data-ttu-id="05108-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="05108-146">System.Boolean</span></span>

## <span data-ttu-id="05108-147">Notas</span><span class="sxs-lookup"><span data-stu-id="05108-147">NOTES</span></span>

## <span data-ttu-id="05108-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05108-148">RELATED LINKS</span></span>
