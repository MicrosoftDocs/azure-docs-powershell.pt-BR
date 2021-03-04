---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 21ccb8a16ff3622e6661bd5548721d6d1227e7e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891284"
---
# <span data-ttu-id="3f258-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f258-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="3f258-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f258-102">SYNOPSIS</span></span>
<span data-ttu-id="3f258-103">Recupera Alias(Configuração de Recuperação de Desastre) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="3f258-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="3f258-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3f258-104">SYNTAX</span></span>

### <span data-ttu-id="3f258-105">GeoDRPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3f258-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f258-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3f258-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f258-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f258-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f258-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3f258-108">DESCRIPTION</span></span>
<span data-ttu-id="3f258-109">**Get-AzServiceBusGeoDRConfiguration** Recupera Alias(Disaster Recovery configuration) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="3f258-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="3f258-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f258-110">EXAMPLES</span></span>

### <span data-ttu-id="3f258-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3f258-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="3f258-112">Recupera a configuração de alias "SampleDRConfigName" para o namespace principal "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="3f258-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="3f258-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3f258-113">PARAMETERS</span></span>

### <span data-ttu-id="3f258-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f258-114">-DefaultProfile</span></span>
<span data-ttu-id="3f258-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f258-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f258-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f258-116">-InputObject</span></span>
<span data-ttu-id="3f258-117">Objeto Namespace</span><span class="sxs-lookup"><span data-stu-id="3f258-117">Namespace Object</span></span>

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

### <span data-ttu-id="3f258-118">-Name</span><span class="sxs-lookup"><span data-stu-id="3f258-118">-Name</span></span>
<span data-ttu-id="3f258-119">Nome da configuração dr</span><span class="sxs-lookup"><span data-stu-id="3f258-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="3f258-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3f258-120">-Namespace</span></span>
<span data-ttu-id="3f258-121">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="3f258-121">Namespace Name</span></span>

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

### <span data-ttu-id="3f258-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f258-122">-ResourceGroupName</span></span>
<span data-ttu-id="3f258-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="3f258-123">Resource Group Name</span></span>

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

### <span data-ttu-id="3f258-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f258-124">-ResourceId</span></span>
<span data-ttu-id="3f258-125">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="3f258-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="3f258-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f258-126">CommonParameters</span></span>
<span data-ttu-id="3f258-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f258-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f258-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f258-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f258-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f258-129">INPUTS</span></span>

### <span data-ttu-id="3f258-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3f258-130">System.String</span></span>

### <span data-ttu-id="3f258-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="3f258-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="3f258-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3f258-132">OUTPUTS</span></span>

### <span data-ttu-id="3f258-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="3f258-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="3f258-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="3f258-134">NOTES</span></span>

## <span data-ttu-id="3f258-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f258-135">RELATED LINKS</span></span>
