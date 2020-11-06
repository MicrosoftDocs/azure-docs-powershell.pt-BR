---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 1a6fc5bca4c31afe08591190c111649495555cde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431603"
---
# <span data-ttu-id="8ecfa-101">Set-AzureRmServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="8ecfa-101">Set-AzureRmServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="8ecfa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ecfa-102">SYNOPSIS</span></span>
<span data-ttu-id="8ecfa-103">Invoca o failover de DR geográfico e reconfigura o alias para apontar para o namespace secundário</span><span class="sxs-lookup"><span data-stu-id="8ecfa-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ecfa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ecfa-104">SYNTAX</span></span>

### <span data-ttu-id="8ecfa-105">GeoDRBreakPairFailOverPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8ecfa-105">GeoDRBreakPairFailOverPropertiesSet (Default)</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ecfa-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8ecfa-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ecfa-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ecfa-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ecfa-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ecfa-108">DESCRIPTION</span></span>
<span data-ttu-id="8ecfa-109">O cmdlet **set-AzureRmServiceBusGeoDRConfigurationFailOver** envokes o failover de Dr geográfico e reconfigure o alias para apontar para o namespace secundário</span><span class="sxs-lookup"><span data-stu-id="8ecfa-109">The **Set-AzureRmServiceBusGeoDRConfigurationFailOver** cmdlet envokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="8ecfa-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ecfa-110">EXAMPLES</span></span>

### <span data-ttu-id="8ecfa-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8ecfa-111">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="8ecfa-112">Invoca o failover por alias "SampleDRCongifName", reconfigura e aponta para o namespace secundário "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="8ecfa-112">Invokes the Failover over alias "SampleDRCongifName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="8ecfa-113">OS</span><span class="sxs-lookup"><span data-stu-id="8ecfa-113">PARAMETERS</span></span>

### <span data-ttu-id="8ecfa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ecfa-114">-DefaultProfile</span></span>
<span data-ttu-id="8ecfa-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecfa-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ecfa-116">-InputObject</span></span>
<span data-ttu-id="8ecfa-117">Objeto de configuração do barramento do serviço GeoDR</span><span class="sxs-lookup"><span data-stu-id="8ecfa-117">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ecfa-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ecfa-118">-Name</span></span>
<span data-ttu-id="8ecfa-119">Nome de configuração DR-alias</span><span class="sxs-lookup"><span data-stu-id="8ecfa-119">DR Configuration Name - Alias</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ecfa-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8ecfa-120">-Namespace</span></span>
<span data-ttu-id="8ecfa-121">Nome do namespace-namespace secundário</span><span class="sxs-lookup"><span data-stu-id="8ecfa-121">Namespace Name - Secondary Namespace</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ecfa-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ecfa-122">-PassThru</span></span>
<span data-ttu-id="8ecfa-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8ecfa-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecfa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ecfa-125">-ResourceGroupName</span></span>
<span data-ttu-id="8ecfa-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8ecfa-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ecfa-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ecfa-127">-ResourceId</span></span>
<span data-ttu-id="8ecfa-128">ID do recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ecfa-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ecfa-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8ecfa-129">-Confirm</span></span>
<span data-ttu-id="8ecfa-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecfa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ecfa-131">-WhatIf</span></span>
<span data-ttu-id="8ecfa-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ecfa-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecfa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ecfa-134">CommonParameters</span></span>
<span data-ttu-id="8ecfa-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ecfa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8ecfa-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ecfa-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ecfa-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ecfa-137">INPUTS</span></span>

### <span data-ttu-id="8ecfa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8ecfa-138">System.String</span></span>
<span data-ttu-id="8ecfa-139">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="8ecfa-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>


## <span data-ttu-id="8ecfa-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ecfa-140">OUTPUTS</span></span>

### <span data-ttu-id="8ecfa-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8ecfa-141">System.Boolean</span></span>


## <span data-ttu-id="8ecfa-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ecfa-142">NOTES</span></span>

## <span data-ttu-id="8ecfa-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ecfa-143">RELATED LINKS</span></span>
