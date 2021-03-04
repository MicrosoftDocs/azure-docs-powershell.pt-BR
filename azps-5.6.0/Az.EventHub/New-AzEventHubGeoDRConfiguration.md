---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: d545883f1c4ce51d4e3efce15787a2e0fa144378
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886024"
---
# <span data-ttu-id="14a17-101">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="14a17-101">New-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="14a17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14a17-102">SYNOPSIS</span></span>
<span data-ttu-id="14a17-103">Cria um novo Alias(Configuração de Recuperação de Desastre)</span><span class="sxs-lookup"><span data-stu-id="14a17-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="14a17-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="14a17-104">SYNTAX</span></span>

### <span data-ttu-id="14a17-105">GeoDRParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="14a17-105">GeoDRParameterSet (Default)</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14a17-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="14a17-106">NamespaceInputObjectSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14a17-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14a17-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14a17-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="14a17-108">DESCRIPTION</span></span>
<span data-ttu-id="14a17-109">O cmdlet **New-AzEventHubGeoDRConfiguration** cria um novo Alias(Configuração de Recuperação de Desastre)</span><span class="sxs-lookup"><span data-stu-id="14a17-109">The **New-AzEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="14a17-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14a17-110">EXAMPLES</span></span>

### <span data-ttu-id="14a17-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="14a17-111">Example 1</span></span>
```
PS C:\> New-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="14a17-112">Cria um alias "SampleDRConfigName" com namespace principal "SampleNamespace_Primary" com namespace secundário "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="14a17-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="14a17-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="14a17-113">PARAMETERS</span></span>

### <span data-ttu-id="14a17-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="14a17-114">-AlternateName</span></span>
<span data-ttu-id="14a17-115">AlternateName obrigatório quando o nome da configuração dr é o mesmo que Namespace primário</span><span class="sxs-lookup"><span data-stu-id="14a17-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="14a17-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14a17-116">-AsJob</span></span>
<span data-ttu-id="14a17-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="14a17-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14a17-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14a17-118">-DefaultProfile</span></span>
<span data-ttu-id="14a17-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14a17-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14a17-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14a17-120">-InputObject</span></span>
<span data-ttu-id="14a17-121">Objeto Namespace</span><span class="sxs-lookup"><span data-stu-id="14a17-121">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14a17-122">-Name</span><span class="sxs-lookup"><span data-stu-id="14a17-122">-Name</span></span>
<span data-ttu-id="14a17-123">Nome da configuração dr</span><span class="sxs-lookup"><span data-stu-id="14a17-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="14a17-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="14a17-124">-Namespace</span></span>
<span data-ttu-id="14a17-125">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="14a17-125">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14a17-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="14a17-126">-PartnerNamespace</span></span>
<span data-ttu-id="14a17-127">ID do PartnerNamespace de Configuração ARM DR</span><span class="sxs-lookup"><span data-stu-id="14a17-127">DR Configuration PartnerNamespace ARM ID</span></span>

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

### <span data-ttu-id="14a17-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14a17-128">-ResourceGroupName</span></span>
<span data-ttu-id="14a17-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="14a17-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14a17-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14a17-130">-ResourceId</span></span>
<span data-ttu-id="14a17-131">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="14a17-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="14a17-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14a17-132">-Confirm</span></span>
<span data-ttu-id="14a17-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14a17-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14a17-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14a17-134">-WhatIf</span></span>
<span data-ttu-id="14a17-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14a17-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14a17-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14a17-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14a17-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14a17-137">CommonParameters</span></span>
<span data-ttu-id="14a17-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14a17-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14a17-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14a17-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14a17-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14a17-140">INPUTS</span></span>

### <span data-ttu-id="14a17-141">System.String</span><span class="sxs-lookup"><span data-stu-id="14a17-141">System.String</span></span>

### <span data-ttu-id="14a17-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="14a17-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="14a17-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="14a17-143">OUTPUTS</span></span>

### <span data-ttu-id="14a17-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="14a17-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="14a17-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="14a17-145">NOTES</span></span>

## <span data-ttu-id="14a17-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14a17-146">RELATED LINKS</span></span>
