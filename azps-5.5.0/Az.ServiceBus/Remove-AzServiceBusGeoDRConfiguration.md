---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: c226f11eecc7cf046234378be7f0417da301cf40
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117128"
---
# <span data-ttu-id="78219-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="78219-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="78219-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78219-102">SYNOPSIS</span></span>
<span data-ttu-id="78219-103">Exclui um Alias(configuração de Recuperação de Desastres)</span><span class="sxs-lookup"><span data-stu-id="78219-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="78219-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78219-104">SYNTAX</span></span>

### <span data-ttu-id="78219-105">GeoDRPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="78219-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78219-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="78219-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78219-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78219-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78219-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="78219-108">DESCRIPTION</span></span>
<span data-ttu-id="78219-109">O cmdlet **Remove-AzServiceBusGeoDRConfiguration** exclui um Alias(configuração de Recuperação de Desastres)</span><span class="sxs-lookup"><span data-stu-id="78219-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="78219-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="78219-110">EXAMPLES</span></span>

### <span data-ttu-id="78219-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="78219-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="78219-112">Exclui um Alias(configuração de Recuperação de Desastres)</span><span class="sxs-lookup"><span data-stu-id="78219-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="78219-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78219-113">PARAMETERS</span></span>

### <span data-ttu-id="78219-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78219-114">-AsJob</span></span>
<span data-ttu-id="78219-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="78219-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78219-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78219-116">-DefaultProfile</span></span>
<span data-ttu-id="78219-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78219-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78219-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78219-118">-InputObject</span></span>
<span data-ttu-id="78219-119">Objeto de configuração geodr do barramento de serviço</span><span class="sxs-lookup"><span data-stu-id="78219-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="78219-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="78219-120">-Name</span></span>
<span data-ttu-id="78219-121">Alias (GeoDR) Name</span><span class="sxs-lookup"><span data-stu-id="78219-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="78219-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="78219-122">-Namespace</span></span>
<span data-ttu-id="78219-123">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="78219-123">Namespace Name</span></span>

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

### <span data-ttu-id="78219-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78219-124">-PassThru</span></span>
<span data-ttu-id="78219-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="78219-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="78219-126">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="78219-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="78219-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78219-127">-ResourceGroupName</span></span>
<span data-ttu-id="78219-128">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="78219-128">Resource Group Name</span></span>

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

### <span data-ttu-id="78219-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78219-129">-ResourceId</span></span>
<span data-ttu-id="78219-130">ID do Recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="78219-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="78219-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="78219-131">-Confirm</span></span>
<span data-ttu-id="78219-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78219-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78219-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78219-133">-WhatIf</span></span>
<span data-ttu-id="78219-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="78219-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78219-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="78219-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78219-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78219-136">CommonParameters</span></span>
<span data-ttu-id="78219-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78219-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78219-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78219-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78219-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="78219-139">INPUTS</span></span>

### <span data-ttu-id="78219-140">System.String</span><span class="sxs-lookup"><span data-stu-id="78219-140">System.String</span></span>

### <span data-ttu-id="78219-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="78219-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="78219-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="78219-142">OUTPUTS</span></span>

### <span data-ttu-id="78219-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="78219-143">System.Boolean</span></span>

## <span data-ttu-id="78219-144">Notas</span><span class="sxs-lookup"><span data-stu-id="78219-144">NOTES</span></span>

## <span data-ttu-id="78219-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78219-145">RELATED LINKS</span></span>
