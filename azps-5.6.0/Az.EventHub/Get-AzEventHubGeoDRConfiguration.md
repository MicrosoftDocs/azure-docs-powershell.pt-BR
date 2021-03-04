---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: b2003821178875777240cb43bcdc1e9e53784fc4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886042"
---
# <span data-ttu-id="e3f58-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3f58-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="e3f58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3f58-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f58-103">Recupera Alias(Configuração de Recuperação de Desastre) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="e3f58-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="e3f58-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e3f58-104">SYNTAX</span></span>

### <span data-ttu-id="e3f58-105">GeoDRParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e3f58-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3f58-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e3f58-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3f58-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3f58-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3f58-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e3f58-108">DESCRIPTION</span></span>
<span data-ttu-id="e3f58-109">O **Get-AzEventHubGeoDRConfiguration** recupera Alias(Disaster Recovery configuration) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="e3f58-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="e3f58-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3f58-110">EXAMPLES</span></span>

### <span data-ttu-id="e3f58-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e3f58-111">Example 1</span></span>
```
PS C:\> Get-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
AlternateName     :
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="e3f58-112">Recupera a configuração de alias "SampleDRConfigName" para o namespace principal "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="e3f58-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="e3f58-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e3f58-113">PARAMETERS</span></span>

### <span data-ttu-id="e3f58-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3f58-114">-DefaultProfile</span></span>
<span data-ttu-id="e3f58-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3f58-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3f58-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3f58-116">-InputObject</span></span>
<span data-ttu-id="e3f58-117">Objeto Namespace</span><span class="sxs-lookup"><span data-stu-id="e3f58-117">Namespace Object</span></span>

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

### <span data-ttu-id="e3f58-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e3f58-118">-Name</span></span>
<span data-ttu-id="e3f58-119">Nome da configuração dr</span><span class="sxs-lookup"><span data-stu-id="e3f58-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="e3f58-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e3f58-120">-Namespace</span></span>
<span data-ttu-id="e3f58-121">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="e3f58-121">Namespace Name</span></span>

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

### <span data-ttu-id="e3f58-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3f58-122">-ResourceGroupName</span></span>
<span data-ttu-id="e3f58-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="e3f58-123">Resource Group Name</span></span>

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

### <span data-ttu-id="e3f58-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3f58-124">-ResourceId</span></span>
<span data-ttu-id="e3f58-125">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="e3f58-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f58-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f58-126">CommonParameters</span></span>
<span data-ttu-id="e3f58-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3f58-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f58-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3f58-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f58-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3f58-129">INPUTS</span></span>

### <span data-ttu-id="e3f58-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e3f58-130">System.String</span></span>

### <span data-ttu-id="e3f58-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e3f58-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="e3f58-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e3f58-132">OUTPUTS</span></span>

### <span data-ttu-id="e3f58-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="e3f58-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="e3f58-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="e3f58-134">NOTES</span></span>

## <span data-ttu-id="e3f58-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3f58-135">RELATED LINKS</span></span>
