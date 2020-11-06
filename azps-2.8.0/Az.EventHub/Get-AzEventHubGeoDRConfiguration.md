---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 4c9d4d1a4ec79da0677bc44d53a3843aa9a6d102
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596494"
---
# <span data-ttu-id="9d7ab-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d7ab-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="9d7ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d7ab-102">SYNOPSIS</span></span>
<span data-ttu-id="9d7ab-103">Recupera o alias (configuração de recuperação de desastres) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="9d7ab-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="9d7ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d7ab-104">SYNTAX</span></span>

### <span data-ttu-id="9d7ab-105">GeoDRParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9d7ab-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d7ab-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9d7ab-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d7ab-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d7ab-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d7ab-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d7ab-108">DESCRIPTION</span></span>
<span data-ttu-id="9d7ab-109">**Get-AzEventHubGeoDRConfiguration** recupera o alias (configuração de recuperação de desastres) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="9d7ab-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="9d7ab-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d7ab-110">EXAMPLES</span></span>

### <span data-ttu-id="9d7ab-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9d7ab-111">Example 1</span></span>
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

<span data-ttu-id="9d7ab-112">Recupera a configuração "SampleDRConfigName" do alias para o namespace primário "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="9d7ab-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="9d7ab-113">OS</span><span class="sxs-lookup"><span data-stu-id="9d7ab-113">PARAMETERS</span></span>

### <span data-ttu-id="9d7ab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d7ab-114">-DefaultProfile</span></span>
<span data-ttu-id="9d7ab-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9d7ab-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d7ab-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d7ab-116">-InputObject</span></span>
<span data-ttu-id="9d7ab-117">Objeto namespace</span><span class="sxs-lookup"><span data-stu-id="9d7ab-117">Namespace Object</span></span>

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

### <span data-ttu-id="9d7ab-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d7ab-118">-Name</span></span>
<span data-ttu-id="9d7ab-119">Nome de configuração DR</span><span class="sxs-lookup"><span data-stu-id="9d7ab-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="9d7ab-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9d7ab-120">-Namespace</span></span>
<span data-ttu-id="9d7ab-121">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="9d7ab-121">Namespace Name</span></span>

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

### <span data-ttu-id="9d7ab-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d7ab-122">-ResourceGroupName</span></span>
<span data-ttu-id="9d7ab-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9d7ab-123">Resource Group Name</span></span>

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

### <span data-ttu-id="9d7ab-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d7ab-124">-ResourceId</span></span>
<span data-ttu-id="9d7ab-125">ID do recurso namespace</span><span class="sxs-lookup"><span data-stu-id="9d7ab-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="9d7ab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d7ab-126">CommonParameters</span></span>
<span data-ttu-id="9d7ab-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d7ab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d7ab-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d7ab-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d7ab-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d7ab-129">INPUTS</span></span>

### <span data-ttu-id="9d7ab-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9d7ab-130">System.String</span></span>

### <span data-ttu-id="9d7ab-131">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="9d7ab-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="9d7ab-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d7ab-132">OUTPUTS</span></span>

### <span data-ttu-id="9d7ab-133">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="9d7ab-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="9d7ab-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d7ab-134">NOTES</span></span>

## <span data-ttu-id="9d7ab-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d7ab-135">RELATED LINKS</span></span>
