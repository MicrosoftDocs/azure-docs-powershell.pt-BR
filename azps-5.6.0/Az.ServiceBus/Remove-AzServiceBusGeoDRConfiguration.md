---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 3fa1dd4c3f926e0c6011d8ffec3a510340a7eab3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891617"
---
# <span data-ttu-id="5646f-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="5646f-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="5646f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5646f-102">SYNOPSIS</span></span>
<span data-ttu-id="5646f-103">Exclui um Alias(Configuração de Recuperação de Desastre)</span><span class="sxs-lookup"><span data-stu-id="5646f-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="5646f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5646f-104">SYNTAX</span></span>

### <span data-ttu-id="5646f-105">GeoDRPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5646f-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5646f-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5646f-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5646f-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5646f-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5646f-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5646f-108">DESCRIPTION</span></span>
<span data-ttu-id="5646f-109">O cmdlet **Remove-AzServiceBusGeoDRConfiguration** exclui um Alias(Disaster Recovery configuration)</span><span class="sxs-lookup"><span data-stu-id="5646f-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="5646f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5646f-110">EXAMPLES</span></span>

### <span data-ttu-id="5646f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5646f-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="5646f-112">Exclui um Alias(Configuração de Recuperação de Desastre)</span><span class="sxs-lookup"><span data-stu-id="5646f-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="5646f-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5646f-113">PARAMETERS</span></span>

### <span data-ttu-id="5646f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5646f-114">-AsJob</span></span>
<span data-ttu-id="5646f-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5646f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5646f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5646f-116">-DefaultProfile</span></span>
<span data-ttu-id="5646f-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5646f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5646f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5646f-118">-InputObject</span></span>
<span data-ttu-id="5646f-119">Objeto de configuração geográfica do Barramento de Serviço</span><span class="sxs-lookup"><span data-stu-id="5646f-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="5646f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5646f-120">-Name</span></span>
<span data-ttu-id="5646f-121">Alias (GeoDR) Name</span><span class="sxs-lookup"><span data-stu-id="5646f-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="5646f-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5646f-122">-Namespace</span></span>
<span data-ttu-id="5646f-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="5646f-123">Namespace Name</span></span>

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

### <span data-ttu-id="5646f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5646f-124">-PassThru</span></span>
<span data-ttu-id="5646f-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="5646f-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5646f-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="5646f-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5646f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5646f-127">-ResourceGroupName</span></span>
<span data-ttu-id="5646f-128">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="5646f-128">Resource Group Name</span></span>

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

### <span data-ttu-id="5646f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5646f-129">-ResourceId</span></span>
<span data-ttu-id="5646f-130">ID do Recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="5646f-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="5646f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5646f-131">-Confirm</span></span>
<span data-ttu-id="5646f-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5646f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5646f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5646f-133">-WhatIf</span></span>
<span data-ttu-id="5646f-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5646f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5646f-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5646f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5646f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5646f-136">CommonParameters</span></span>
<span data-ttu-id="5646f-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5646f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5646f-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5646f-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5646f-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5646f-139">INPUTS</span></span>

### <span data-ttu-id="5646f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5646f-140">System.String</span></span>

### <span data-ttu-id="5646f-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="5646f-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="5646f-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5646f-142">OUTPUTS</span></span>

### <span data-ttu-id="5646f-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5646f-143">System.Boolean</span></span>

## <span data-ttu-id="5646f-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="5646f-144">NOTES</span></span>

## <span data-ttu-id="5646f-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5646f-145">RELATED LINKS</span></span>
