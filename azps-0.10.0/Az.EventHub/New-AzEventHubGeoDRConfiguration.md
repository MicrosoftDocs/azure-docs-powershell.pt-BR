---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: b2c48ad3bda14775dd0535b63343d90f026bf614
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775881"
---
# <span data-ttu-id="b65a9-101">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="b65a9-101">New-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="b65a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b65a9-102">SYNOPSIS</span></span>
<span data-ttu-id="b65a9-103">Cria um novo alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="b65a9-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="b65a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b65a9-104">SYNTAX</span></span>

### <span data-ttu-id="b65a9-105">GeoDRParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b65a9-105">GeoDRParameterSet (Default)</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b65a9-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b65a9-106">NamespaceInputObjectSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b65a9-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b65a9-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b65a9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b65a9-108">DESCRIPTION</span></span>
<span data-ttu-id="b65a9-109">O cmdlet **New-AzEventHubGeoDRConfiguration** cria um novo alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="b65a9-109">The **New-AzEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="b65a9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b65a9-110">EXAMPLES</span></span>

### <span data-ttu-id="b65a9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b65a9-111">Example 1</span></span>
```
PS C:\> New-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="b65a9-112">Cria um alias "SampleDRConfigName" com o namespace principal "SampleNamespace_Primary" com o namespace secundário "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="b65a9-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="b65a9-113">OS</span><span class="sxs-lookup"><span data-stu-id="b65a9-113">PARAMETERS</span></span>

### <span data-ttu-id="b65a9-114">-Alternatename</span><span class="sxs-lookup"><span data-stu-id="b65a9-114">-AlternateName</span></span>
<span data-ttu-id="b65a9-115">Alternatename necessário quando o nome de configuração de DR é igual ao principal namespace</span><span class="sxs-lookup"><span data-stu-id="b65a9-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="b65a9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b65a9-116">-AsJob</span></span>
<span data-ttu-id="b65a9-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b65a9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b65a9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b65a9-118">-DefaultProfile</span></span>
<span data-ttu-id="b65a9-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b65a9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b65a9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b65a9-120">-InputObject</span></span>
<span data-ttu-id="b65a9-121">Objeto namespace</span><span class="sxs-lookup"><span data-stu-id="b65a9-121">Namespace Object</span></span>

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

### <span data-ttu-id="b65a9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b65a9-122">-Name</span></span>
<span data-ttu-id="b65a9-123">Nome de configuração DR</span><span class="sxs-lookup"><span data-stu-id="b65a9-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="b65a9-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b65a9-124">-Namespace</span></span>
<span data-ttu-id="b65a9-125">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="b65a9-125">Namespace Name</span></span>

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

### <span data-ttu-id="b65a9-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="b65a9-126">-PartnerNamespace</span></span>
<span data-ttu-id="b65a9-127">RECUPERAÇÃO de configuração PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="b65a9-127">DR Configuration PartnerNamespace</span></span>

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

### <span data-ttu-id="b65a9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b65a9-128">-ResourceGroupName</span></span>
<span data-ttu-id="b65a9-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b65a9-129">Resource Group Name</span></span>

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

### <span data-ttu-id="b65a9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b65a9-130">-ResourceId</span></span>
<span data-ttu-id="b65a9-131">ID do recurso namespace</span><span class="sxs-lookup"><span data-stu-id="b65a9-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="b65a9-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b65a9-132">-Confirm</span></span>
<span data-ttu-id="b65a9-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b65a9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b65a9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b65a9-134">-WhatIf</span></span>
<span data-ttu-id="b65a9-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b65a9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b65a9-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b65a9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b65a9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b65a9-137">CommonParameters</span></span>
<span data-ttu-id="b65a9-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b65a9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b65a9-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b65a9-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b65a9-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b65a9-140">INPUTS</span></span>

### <span data-ttu-id="b65a9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b65a9-141">System.String</span></span>

### <span data-ttu-id="b65a9-142">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="b65a9-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="b65a9-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b65a9-143">OUTPUTS</span></span>

### <span data-ttu-id="b65a9-144">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="b65a9-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="b65a9-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b65a9-145">NOTES</span></span>

## <span data-ttu-id="b65a9-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b65a9-146">RELATED LINKS</span></span>