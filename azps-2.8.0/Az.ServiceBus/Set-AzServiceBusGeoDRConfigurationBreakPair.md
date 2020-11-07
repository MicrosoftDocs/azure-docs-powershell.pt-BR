---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: 1284b0d039ff057fa6bd09d0530c7ff9b2515ed2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772450"
---
# <span data-ttu-id="2befb-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="2befb-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="2befb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2befb-102">SYNOPSIS</span></span>
<span data-ttu-id="2befb-103">Esta operação desabilita a recuperação de desastres e interrompe a replicação de alterações de namespaces primário para secundário</span><span class="sxs-lookup"><span data-stu-id="2befb-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="2befb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2befb-104">SYNTAX</span></span>

### <span data-ttu-id="2befb-105">GeoDRPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2befb-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2befb-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2befb-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2befb-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2befb-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2befb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2befb-108">DESCRIPTION</span></span>
<span data-ttu-id="2befb-109">O cmdlet **set-AzServiceBusGeoDRConfigurationBreakPair** desabilita a recuperação de desastres e interrompe a replicação de alterações de namespaces primário para secundário</span><span class="sxs-lookup"><span data-stu-id="2befb-109">The **Set-AzServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="2befb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2befb-110">EXAMPLES</span></span>

### <span data-ttu-id="2befb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2befb-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="2befb-112">Esta operação desabilita a recuperação de desastres e interrompe a replicação de alterações de namespaces primário para secundário</span><span class="sxs-lookup"><span data-stu-id="2befb-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="2befb-113">OS</span><span class="sxs-lookup"><span data-stu-id="2befb-113">PARAMETERS</span></span>

### <span data-ttu-id="2befb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2befb-114">-DefaultProfile</span></span>
<span data-ttu-id="2befb-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2befb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2befb-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2befb-116">-InputObject</span></span>
<span data-ttu-id="2befb-117">Objeto de configuração do barramento do serviço GeoDR</span><span class="sxs-lookup"><span data-stu-id="2befb-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="2befb-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="2befb-118">-Name</span></span>
<span data-ttu-id="2befb-119">Nome de configuração DR</span><span class="sxs-lookup"><span data-stu-id="2befb-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="2befb-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2befb-120">-Namespace</span></span>
<span data-ttu-id="2befb-121">Nome do namespace-namespace primário</span><span class="sxs-lookup"><span data-stu-id="2befb-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="2befb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2befb-122">-PassThru</span></span>
<span data-ttu-id="2befb-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="2befb-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2befb-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="2befb-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2befb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2befb-125">-ResourceGroupName</span></span>
<span data-ttu-id="2befb-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2befb-126">Resource Group Name</span></span>

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

### <span data-ttu-id="2befb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2befb-127">-ResourceId</span></span>
<span data-ttu-id="2befb-128">ID do recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="2befb-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="2befb-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2befb-129">-Confirm</span></span>
<span data-ttu-id="2befb-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2befb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2befb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2befb-131">-WhatIf</span></span>
<span data-ttu-id="2befb-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2befb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2befb-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2befb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2befb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2befb-134">CommonParameters</span></span>
<span data-ttu-id="2befb-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2befb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2befb-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2befb-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2befb-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2befb-137">INPUTS</span></span>

### <span data-ttu-id="2befb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2befb-138">System.String</span></span>

### <span data-ttu-id="2befb-139">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="2befb-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="2befb-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2befb-140">OUTPUTS</span></span>

### <span data-ttu-id="2befb-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2befb-141">System.Boolean</span></span>

## <span data-ttu-id="2befb-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2befb-142">NOTES</span></span>

## <span data-ttu-id="2befb-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2befb-143">RELATED LINKS</span></span>
