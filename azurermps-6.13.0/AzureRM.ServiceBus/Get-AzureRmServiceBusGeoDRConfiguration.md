---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 7d3635b33e96052c42ca77384d2f138af5cc0d5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432733"
---
# <span data-ttu-id="6e701-101">Get-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e701-101">Get-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="6e701-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e701-102">SYNOPSIS</span></span>
<span data-ttu-id="6e701-103">Recupera o alias (configuração de recuperação de desastres) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="6e701-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e701-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e701-104">SYNTAX</span></span>

### <span data-ttu-id="6e701-105">GeoDRPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6e701-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e701-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6e701-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e701-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e701-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e701-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6e701-108">DESCRIPTION</span></span>
<span data-ttu-id="6e701-109">**Get-AzureRmServiceBusGeoDRConfiguration** recupera o alias (configuração de recuperação de desastres) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="6e701-109">The **Get-AzureRmServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="6e701-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e701-110">EXAMPLES</span></span>

### <span data-ttu-id="6e701-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6e701-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="6e701-112">Recupera a configuração "SampleDRCongifName" do alias para o namespace primário "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="6e701-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="6e701-113">OS</span><span class="sxs-lookup"><span data-stu-id="6e701-113">PARAMETERS</span></span>

### <span data-ttu-id="6e701-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e701-114">-DefaultProfile</span></span>
<span data-ttu-id="6e701-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e701-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e701-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e701-116">-InputObject</span></span>
<span data-ttu-id="6e701-117">Objeto namespace</span><span class="sxs-lookup"><span data-stu-id="6e701-117">Namespace Object</span></span>

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

### <span data-ttu-id="6e701-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e701-118">-Name</span></span>
<span data-ttu-id="6e701-119">Nome de configuração DR</span><span class="sxs-lookup"><span data-stu-id="6e701-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="6e701-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6e701-120">-Namespace</span></span>
<span data-ttu-id="6e701-121">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="6e701-121">Namespace Name</span></span>

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

### <span data-ttu-id="6e701-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e701-122">-ResourceGroupName</span></span>
<span data-ttu-id="6e701-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6e701-123">Resource Group Name</span></span>

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

### <span data-ttu-id="6e701-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e701-124">-ResourceId</span></span>
<span data-ttu-id="6e701-125">ID do recurso namespace</span><span class="sxs-lookup"><span data-stu-id="6e701-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="6e701-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e701-126">CommonParameters</span></span>
<span data-ttu-id="6e701-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e701-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e701-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e701-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e701-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6e701-129">INPUTS</span></span>

### <span data-ttu-id="6e701-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6e701-130">System.String</span></span>

### <span data-ttu-id="6e701-131">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="6e701-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="6e701-132">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6e701-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="6e701-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6e701-133">OUTPUTS</span></span>

### <span data-ttu-id="6e701-134">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="6e701-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="6e701-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6e701-135">NOTES</span></span>

## <span data-ttu-id="6e701-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e701-136">RELATED LINKS</span></span>
