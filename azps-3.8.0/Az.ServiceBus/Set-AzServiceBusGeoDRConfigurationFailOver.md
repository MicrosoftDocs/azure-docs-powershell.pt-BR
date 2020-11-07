---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 05a395ce1244130f5f11eb4e0593a1855dc8fb76
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941090"
---
# <span data-ttu-id="b47b1-101">Set-AzServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="b47b1-101">Set-AzServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="b47b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b47b1-102">SYNOPSIS</span></span>
<span data-ttu-id="b47b1-103">Invoca o failover de DR geográfico e reconfigura o alias para apontar para o namespace secundário</span><span class="sxs-lookup"><span data-stu-id="b47b1-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="b47b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b47b1-104">SYNTAX</span></span>

### <span data-ttu-id="b47b1-105">GeoDRPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b47b1-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b47b1-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b47b1-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b47b1-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b47b1-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b47b1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b47b1-108">DESCRIPTION</span></span>
<span data-ttu-id="b47b1-109">O cmdlet **set-AzServiceBusGeoDRConfigurationFailOver** invoca o failover de Dr geográfico e reconfigura o alias para apontar para o namespace secundário</span><span class="sxs-lookup"><span data-stu-id="b47b1-109">The **Set-AzServiceBusGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="b47b1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b47b1-110">EXAMPLES</span></span>

### <span data-ttu-id="b47b1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b47b1-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="b47b1-112">Invoca o failover por alias "SampleDRConfigName", reconfigura e aponta para o namespace secundário "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="b47b1-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="b47b1-113">OS</span><span class="sxs-lookup"><span data-stu-id="b47b1-113">PARAMETERS</span></span>

### <span data-ttu-id="b47b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b47b1-114">-DefaultProfile</span></span>
<span data-ttu-id="b47b1-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b47b1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b47b1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b47b1-116">-InputObject</span></span>
<span data-ttu-id="b47b1-117">Objeto de configuração do barramento do serviço GeoDR</span><span class="sxs-lookup"><span data-stu-id="b47b1-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="b47b1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b47b1-118">-Name</span></span>
<span data-ttu-id="b47b1-119">Nome de configuração DR-alias</span><span class="sxs-lookup"><span data-stu-id="b47b1-119">DR Configuration Name - Alias</span></span>

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

### <span data-ttu-id="b47b1-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b47b1-120">-Namespace</span></span>
<span data-ttu-id="b47b1-121">Nome do namespace-namespace secundário</span><span class="sxs-lookup"><span data-stu-id="b47b1-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="b47b1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b47b1-122">-PassThru</span></span>
<span data-ttu-id="b47b1-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="b47b1-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b47b1-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="b47b1-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b47b1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b47b1-125">-ResourceGroupName</span></span>
<span data-ttu-id="b47b1-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b47b1-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b47b1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b47b1-127">-ResourceId</span></span>
<span data-ttu-id="b47b1-128">ID do recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="b47b1-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="b47b1-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b47b1-129">-Confirm</span></span>
<span data-ttu-id="b47b1-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b47b1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b47b1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b47b1-131">-WhatIf</span></span>
<span data-ttu-id="b47b1-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b47b1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b47b1-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b47b1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b47b1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b47b1-134">CommonParameters</span></span>
<span data-ttu-id="b47b1-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b47b1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b47b1-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b47b1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b47b1-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b47b1-137">INPUTS</span></span>

### <span data-ttu-id="b47b1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b47b1-138">System.String</span></span>

### <span data-ttu-id="b47b1-139">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="b47b1-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="b47b1-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b47b1-140">OUTPUTS</span></span>

### <span data-ttu-id="b47b1-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b47b1-141">System.Boolean</span></span>

## <span data-ttu-id="b47b1-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b47b1-142">NOTES</span></span>

## <span data-ttu-id="b47b1-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b47b1-143">RELATED LINKS</span></span>
