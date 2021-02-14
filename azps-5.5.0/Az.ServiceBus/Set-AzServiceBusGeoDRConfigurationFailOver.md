---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 05a395ce1244130f5f11eb4e0593a1855dc8fb76
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117111"
---
# <span data-ttu-id="b4762-101">Set-AzServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="b4762-101">Set-AzServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="b4762-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4762-102">SYNOPSIS</span></span>
<span data-ttu-id="b4762-103">Invoca o failover GEO DR e reconfigura o alias para apontar para o namespace secundário</span><span class="sxs-lookup"><span data-stu-id="b4762-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="b4762-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4762-104">SYNTAX</span></span>

### <span data-ttu-id="b4762-105">GeoDRPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b4762-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4762-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b4762-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4762-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4762-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4762-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4762-108">DESCRIPTION</span></span>
<span data-ttu-id="b4762-109">O cmdlet **Set-AzServiceBusGeoDRConfigurationFailOver** invoca o failover GEO DR e reconfigura o alias para apontar para o namespace secundário</span><span class="sxs-lookup"><span data-stu-id="b4762-109">The **Set-AzServiceBusGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="b4762-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b4762-110">EXAMPLES</span></span>

### <span data-ttu-id="b4762-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b4762-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="b4762-112">Invoca o Failover sobre o alias "SampleDRConfigName", reconfigura e aponta para o namespace secundário "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="b4762-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="b4762-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4762-113">PARAMETERS</span></span>

### <span data-ttu-id="b4762-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4762-114">-DefaultProfile</span></span>
<span data-ttu-id="b4762-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4762-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4762-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4762-116">-InputObject</span></span>
<span data-ttu-id="b4762-117">Objeto de configuração geodr do barramento de serviço</span><span class="sxs-lookup"><span data-stu-id="b4762-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="b4762-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4762-118">-Name</span></span>
<span data-ttu-id="b4762-119">Nome de configuração dr – alias</span><span class="sxs-lookup"><span data-stu-id="b4762-119">DR Configuration Name - Alias</span></span>

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

### <span data-ttu-id="b4762-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b4762-120">-Namespace</span></span>
<span data-ttu-id="b4762-121">Namespace Name - Secondary Namespace</span><span class="sxs-lookup"><span data-stu-id="b4762-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="b4762-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4762-122">-PassThru</span></span>
<span data-ttu-id="b4762-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="b4762-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b4762-124">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="b4762-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b4762-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4762-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4762-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="b4762-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b4762-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4762-127">-ResourceId</span></span>
<span data-ttu-id="b4762-128">ID do Recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4762-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="b4762-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b4762-129">-Confirm</span></span>
<span data-ttu-id="b4762-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4762-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4762-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4762-131">-WhatIf</span></span>
<span data-ttu-id="b4762-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b4762-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4762-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4762-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4762-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4762-134">CommonParameters</span></span>
<span data-ttu-id="b4762-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4762-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4762-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4762-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4762-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="b4762-137">INPUTS</span></span>

### <span data-ttu-id="b4762-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b4762-138">System.String</span></span>

### <span data-ttu-id="b4762-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="b4762-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="b4762-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="b4762-140">OUTPUTS</span></span>

### <span data-ttu-id="b4762-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b4762-141">System.Boolean</span></span>

## <span data-ttu-id="b4762-142">Notas</span><span class="sxs-lookup"><span data-stu-id="b4762-142">NOTES</span></span>

## <span data-ttu-id="b4762-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4762-143">RELATED LINKS</span></span>
