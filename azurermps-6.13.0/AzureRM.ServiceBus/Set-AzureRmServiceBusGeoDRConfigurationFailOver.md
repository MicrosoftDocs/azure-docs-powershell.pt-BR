---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 274563165beefdc8a5d7575bd32328f68bf40efa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433185"
---
# <span data-ttu-id="a1a87-101">Set-AzureRmServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="a1a87-101">Set-AzureRmServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="a1a87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1a87-102">SYNOPSIS</span></span>
<span data-ttu-id="a1a87-103">Invoca o failover de DR geográfico e reconfigura o alias para apontar para o namespace secundário</span><span class="sxs-lookup"><span data-stu-id="a1a87-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1a87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1a87-104">SYNTAX</span></span>

### <span data-ttu-id="a1a87-105">GeoDRPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a1a87-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1a87-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a1a87-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1a87-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1a87-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1a87-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1a87-108">DESCRIPTION</span></span>
<span data-ttu-id="a1a87-109">O cmdlet **set-AzureRmServiceBusGeoDRConfigurationFailOver** envokes o failover de Dr geográfico e reconfigure o alias para apontar para o namespace secundário</span><span class="sxs-lookup"><span data-stu-id="a1a87-109">The **Set-AzureRmServiceBusGeoDRConfigurationFailOver** cmdlet envokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="a1a87-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1a87-110">EXAMPLES</span></span>

### <span data-ttu-id="a1a87-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a1a87-111">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="a1a87-112">Invoca o failover por alias "SampleDRCongifName", reconfigura e aponta para o namespace secundário "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="a1a87-112">Invokes the Failover over alias "SampleDRCongifName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="a1a87-113">OS</span><span class="sxs-lookup"><span data-stu-id="a1a87-113">PARAMETERS</span></span>

### <span data-ttu-id="a1a87-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1a87-114">-DefaultProfile</span></span>
<span data-ttu-id="a1a87-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1a87-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1a87-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1a87-116">-InputObject</span></span>
<span data-ttu-id="a1a87-117">Objeto de configuração do barramento do serviço GeoDR</span><span class="sxs-lookup"><span data-stu-id="a1a87-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="a1a87-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1a87-118">-Name</span></span>
<span data-ttu-id="a1a87-119">Nome de configuração DR-alias</span><span class="sxs-lookup"><span data-stu-id="a1a87-119">DR Configuration Name - Alias</span></span>

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

### <span data-ttu-id="a1a87-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a1a87-120">-Namespace</span></span>
<span data-ttu-id="a1a87-121">Nome do namespace-namespace secundário</span><span class="sxs-lookup"><span data-stu-id="a1a87-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="a1a87-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1a87-122">-PassThru</span></span>
<span data-ttu-id="a1a87-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="a1a87-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a1a87-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="a1a87-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a1a87-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1a87-125">-ResourceGroupName</span></span>
<span data-ttu-id="a1a87-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a1a87-126">Resource Group Name</span></span>

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

### <span data-ttu-id="a1a87-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1a87-127">-ResourceId</span></span>
<span data-ttu-id="a1a87-128">ID do recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1a87-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="a1a87-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a1a87-129">-Confirm</span></span>
<span data-ttu-id="a1a87-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1a87-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1a87-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1a87-131">-WhatIf</span></span>
<span data-ttu-id="a1a87-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a1a87-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1a87-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1a87-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1a87-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1a87-134">CommonParameters</span></span>
<span data-ttu-id="a1a87-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1a87-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1a87-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1a87-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1a87-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1a87-137">INPUTS</span></span>

### <span data-ttu-id="a1a87-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a1a87-138">System.String</span></span>

### <span data-ttu-id="a1a87-139">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="a1a87-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="a1a87-140">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a1a87-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a1a87-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1a87-141">OUTPUTS</span></span>

### <span data-ttu-id="a1a87-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a1a87-142">System.Boolean</span></span>

## <span data-ttu-id="a1a87-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1a87-143">NOTES</span></span>

## <span data-ttu-id="a1a87-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1a87-144">RELATED LINKS</span></span>
