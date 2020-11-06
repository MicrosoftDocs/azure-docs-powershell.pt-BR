---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: feeb47a1db28debfcfeb4e5d61c22e15db66b799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428212"
---
# <span data-ttu-id="57d78-101">New-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="57d78-101">New-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="57d78-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57d78-102">SYNOPSIS</span></span>
<span data-ttu-id="57d78-103">Cria um novo alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="57d78-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57d78-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57d78-104">SYNTAX</span></span>

### <span data-ttu-id="57d78-105">GeoDRParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="57d78-105">GeoDRParameterSet (Default)</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57d78-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="57d78-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57d78-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57d78-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57d78-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="57d78-108">DESCRIPTION</span></span>
<span data-ttu-id="57d78-109">O cmdlet **New-AzureRmEventHubGeoDRConfiguration** cria um novo alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="57d78-109">The **New-AzureRmEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="57d78-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57d78-110">EXAMPLES</span></span>

### <span data-ttu-id="57d78-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="57d78-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="57d78-112">Cria um alias "SampleDRCongifName" com o namespace principal "SampleNamespace_Primary" com o namespace secundário "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="57d78-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="57d78-113">OS</span><span class="sxs-lookup"><span data-stu-id="57d78-113">PARAMETERS</span></span>

### <span data-ttu-id="57d78-114">-Alternatename</span><span class="sxs-lookup"><span data-stu-id="57d78-114">-AlternateName</span></span>
<span data-ttu-id="57d78-115">Alternatename necessário quando o nome de configuração de DR é igual ao principal namespace</span><span class="sxs-lookup"><span data-stu-id="57d78-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57d78-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57d78-116">-AsJob</span></span>
<span data-ttu-id="57d78-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="57d78-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57d78-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57d78-118">-DefaultProfile</span></span>
<span data-ttu-id="57d78-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57d78-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57d78-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57d78-120">-InputObject</span></span>
<span data-ttu-id="57d78-121">Objeto namespace</span><span class="sxs-lookup"><span data-stu-id="57d78-121">Namespace Object</span></span>

```yaml
Type: PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57d78-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="57d78-122">-Name</span></span>
<span data-ttu-id="57d78-123">Nome de configuração DR</span><span class="sxs-lookup"><span data-stu-id="57d78-123">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57d78-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="57d78-124">-Namespace</span></span>
<span data-ttu-id="57d78-125">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="57d78-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57d78-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="57d78-126">-PartnerNamespace</span></span>
<span data-ttu-id="57d78-127">RECUPERAÇÃO de configuração PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="57d78-127">DR Configuration PartnerNamespace</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57d78-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57d78-128">-ResourceGroupName</span></span>
<span data-ttu-id="57d78-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="57d78-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57d78-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57d78-130">-ResourceId</span></span>
<span data-ttu-id="57d78-131">ID do recurso namespace</span><span class="sxs-lookup"><span data-stu-id="57d78-131">Namespace Resource Id</span></span>

```yaml
Type: String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57d78-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="57d78-132">-Confirm</span></span>
<span data-ttu-id="57d78-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57d78-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57d78-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57d78-134">-WhatIf</span></span>
<span data-ttu-id="57d78-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="57d78-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57d78-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="57d78-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57d78-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57d78-137">CommonParameters</span></span>
<span data-ttu-id="57d78-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57d78-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="57d78-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57d78-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57d78-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="57d78-140">INPUTS</span></span>

### <span data-ttu-id="57d78-141">System. String</span><span class="sxs-lookup"><span data-stu-id="57d78-141">System.String</span></span>
<span data-ttu-id="57d78-142">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="57d78-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="57d78-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="57d78-143">OUTPUTS</span></span>

### <span data-ttu-id="57d78-144">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="57d78-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="57d78-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="57d78-145">NOTES</span></span>

## <span data-ttu-id="57d78-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57d78-146">RELATED LINKS</span></span>
