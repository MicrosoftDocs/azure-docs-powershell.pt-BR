---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 02335868ca9984d4da57be905b9600b81333b484
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885964"
---
# <span data-ttu-id="5b1e1-101">New-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b1e1-101">New-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="5b1e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b1e1-102">SYNOPSIS</span></span>
<span data-ttu-id="5b1e1-103">Cria um novo Alias(Configuração de Recuperação de Desastre)</span><span class="sxs-lookup"><span data-stu-id="5b1e1-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="5b1e1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5b1e1-104">SYNTAX</span></span>

### <span data-ttu-id="5b1e1-105">GeoDRPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5b1e1-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b1e1-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5b1e1-106">NamespaceInputObjectSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b1e1-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b1e1-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b1e1-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5b1e1-108">DESCRIPTION</span></span>
<span data-ttu-id="5b1e1-109">O cmdlet **New-AzServiceBusGeoDRConfiguration** cria um novo Alias(Configuração de Recuperação de Desastre)</span><span class="sxs-lookup"><span data-stu-id="5b1e1-109">The **New-AzServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="5b1e1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5b1e1-110">EXAMPLES</span></span>

### <span data-ttu-id="5b1e1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5b1e1-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="5b1e1-112">Cria um alias "SampleDRConfigName" com namespace principal "SampleNamespace_Primary" com namespace secundário "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="5b1e1-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="5b1e1-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5b1e1-113">PARAMETERS</span></span>

### <span data-ttu-id="5b1e1-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="5b1e1-114">-AlternateName</span></span>
<span data-ttu-id="5b1e1-115">AlternateName</span><span class="sxs-lookup"><span data-stu-id="5b1e1-115">AlternateName</span></span>

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

### <span data-ttu-id="5b1e1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b1e1-116">-AsJob</span></span>
<span data-ttu-id="5b1e1-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5b1e1-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b1e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b1e1-118">-DefaultProfile</span></span>
<span data-ttu-id="5b1e1-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5b1e1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b1e1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b1e1-120">-InputObject</span></span>
<span data-ttu-id="5b1e1-121">Objeto Namespace</span><span class="sxs-lookup"><span data-stu-id="5b1e1-121">Namespace Object</span></span>

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

### <span data-ttu-id="5b1e1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5b1e1-122">-Name</span></span>
<span data-ttu-id="5b1e1-123">Nome da configuração dr</span><span class="sxs-lookup"><span data-stu-id="5b1e1-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="5b1e1-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5b1e1-124">-Namespace</span></span>
<span data-ttu-id="5b1e1-125">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="5b1e1-125">Namespace Name</span></span>

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

### <span data-ttu-id="5b1e1-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="5b1e1-126">-PartnerNamespace</span></span>
<span data-ttu-id="5b1e1-127">Dr Configuration PartnerNamespace (ARM ID do PartnerNamespace [namespace secundário])</span><span class="sxs-lookup"><span data-stu-id="5b1e1-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

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

### <span data-ttu-id="5b1e1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b1e1-128">-ResourceGroupName</span></span>
<span data-ttu-id="5b1e1-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="5b1e1-129">Resource Group Name</span></span>

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

### <span data-ttu-id="5b1e1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b1e1-130">-ResourceId</span></span>
<span data-ttu-id="5b1e1-131">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="5b1e1-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="5b1e1-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b1e1-132">-Confirm</span></span>
<span data-ttu-id="5b1e1-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b1e1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b1e1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b1e1-134">-WhatIf</span></span>
<span data-ttu-id="5b1e1-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5b1e1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b1e1-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5b1e1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b1e1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b1e1-137">CommonParameters</span></span>
<span data-ttu-id="5b1e1-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b1e1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b1e1-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b1e1-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b1e1-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b1e1-140">INPUTS</span></span>

### <span data-ttu-id="5b1e1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="5b1e1-141">System.String</span></span>

### <span data-ttu-id="5b1e1-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="5b1e1-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="5b1e1-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5b1e1-143">OUTPUTS</span></span>

### <span data-ttu-id="5b1e1-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="5b1e1-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="5b1e1-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="5b1e1-145">NOTES</span></span>

## <span data-ttu-id="5b1e1-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b1e1-146">RELATED LINKS</span></span>
