---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: c226f11eecc7cf046234378be7f0417da301cf40
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116540"
---
# <span data-ttu-id="f5575-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5575-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="f5575-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5575-102">SYNOPSIS</span></span>
<span data-ttu-id="f5575-103">Exclui um alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="f5575-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f5575-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5575-104">SYNTAX</span></span>

### <span data-ttu-id="f5575-105">GeoDRPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f5575-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5575-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f5575-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5575-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5575-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5575-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5575-108">DESCRIPTION</span></span>
<span data-ttu-id="f5575-109">O cmdlet **Remove-AzServiceBusGeoDRConfiguration** exclui um alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="f5575-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f5575-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5575-110">EXAMPLES</span></span>

### <span data-ttu-id="f5575-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f5575-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="f5575-112">Exclui um alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="f5575-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f5575-113">OS</span><span class="sxs-lookup"><span data-stu-id="f5575-113">PARAMETERS</span></span>

### <span data-ttu-id="f5575-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5575-114">-AsJob</span></span>
<span data-ttu-id="f5575-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f5575-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5575-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5575-116">-DefaultProfile</span></span>
<span data-ttu-id="f5575-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5575-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5575-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5575-118">-InputObject</span></span>
<span data-ttu-id="f5575-119">Objeto de configuração do barramento do serviço GeoDR</span><span class="sxs-lookup"><span data-stu-id="f5575-119">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5575-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5575-120">-Name</span></span>
<span data-ttu-id="f5575-121">Nome do alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="f5575-121">Alias (GeoDR) Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5575-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f5575-122">-Namespace</span></span>
<span data-ttu-id="f5575-123">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="f5575-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5575-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5575-124">-PassThru</span></span>
<span data-ttu-id="f5575-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="f5575-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f5575-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f5575-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f5575-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5575-127">-ResourceGroupName</span></span>
<span data-ttu-id="f5575-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f5575-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5575-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5575-129">-ResourceId</span></span>
<span data-ttu-id="f5575-130">ID do recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5575-130">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5575-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f5575-131">-Confirm</span></span>
<span data-ttu-id="f5575-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5575-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5575-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5575-133">-WhatIf</span></span>
<span data-ttu-id="f5575-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f5575-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5575-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5575-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5575-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5575-136">CommonParameters</span></span>
<span data-ttu-id="f5575-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5575-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5575-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5575-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5575-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5575-139">INPUTS</span></span>

### <span data-ttu-id="f5575-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f5575-140">System.String</span></span>

### <span data-ttu-id="f5575-141">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="f5575-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="f5575-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5575-142">OUTPUTS</span></span>

### <span data-ttu-id="f5575-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5575-143">System.Boolean</span></span>

## <span data-ttu-id="f5575-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5575-144">NOTES</span></span>

## <span data-ttu-id="f5575-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5575-145">RELATED LINKS</span></span>
