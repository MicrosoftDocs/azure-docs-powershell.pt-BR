---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 5a2f3a3310675324fde3ff262cf88325224193c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943753"
---
# <span data-ttu-id="46f88-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="46f88-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="46f88-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46f88-102">SYNOPSIS</span></span>
<span data-ttu-id="46f88-103">Recupera o alias (configuração de recuperação de desastres) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="46f88-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="46f88-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46f88-104">SYNTAX</span></span>

### <span data-ttu-id="46f88-105">GeoDRPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="46f88-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46f88-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="46f88-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46f88-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="46f88-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46f88-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="46f88-108">DESCRIPTION</span></span>
<span data-ttu-id="46f88-109">**Get-AzServiceBusGeoDRConfiguration** recupera o alias (configuração de recuperação de desastres) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="46f88-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="46f88-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46f88-110">EXAMPLES</span></span>

### <span data-ttu-id="46f88-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="46f88-111">Example 1</span></span>
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

<span data-ttu-id="46f88-112">Recupera a configuração "SampleDRConfigName" do alias para o namespace primário "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="46f88-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="46f88-113">OS</span><span class="sxs-lookup"><span data-stu-id="46f88-113">PARAMETERS</span></span>

### <span data-ttu-id="46f88-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46f88-114">-DefaultProfile</span></span>
<span data-ttu-id="46f88-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46f88-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46f88-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46f88-116">-InputObject</span></span>
<span data-ttu-id="46f88-117">Objeto namespace</span><span class="sxs-lookup"><span data-stu-id="46f88-117">Namespace Object</span></span>

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

### <span data-ttu-id="46f88-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="46f88-118">-Name</span></span>
<span data-ttu-id="46f88-119">Nome de configuração DR</span><span class="sxs-lookup"><span data-stu-id="46f88-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="46f88-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="46f88-120">-Namespace</span></span>
<span data-ttu-id="46f88-121">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="46f88-121">Namespace Name</span></span>

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

### <span data-ttu-id="46f88-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46f88-122">-ResourceGroupName</span></span>
<span data-ttu-id="46f88-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="46f88-123">Resource Group Name</span></span>

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

### <span data-ttu-id="46f88-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46f88-124">-ResourceId</span></span>
<span data-ttu-id="46f88-125">ID do recurso namespace</span><span class="sxs-lookup"><span data-stu-id="46f88-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="46f88-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f88-126">CommonParameters</span></span>
<span data-ttu-id="46f88-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46f88-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f88-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46f88-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f88-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="46f88-129">INPUTS</span></span>

### <span data-ttu-id="46f88-130">System. String</span><span class="sxs-lookup"><span data-stu-id="46f88-130">System.String</span></span>

### <span data-ttu-id="46f88-131">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="46f88-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="46f88-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="46f88-132">OUTPUTS</span></span>

### <span data-ttu-id="46f88-133">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="46f88-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="46f88-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="46f88-134">NOTES</span></span>

## <span data-ttu-id="46f88-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46f88-135">RELATED LINKS</span></span>
