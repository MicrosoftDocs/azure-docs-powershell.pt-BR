---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 8c48e6dc8fb095258953a57498b76219dec4ef42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439875"
---
# <span data-ttu-id="62b1a-101">Get-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="62b1a-101">Get-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="62b1a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62b1a-102">SYNOPSIS</span></span>
<span data-ttu-id="62b1a-103">Recupera o alias (configuração de recuperação de desastres) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="62b1a-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62b1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62b1a-104">SYNTAX</span></span>

### <span data-ttu-id="62b1a-105">GeoDRParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="62b1a-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62b1a-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="62b1a-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62b1a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62b1a-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62b1a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="62b1a-108">DESCRIPTION</span></span>
<span data-ttu-id="62b1a-109">**Get-AzureRmEventHubGeoDRConfiguration** recupera o alias (configuração de recuperação de desastres) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="62b1a-109">The **Get-AzureRmEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="62b1a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62b1a-110">EXAMPLES</span></span>

### <span data-ttu-id="62b1a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="62b1a-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="62b1a-112">Recupera a configuração "SampleDRCongifName" do alias para o namespace primário "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="62b1a-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="62b1a-113">OS</span><span class="sxs-lookup"><span data-stu-id="62b1a-113">PARAMETERS</span></span>

### <span data-ttu-id="62b1a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b1a-114">-DefaultProfile</span></span>
<span data-ttu-id="62b1a-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="62b1a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62b1a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62b1a-116">-InputObject</span></span>
<span data-ttu-id="62b1a-117">Objeto namespace</span><span class="sxs-lookup"><span data-stu-id="62b1a-117">Namespace Object</span></span>

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

### <span data-ttu-id="62b1a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="62b1a-118">-Name</span></span>
<span data-ttu-id="62b1a-119">Nome de configuração DR</span><span class="sxs-lookup"><span data-stu-id="62b1a-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="62b1a-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="62b1a-120">-Namespace</span></span>
<span data-ttu-id="62b1a-121">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="62b1a-121">Namespace Name</span></span>

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

### <span data-ttu-id="62b1a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62b1a-122">-ResourceGroupName</span></span>
<span data-ttu-id="62b1a-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="62b1a-123">Resource Group Name</span></span>

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

### <span data-ttu-id="62b1a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62b1a-124">-ResourceId</span></span>
<span data-ttu-id="62b1a-125">ID do recurso namespace</span><span class="sxs-lookup"><span data-stu-id="62b1a-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="62b1a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b1a-126">CommonParameters</span></span>
<span data-ttu-id="62b1a-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62b1a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b1a-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62b1a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b1a-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="62b1a-129">INPUTS</span></span>

### <span data-ttu-id="62b1a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="62b1a-130">System.String</span></span>
<span data-ttu-id="62b1a-131">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="62b1a-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="62b1a-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="62b1a-132">OUTPUTS</span></span>

### <span data-ttu-id="62b1a-133">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="62b1a-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="62b1a-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="62b1a-134">NOTES</span></span>

## <span data-ttu-id="62b1a-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62b1a-135">RELATED LINKS</span></span>
