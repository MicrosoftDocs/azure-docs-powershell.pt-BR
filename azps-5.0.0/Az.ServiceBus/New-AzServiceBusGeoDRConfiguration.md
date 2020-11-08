---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 1bb881d96b0247b4cc6d59171c146d75f6df9de0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125557"
---
# <span data-ttu-id="21f38-101">New-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="21f38-101">New-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="21f38-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21f38-102">SYNOPSIS</span></span>
<span data-ttu-id="21f38-103">Cria um novo alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="21f38-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="21f38-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21f38-104">SYNTAX</span></span>

### <span data-ttu-id="21f38-105">GeoDRPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="21f38-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21f38-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="21f38-106">NamespaceInputObjectSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21f38-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21f38-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21f38-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21f38-108">DESCRIPTION</span></span>
<span data-ttu-id="21f38-109">O cmdlet **New-AzServiceBusGeoDRConfiguration** cria um novo alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="21f38-109">The **New-AzServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="21f38-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21f38-110">EXAMPLES</span></span>

### <span data-ttu-id="21f38-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="21f38-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="21f38-112">Cria um alias "SampleDRConfigName" com o namespace principal "SampleNamespace_Primary" com o namespace secundário "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="21f38-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="21f38-113">OS</span><span class="sxs-lookup"><span data-stu-id="21f38-113">PARAMETERS</span></span>

### <span data-ttu-id="21f38-114">-Alternatename</span><span class="sxs-lookup"><span data-stu-id="21f38-114">-AlternateName</span></span>
<span data-ttu-id="21f38-115">Alternatename</span><span class="sxs-lookup"><span data-stu-id="21f38-115">AlternateName</span></span>

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

### <span data-ttu-id="21f38-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21f38-116">-AsJob</span></span>
<span data-ttu-id="21f38-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="21f38-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21f38-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21f38-118">-DefaultProfile</span></span>
<span data-ttu-id="21f38-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="21f38-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21f38-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21f38-120">-InputObject</span></span>
<span data-ttu-id="21f38-121">Objeto namespace</span><span class="sxs-lookup"><span data-stu-id="21f38-121">Namespace Object</span></span>

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

### <span data-ttu-id="21f38-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="21f38-122">-Name</span></span>
<span data-ttu-id="21f38-123">Nome de configuração DR</span><span class="sxs-lookup"><span data-stu-id="21f38-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="21f38-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="21f38-124">-Namespace</span></span>
<span data-ttu-id="21f38-125">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="21f38-125">Namespace Name</span></span>

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

### <span data-ttu-id="21f38-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="21f38-126">-PartnerNamespace</span></span>
<span data-ttu-id="21f38-127">PartnerNamespace de configuração DR (ID ARM de PartnerNamespace [namespace secundário])</span><span class="sxs-lookup"><span data-stu-id="21f38-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

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

### <span data-ttu-id="21f38-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21f38-128">-ResourceGroupName</span></span>
<span data-ttu-id="21f38-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="21f38-129">Resource Group Name</span></span>

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

### <span data-ttu-id="21f38-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21f38-130">-ResourceId</span></span>
<span data-ttu-id="21f38-131">ID do recurso namespace</span><span class="sxs-lookup"><span data-stu-id="21f38-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="21f38-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="21f38-132">-Confirm</span></span>
<span data-ttu-id="21f38-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21f38-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21f38-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21f38-134">-WhatIf</span></span>
<span data-ttu-id="21f38-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="21f38-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21f38-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="21f38-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21f38-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21f38-137">CommonParameters</span></span>
<span data-ttu-id="21f38-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21f38-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21f38-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21f38-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21f38-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21f38-140">INPUTS</span></span>

### <span data-ttu-id="21f38-141">System. String</span><span class="sxs-lookup"><span data-stu-id="21f38-141">System.String</span></span>

### <span data-ttu-id="21f38-142">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="21f38-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="21f38-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21f38-143">OUTPUTS</span></span>

### <span data-ttu-id="21f38-144">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="21f38-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="21f38-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21f38-145">NOTES</span></span>

## <span data-ttu-id="21f38-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21f38-146">RELATED LINKS</span></span>
