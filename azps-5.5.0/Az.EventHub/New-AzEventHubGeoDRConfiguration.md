---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 83d1e9edde6e2e792a24e0dc943cf62068938c2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115799"
---
# <span data-ttu-id="3f016-101">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f016-101">New-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="3f016-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f016-102">SYNOPSIS</span></span>
<span data-ttu-id="3f016-103">Cria um novo Alias(configuração de Recuperação de Desastres)</span><span class="sxs-lookup"><span data-stu-id="3f016-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="3f016-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f016-104">SYNTAX</span></span>

### <span data-ttu-id="3f016-105">GeoDRParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3f016-105">GeoDRParameterSet (Default)</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f016-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3f016-106">NamespaceInputObjectSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f016-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f016-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f016-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3f016-108">DESCRIPTION</span></span>
<span data-ttu-id="3f016-109">O **cmdlet New-AzEventHubGeoDRConfiguration** cria um novo Alias(configuração de Recuperação de Desastres)</span><span class="sxs-lookup"><span data-stu-id="3f016-109">The **New-AzEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="3f016-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3f016-110">EXAMPLES</span></span>

### <span data-ttu-id="3f016-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3f016-111">Example 1</span></span>
```
PS C:\> New-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="3f016-112">Cria um alias "SampleDRConfigName" com namespace principal "SampleNamespace_Primary" com namespace secundário "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="3f016-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="3f016-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f016-113">PARAMETERS</span></span>

### <span data-ttu-id="3f016-114">-Nome Alternativo</span><span class="sxs-lookup"><span data-stu-id="3f016-114">-AlternateName</span></span>
<span data-ttu-id="3f016-115">Nome Alternativo necessário quando o nome da configuração DR é igual ao Namespace Principal</span><span class="sxs-lookup"><span data-stu-id="3f016-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="3f016-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f016-116">-AsJob</span></span>
<span data-ttu-id="3f016-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3f016-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f016-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f016-118">-DefaultProfile</span></span>
<span data-ttu-id="3f016-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f016-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f016-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f016-120">-InputObject</span></span>
<span data-ttu-id="3f016-121">Objeto Namespace</span><span class="sxs-lookup"><span data-stu-id="3f016-121">Namespace Object</span></span>

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

### <span data-ttu-id="3f016-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f016-122">-Name</span></span>
<span data-ttu-id="3f016-123">Nome da configuração dr</span><span class="sxs-lookup"><span data-stu-id="3f016-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="3f016-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3f016-124">-Namespace</span></span>
<span data-ttu-id="3f016-125">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="3f016-125">Namespace Name</span></span>

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

### <span data-ttu-id="3f016-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="3f016-126">-PartnerNamespace</span></span>
<span data-ttu-id="3f016-127">ID do ARM do PartnerNamespace de Configuração DR</span><span class="sxs-lookup"><span data-stu-id="3f016-127">DR Configuration PartnerNamespace ARM ID</span></span>

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

### <span data-ttu-id="3f016-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f016-128">-ResourceGroupName</span></span>
<span data-ttu-id="3f016-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="3f016-129">Resource Group Name</span></span>

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

### <span data-ttu-id="3f016-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f016-130">-ResourceId</span></span>
<span data-ttu-id="3f016-131">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="3f016-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="3f016-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3f016-132">-Confirm</span></span>
<span data-ttu-id="3f016-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f016-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f016-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f016-134">-WhatIf</span></span>
<span data-ttu-id="3f016-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3f016-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f016-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3f016-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f016-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f016-137">CommonParameters</span></span>
<span data-ttu-id="3f016-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f016-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f016-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f016-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f016-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="3f016-140">INPUTS</span></span>

### <span data-ttu-id="3f016-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3f016-141">System.String</span></span>

### <span data-ttu-id="3f016-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="3f016-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="3f016-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="3f016-143">OUTPUTS</span></span>

### <span data-ttu-id="3f016-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="3f016-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="3f016-145">Notas</span><span class="sxs-lookup"><span data-stu-id="3f016-145">NOTES</span></span>

## <span data-ttu-id="3f016-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f016-146">RELATED LINKS</span></span>
