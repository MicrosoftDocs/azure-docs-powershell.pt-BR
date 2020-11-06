---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: fd87311c59c0889a57cb22eb08aba855e5c3b49c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599210"
---
# <span data-ttu-id="3182f-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="3182f-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="3182f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3182f-102">SYNOPSIS</span></span>
<span data-ttu-id="3182f-103">Recupera o alias (configuração de recuperação de desastres) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="3182f-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="3182f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3182f-104">SYNTAX</span></span>

### <span data-ttu-id="3182f-105">GeoDRPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3182f-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3182f-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3182f-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3182f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3182f-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3182f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3182f-108">DESCRIPTION</span></span>
<span data-ttu-id="3182f-109">**Get-AzServiceBusGeoDRConfiguration** recupera o alias (configuração de recuperação de desastres) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="3182f-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="3182f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3182f-110">EXAMPLES</span></span>

### <span data-ttu-id="3182f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3182f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="3182f-112">Recupera a configuração "SampleDRCongifName" do alias para o namespace primário "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="3182f-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="3182f-113">OS</span><span class="sxs-lookup"><span data-stu-id="3182f-113">PARAMETERS</span></span>

### <span data-ttu-id="3182f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3182f-114">-DefaultProfile</span></span>
<span data-ttu-id="3182f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3182f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3182f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3182f-116">-InputObject</span></span>
<span data-ttu-id="3182f-117">Objeto namespace</span><span class="sxs-lookup"><span data-stu-id="3182f-117">Namespace Object</span></span>

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

### <span data-ttu-id="3182f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="3182f-118">-Name</span></span>
<span data-ttu-id="3182f-119">Nome de configuração DR</span><span class="sxs-lookup"><span data-stu-id="3182f-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="3182f-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3182f-120">-Namespace</span></span>
<span data-ttu-id="3182f-121">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="3182f-121">Namespace Name</span></span>

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

### <span data-ttu-id="3182f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3182f-122">-ResourceGroupName</span></span>
<span data-ttu-id="3182f-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3182f-123">Resource Group Name</span></span>

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

### <span data-ttu-id="3182f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3182f-124">-ResourceId</span></span>
<span data-ttu-id="3182f-125">ID do recurso namespace</span><span class="sxs-lookup"><span data-stu-id="3182f-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="3182f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3182f-126">CommonParameters</span></span>
<span data-ttu-id="3182f-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3182f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3182f-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3182f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3182f-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3182f-129">INPUTS</span></span>

### <span data-ttu-id="3182f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3182f-130">System.String</span></span>

### <span data-ttu-id="3182f-131">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="3182f-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="3182f-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3182f-132">OUTPUTS</span></span>

### <span data-ttu-id="3182f-133">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="3182f-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="3182f-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3182f-134">NOTES</span></span>

## <span data-ttu-id="3182f-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3182f-135">RELATED LINKS</span></span>
