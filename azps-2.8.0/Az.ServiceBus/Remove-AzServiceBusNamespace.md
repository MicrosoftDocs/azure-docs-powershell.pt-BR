---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: b17fa7309274f261c329eaf896519f8bb70d06fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773227"
---
# <span data-ttu-id="c3d88-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="c3d88-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="c3d88-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3d88-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d88-103">Remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="c3d88-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="c3d88-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3d88-104">SYNTAX</span></span>

### <span data-ttu-id="c3d88-105">NamespacePropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c3d88-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3d88-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c3d88-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3d88-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3d88-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3d88-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3d88-108">DESCRIPTION</span></span>
<span data-ttu-id="c3d88-109">O cmdlet **Remove-AzServiceBusNamespace** remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="c3d88-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="c3d88-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3d88-110">EXAMPLES</span></span>

### <span data-ttu-id="c3d88-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c3d88-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="c3d88-112">Remove o namespace de barramento do serviço `SB-Example1` do grupo de recursos especificado `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="c3d88-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="c3d88-113">Exemplo 2,1-InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="c3d88-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="c3d88-114">Remove o namespace de barramento de serviço fornecido por meio da $inputobject.</span><span class="sxs-lookup"><span data-stu-id="c3d88-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="c3d88-115">Exemplo 2,2-InputObject-usando o encanamento:</span><span class="sxs-lookup"><span data-stu-id="c3d88-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="c3d88-116">Remove o namespace de barramento do serviço usando o encanamento.</span><span class="sxs-lookup"><span data-stu-id="c3d88-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="c3d88-117">Exemplo de 3-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3d88-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="c3d88-118">Remove o namespace de barramento de serviço fornecido por meio do ID ARM no parâmetro $resourceid para-ResourceId ou por meio do encanamento.</span><span class="sxs-lookup"><span data-stu-id="c3d88-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="c3d88-119">OS</span><span class="sxs-lookup"><span data-stu-id="c3d88-119">PARAMETERS</span></span>

### <span data-ttu-id="c3d88-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3d88-120">-AsJob</span></span>
<span data-ttu-id="c3d88-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c3d88-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3d88-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d88-122">-DefaultProfile</span></span>
<span data-ttu-id="c3d88-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3d88-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3d88-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3d88-124">-InputObject</span></span>
<span data-ttu-id="c3d88-125">Objeto namespace do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="c3d88-125">Service Bus Namespace Object</span></span>

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

### <span data-ttu-id="c3d88-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3d88-126">-Name</span></span>
<span data-ttu-id="c3d88-127">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="c3d88-127">Namespace Name.</span></span>

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

### <span data-ttu-id="c3d88-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3d88-128">-PassThru</span></span>
<span data-ttu-id="c3d88-129">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c3d88-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c3d88-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3d88-130">-ResourceGroupName</span></span>
<span data-ttu-id="c3d88-131">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c3d88-131">The name of the resource group</span></span>

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

### <span data-ttu-id="c3d88-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3d88-132">-ResourceId</span></span>
<span data-ttu-id="c3d88-133">ID do recurso namespace do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="c3d88-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="c3d88-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c3d88-134">-Confirm</span></span>
<span data-ttu-id="c3d88-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3d88-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3d88-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3d88-136">-WhatIf</span></span>
<span data-ttu-id="c3d88-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c3d88-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3d88-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c3d88-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3d88-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d88-139">CommonParameters</span></span>
<span data-ttu-id="c3d88-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3d88-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d88-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3d88-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d88-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3d88-142">INPUTS</span></span>

### <span data-ttu-id="c3d88-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c3d88-143">System.String</span></span>

### <span data-ttu-id="c3d88-144">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c3d88-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="c3d88-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3d88-145">OUTPUTS</span></span>

### <span data-ttu-id="c3d88-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c3d88-146">System.Boolean</span></span>

## <span data-ttu-id="c3d88-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3d88-147">NOTES</span></span>

## <span data-ttu-id="c3d88-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3d88-148">RELATED LINKS</span></span>
