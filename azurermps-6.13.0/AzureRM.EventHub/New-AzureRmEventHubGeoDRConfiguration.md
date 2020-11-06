---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: e2ac72ba5d563b4be902d424ad30c19b40bff9d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427233"
---
# <span data-ttu-id="7a8d9-101">New-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a8d9-101">New-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="7a8d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a8d9-102">SYNOPSIS</span></span>
<span data-ttu-id="7a8d9-103">Cria um novo alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="7a8d9-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a8d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a8d9-104">SYNTAX</span></span>

### <span data-ttu-id="7a8d9-105">GeoDRParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7a8d9-105">GeoDRParameterSet (Default)</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a8d9-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7a8d9-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a8d9-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a8d9-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a8d9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a8d9-108">DESCRIPTION</span></span>
<span data-ttu-id="7a8d9-109">O cmdlet **New-AzureRmEventHubGeoDRConfiguration** cria um novo alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="7a8d9-109">The **New-AzureRmEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="7a8d9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a8d9-110">EXAMPLES</span></span>

### <span data-ttu-id="7a8d9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7a8d9-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="7a8d9-112">Cria um alias "SampleDRCongifName" com o namespace principal "SampleNamespace_Primary" com o namespace secundário "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="7a8d9-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="7a8d9-113">OS</span><span class="sxs-lookup"><span data-stu-id="7a8d9-113">PARAMETERS</span></span>

### <span data-ttu-id="7a8d9-114">-Alternatename</span><span class="sxs-lookup"><span data-stu-id="7a8d9-114">-AlternateName</span></span>
<span data-ttu-id="7a8d9-115">Alternatename necessário quando o nome de configuração de DR é igual ao principal namespace</span><span class="sxs-lookup"><span data-stu-id="7a8d9-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="7a8d9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a8d9-116">-AsJob</span></span>
<span data-ttu-id="7a8d9-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7a8d9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a8d9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a8d9-118">-DefaultProfile</span></span>
<span data-ttu-id="7a8d9-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a8d9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a8d9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a8d9-120">-InputObject</span></span>
<span data-ttu-id="7a8d9-121">Objeto namespace</span><span class="sxs-lookup"><span data-stu-id="7a8d9-121">Namespace Object</span></span>

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

### <span data-ttu-id="7a8d9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a8d9-122">-Name</span></span>
<span data-ttu-id="7a8d9-123">Nome de configuração DR</span><span class="sxs-lookup"><span data-stu-id="7a8d9-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="7a8d9-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7a8d9-124">-Namespace</span></span>
<span data-ttu-id="7a8d9-125">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="7a8d9-125">Namespace Name</span></span>

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

### <span data-ttu-id="7a8d9-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="7a8d9-126">-PartnerNamespace</span></span>
<span data-ttu-id="7a8d9-127">RECUPERAÇÃO de configuração PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="7a8d9-127">DR Configuration PartnerNamespace</span></span>

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

### <span data-ttu-id="7a8d9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a8d9-128">-ResourceGroupName</span></span>
<span data-ttu-id="7a8d9-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7a8d9-129">Resource Group Name</span></span>

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

### <span data-ttu-id="7a8d9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a8d9-130">-ResourceId</span></span>
<span data-ttu-id="7a8d9-131">ID do recurso namespace</span><span class="sxs-lookup"><span data-stu-id="7a8d9-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="7a8d9-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7a8d9-132">-Confirm</span></span>
<span data-ttu-id="7a8d9-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a8d9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a8d9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a8d9-134">-WhatIf</span></span>
<span data-ttu-id="7a8d9-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7a8d9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a8d9-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7a8d9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a8d9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a8d9-137">CommonParameters</span></span>
<span data-ttu-id="7a8d9-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a8d9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a8d9-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a8d9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a8d9-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a8d9-140">INPUTS</span></span>

### <span data-ttu-id="7a8d9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7a8d9-141">System.String</span></span>

### <span data-ttu-id="7a8d9-142">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="7a8d9-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="7a8d9-143">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7a8d9-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="7a8d9-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a8d9-144">OUTPUTS</span></span>

### <span data-ttu-id="7a8d9-145">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="7a8d9-145">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="7a8d9-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a8d9-146">NOTES</span></span>

## <span data-ttu-id="7a8d9-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a8d9-147">RELATED LINKS</span></span>
