---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 5a2f3a3310675324fde3ff262cf88325224193c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125887"
---
# <span data-ttu-id="425ee-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="425ee-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="425ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="425ee-102">SYNOPSIS</span></span>
<span data-ttu-id="425ee-103">Recupera o alias (configuração de recuperação de desastres) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="425ee-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="425ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="425ee-104">SYNTAX</span></span>

### <span data-ttu-id="425ee-105">GeoDRPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="425ee-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="425ee-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="425ee-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="425ee-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="425ee-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="425ee-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="425ee-108">DESCRIPTION</span></span>
<span data-ttu-id="425ee-109">**Get-AzServiceBusGeoDRConfiguration** recupera o alias (configuração de recuperação de desastres) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="425ee-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="425ee-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="425ee-110">EXAMPLES</span></span>

### <span data-ttu-id="425ee-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="425ee-111">Example 1</span></span>
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

<span data-ttu-id="425ee-112">Recupera a configuração "SampleDRConfigName" do alias para o namespace primário "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="425ee-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="425ee-113">OS</span><span class="sxs-lookup"><span data-stu-id="425ee-113">PARAMETERS</span></span>

### <span data-ttu-id="425ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="425ee-114">-DefaultProfile</span></span>
<span data-ttu-id="425ee-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="425ee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="425ee-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="425ee-116">-InputObject</span></span>
<span data-ttu-id="425ee-117">Objeto namespace</span><span class="sxs-lookup"><span data-stu-id="425ee-117">Namespace Object</span></span>

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

### <span data-ttu-id="425ee-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="425ee-118">-Name</span></span>
<span data-ttu-id="425ee-119">Nome de configuração DR</span><span class="sxs-lookup"><span data-stu-id="425ee-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="425ee-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="425ee-120">-Namespace</span></span>
<span data-ttu-id="425ee-121">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="425ee-121">Namespace Name</span></span>

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

### <span data-ttu-id="425ee-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="425ee-122">-ResourceGroupName</span></span>
<span data-ttu-id="425ee-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="425ee-123">Resource Group Name</span></span>

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

### <span data-ttu-id="425ee-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="425ee-124">-ResourceId</span></span>
<span data-ttu-id="425ee-125">ID do recurso namespace</span><span class="sxs-lookup"><span data-stu-id="425ee-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="425ee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="425ee-126">CommonParameters</span></span>
<span data-ttu-id="425ee-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="425ee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="425ee-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="425ee-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="425ee-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="425ee-129">INPUTS</span></span>

### <span data-ttu-id="425ee-130">System. String</span><span class="sxs-lookup"><span data-stu-id="425ee-130">System.String</span></span>

### <span data-ttu-id="425ee-131">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="425ee-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="425ee-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="425ee-132">OUTPUTS</span></span>

### <span data-ttu-id="425ee-133">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="425ee-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="425ee-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="425ee-134">NOTES</span></span>

## <span data-ttu-id="425ee-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="425ee-135">RELATED LINKS</span></span>
