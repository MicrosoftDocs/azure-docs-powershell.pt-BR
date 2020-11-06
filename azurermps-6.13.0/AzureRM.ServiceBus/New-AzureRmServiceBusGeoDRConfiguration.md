---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: e2f1edfa0d1b5fa081754457fa3fc53f310eb345
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602894"
---
# <span data-ttu-id="b6199-101">New-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6199-101">New-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="b6199-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6199-102">SYNOPSIS</span></span>
<span data-ttu-id="b6199-103">Cria um novo alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="b6199-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6199-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6199-104">SYNTAX</span></span>

### <span data-ttu-id="b6199-105">GeoDRPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b6199-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6199-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b6199-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6199-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6199-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6199-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b6199-108">DESCRIPTION</span></span>
<span data-ttu-id="b6199-109">O cmdlet **New-AzureRmServiceBusGeoDRConfiguration** cria um novo alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="b6199-109">The **New-AzureRmServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="b6199-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6199-110">EXAMPLES</span></span>

### <span data-ttu-id="b6199-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b6199-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="b6199-112">Cria um alias "SampleDRCongifName" com o namespace principal "SampleNamespace_Primary" com o namespace secundário "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="b6199-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="b6199-113">OS</span><span class="sxs-lookup"><span data-stu-id="b6199-113">PARAMETERS</span></span>

### <span data-ttu-id="b6199-114">-Alternatename</span><span class="sxs-lookup"><span data-stu-id="b6199-114">-AlternateName</span></span>
<span data-ttu-id="b6199-115">Alternatename</span><span class="sxs-lookup"><span data-stu-id="b6199-115">AlternateName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6199-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6199-116">-AsJob</span></span>
<span data-ttu-id="b6199-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b6199-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6199-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6199-118">-DefaultProfile</span></span>
<span data-ttu-id="b6199-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b6199-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6199-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6199-120">-InputObject</span></span>
<span data-ttu-id="b6199-121">Objeto namespace</span><span class="sxs-lookup"><span data-stu-id="b6199-121">Namespace Object</span></span>

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

### <span data-ttu-id="b6199-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6199-122">-Name</span></span>
<span data-ttu-id="b6199-123">Nome de configuração DR</span><span class="sxs-lookup"><span data-stu-id="b6199-123">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6199-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b6199-124">-Namespace</span></span>
<span data-ttu-id="b6199-125">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="b6199-125">Namespace Name</span></span>

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

### <span data-ttu-id="b6199-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="b6199-126">-PartnerNamespace</span></span>
<span data-ttu-id="b6199-127">PartnerNamespace de configuração DR (ID ARM de PartnerNamespace [namespace secundário])</span><span class="sxs-lookup"><span data-stu-id="b6199-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6199-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6199-128">-ResourceGroupName</span></span>
<span data-ttu-id="b6199-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b6199-129">Resource Group Name</span></span>

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

### <span data-ttu-id="b6199-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6199-130">-ResourceId</span></span>
<span data-ttu-id="b6199-131">ID do recurso namespace</span><span class="sxs-lookup"><span data-stu-id="b6199-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="b6199-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b6199-132">-Confirm</span></span>
<span data-ttu-id="b6199-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6199-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6199-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6199-134">-WhatIf</span></span>
<span data-ttu-id="b6199-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b6199-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6199-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b6199-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6199-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6199-137">CommonParameters</span></span>
<span data-ttu-id="b6199-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6199-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6199-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6199-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6199-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b6199-140">INPUTS</span></span>

### <span data-ttu-id="b6199-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b6199-141">System.String</span></span>

### <span data-ttu-id="b6199-142">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="b6199-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="b6199-143">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b6199-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b6199-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b6199-144">OUTPUTS</span></span>

### <span data-ttu-id="b6199-145">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="b6199-145">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="b6199-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b6199-146">NOTES</span></span>

## <span data-ttu-id="b6199-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6199-147">RELATED LINKS</span></span>
