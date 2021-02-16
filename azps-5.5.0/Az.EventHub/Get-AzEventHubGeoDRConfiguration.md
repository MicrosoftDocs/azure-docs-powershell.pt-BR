---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 2e324524319a2eacd24bc08aa727892ef08928c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113201"
---
# <span data-ttu-id="b1d91-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1d91-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="b1d91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1d91-102">SYNOPSIS</span></span>
<span data-ttu-id="b1d91-103">Recupera Alias(Configuração de Recuperação de Desastres) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="b1d91-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="b1d91-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1d91-104">SYNTAX</span></span>

### <span data-ttu-id="b1d91-105">GeoDRParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b1d91-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1d91-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b1d91-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1d91-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1d91-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1d91-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1d91-108">DESCRIPTION</span></span>
<span data-ttu-id="b1d91-109">O **Get-AzEventHubGeoDRConfiguration** recupera alias(configuração de Recuperação de Desastres) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="b1d91-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="b1d91-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b1d91-110">EXAMPLES</span></span>

### <span data-ttu-id="b1d91-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b1d91-111">Example 1</span></span>
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

<span data-ttu-id="b1d91-112">Recupera a configuração de alias "SampleDRConfigName" para o namespace principal "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="b1d91-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="b1d91-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1d91-113">PARAMETERS</span></span>

### <span data-ttu-id="b1d91-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1d91-114">-DefaultProfile</span></span>
<span data-ttu-id="b1d91-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b1d91-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1d91-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1d91-116">-InputObject</span></span>
<span data-ttu-id="b1d91-117">Objeto Namespace</span><span class="sxs-lookup"><span data-stu-id="b1d91-117">Namespace Object</span></span>

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

### <span data-ttu-id="b1d91-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1d91-118">-Name</span></span>
<span data-ttu-id="b1d91-119">Nome da configuração dr</span><span class="sxs-lookup"><span data-stu-id="b1d91-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="b1d91-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b1d91-120">-Namespace</span></span>
<span data-ttu-id="b1d91-121">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="b1d91-121">Namespace Name</span></span>

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

### <span data-ttu-id="b1d91-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1d91-122">-ResourceGroupName</span></span>
<span data-ttu-id="b1d91-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="b1d91-123">Resource Group Name</span></span>

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

### <span data-ttu-id="b1d91-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1d91-124">-ResourceId</span></span>
<span data-ttu-id="b1d91-125">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="b1d91-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="b1d91-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1d91-126">CommonParameters</span></span>
<span data-ttu-id="b1d91-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1d91-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1d91-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1d91-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1d91-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="b1d91-129">INPUTS</span></span>

### <span data-ttu-id="b1d91-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b1d91-130">System.String</span></span>

### <span data-ttu-id="b1d91-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="b1d91-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="b1d91-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="b1d91-132">OUTPUTS</span></span>

### <span data-ttu-id="b1d91-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="b1d91-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="b1d91-134">Notas</span><span class="sxs-lookup"><span data-stu-id="b1d91-134">NOTES</span></span>

## <span data-ttu-id="b1d91-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1d91-135">RELATED LINKS</span></span>
