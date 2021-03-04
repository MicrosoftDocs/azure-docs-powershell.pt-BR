---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: 3b308818df135606ac470bcf82d8cd2c0c12b37a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889096"
---
# <span data-ttu-id="0737a-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="0737a-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="0737a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0737a-102">SYNOPSIS</span></span>
<span data-ttu-id="0737a-103">Essa operação desabilita a Recuperação de Desastre e interrompe a re replicação de alterações de namespaces primários para secundários</span><span class="sxs-lookup"><span data-stu-id="0737a-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="0737a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0737a-104">SYNTAX</span></span>

### <span data-ttu-id="0737a-105">GeoDRPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0737a-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0737a-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0737a-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0737a-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0737a-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0737a-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0737a-108">DESCRIPTION</span></span>
<span data-ttu-id="0737a-109">O cmdlet **Set-AzServiceBusGeoDRConfigurationBreakPair** desabilita a Recuperação de Desastres e interrompe a réplica de alterações de namespaces primários para secundários</span><span class="sxs-lookup"><span data-stu-id="0737a-109">The **Set-AzServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="0737a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0737a-110">EXAMPLES</span></span>

### <span data-ttu-id="0737a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0737a-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="0737a-112">Essa operação desabilita a Recuperação de Desastre e interrompe a re replicação de alterações de namespaces primários para secundários</span><span class="sxs-lookup"><span data-stu-id="0737a-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="0737a-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0737a-113">PARAMETERS</span></span>

### <span data-ttu-id="0737a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0737a-114">-DefaultProfile</span></span>
<span data-ttu-id="0737a-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0737a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0737a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0737a-116">-InputObject</span></span>
<span data-ttu-id="0737a-117">Objeto de configuração geográfica do Barramento de Serviço</span><span class="sxs-lookup"><span data-stu-id="0737a-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="0737a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0737a-118">-Name</span></span>
<span data-ttu-id="0737a-119">Nome da configuração dr</span><span class="sxs-lookup"><span data-stu-id="0737a-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="0737a-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0737a-120">-Namespace</span></span>
<span data-ttu-id="0737a-121">Nome do namespace - Namespace principal</span><span class="sxs-lookup"><span data-stu-id="0737a-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="0737a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0737a-122">-PassThru</span></span>
<span data-ttu-id="0737a-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="0737a-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0737a-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="0737a-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0737a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0737a-125">-ResourceGroupName</span></span>
<span data-ttu-id="0737a-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="0737a-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0737a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0737a-127">-ResourceId</span></span>
<span data-ttu-id="0737a-128">ID do Recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="0737a-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="0737a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0737a-129">-Confirm</span></span>
<span data-ttu-id="0737a-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0737a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0737a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0737a-131">-WhatIf</span></span>
<span data-ttu-id="0737a-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0737a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0737a-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0737a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0737a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0737a-134">CommonParameters</span></span>
<span data-ttu-id="0737a-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0737a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0737a-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0737a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0737a-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0737a-137">INPUTS</span></span>

### <span data-ttu-id="0737a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0737a-138">System.String</span></span>

### <span data-ttu-id="0737a-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="0737a-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="0737a-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0737a-140">OUTPUTS</span></span>

### <span data-ttu-id="0737a-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0737a-141">System.Boolean</span></span>

## <span data-ttu-id="0737a-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="0737a-142">NOTES</span></span>

## <span data-ttu-id="0737a-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0737a-143">RELATED LINKS</span></span>
