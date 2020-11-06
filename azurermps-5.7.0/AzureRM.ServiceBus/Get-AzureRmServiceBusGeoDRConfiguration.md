---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: e5623ed840b9b1d2a7f75150fa686d6f488dc2ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428768"
---
# <span data-ttu-id="e597d-101">Get-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="e597d-101">Get-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="e597d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e597d-102">SYNOPSIS</span></span>
<span data-ttu-id="e597d-103">Recupera o alias (configuração de recuperação de desastres) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="e597d-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e597d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e597d-104">SYNTAX</span></span>

### <span data-ttu-id="e597d-105">GeoDRPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e597d-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e597d-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e597d-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e597d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e597d-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e597d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e597d-108">DESCRIPTION</span></span>
<span data-ttu-id="e597d-109">**Get-AzureRmServiceBusGeoDRConfiguration** recupera o alias (configuração de recuperação de desastres) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="e597d-109">The **Get-AzureRmServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="e597d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e597d-110">EXAMPLES</span></span>

### <span data-ttu-id="e597d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e597d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="e597d-112">Recupera a configuração "SampleDRCongifName" do alias para o namespace primário "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="e597d-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="e597d-113">OS</span><span class="sxs-lookup"><span data-stu-id="e597d-113">PARAMETERS</span></span>

### <span data-ttu-id="e597d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e597d-114">-DefaultProfile</span></span>
<span data-ttu-id="e597d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e597d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e597d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e597d-116">-InputObject</span></span>
<span data-ttu-id="e597d-117">Objeto namespace</span><span class="sxs-lookup"><span data-stu-id="e597d-117">Namespace Object</span></span>

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

### <span data-ttu-id="e597d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e597d-118">-Name</span></span>
<span data-ttu-id="e597d-119">Nome de configuração DR</span><span class="sxs-lookup"><span data-stu-id="e597d-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e597d-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e597d-120">-Namespace</span></span>
<span data-ttu-id="e597d-121">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="e597d-121">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e597d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e597d-122">-ResourceGroupName</span></span>
<span data-ttu-id="e597d-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e597d-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e597d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e597d-124">-ResourceId</span></span>
<span data-ttu-id="e597d-125">ID do recurso namespace</span><span class="sxs-lookup"><span data-stu-id="e597d-125">Namespace Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e597d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e597d-126">CommonParameters</span></span>
<span data-ttu-id="e597d-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e597d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e597d-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e597d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e597d-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e597d-129">INPUTS</span></span>

### <span data-ttu-id="e597d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e597d-130">System.String</span></span>
<span data-ttu-id="e597d-131">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e597d-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="e597d-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e597d-132">OUTPUTS</span></span>

### <span data-ttu-id="e597d-133">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e597d-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="e597d-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e597d-134">NOTES</span></span>

## <span data-ttu-id="e597d-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e597d-135">RELATED LINKS</span></span>
