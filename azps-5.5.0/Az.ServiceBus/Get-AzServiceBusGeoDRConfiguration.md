---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 5a2f3a3310675324fde3ff262cf88325224193c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118679"
---
# <span data-ttu-id="2928c-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="2928c-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="2928c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2928c-102">SYNOPSIS</span></span>
<span data-ttu-id="2928c-103">Recupera Alias(Configuração de Recuperação de Desastres) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="2928c-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="2928c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2928c-104">SYNTAX</span></span>

### <span data-ttu-id="2928c-105">GeoDRPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2928c-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2928c-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2928c-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2928c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2928c-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2928c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2928c-108">DESCRIPTION</span></span>
<span data-ttu-id="2928c-109">O **Get-AzServiceBusGeoDRConfiguration** recupera alias(configuração de Recuperação de Desastres) para namespace primário ou secundário</span><span class="sxs-lookup"><span data-stu-id="2928c-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="2928c-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2928c-110">EXAMPLES</span></span>

### <span data-ttu-id="2928c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2928c-111">Example 1</span></span>
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

<span data-ttu-id="2928c-112">Recupera a configuração de alias "SampleDRConfigName" para o namespace principal "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="2928c-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="2928c-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2928c-113">PARAMETERS</span></span>

### <span data-ttu-id="2928c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2928c-114">-DefaultProfile</span></span>
<span data-ttu-id="2928c-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2928c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2928c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2928c-116">-InputObject</span></span>
<span data-ttu-id="2928c-117">Objeto Namespace</span><span class="sxs-lookup"><span data-stu-id="2928c-117">Namespace Object</span></span>

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

### <span data-ttu-id="2928c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="2928c-118">-Name</span></span>
<span data-ttu-id="2928c-119">Nome da configuração dr</span><span class="sxs-lookup"><span data-stu-id="2928c-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="2928c-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2928c-120">-Namespace</span></span>
<span data-ttu-id="2928c-121">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="2928c-121">Namespace Name</span></span>

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

### <span data-ttu-id="2928c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2928c-122">-ResourceGroupName</span></span>
<span data-ttu-id="2928c-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="2928c-123">Resource Group Name</span></span>

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

### <span data-ttu-id="2928c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2928c-124">-ResourceId</span></span>
<span data-ttu-id="2928c-125">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="2928c-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="2928c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2928c-126">CommonParameters</span></span>
<span data-ttu-id="2928c-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2928c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2928c-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2928c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2928c-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="2928c-129">INPUTS</span></span>

### <span data-ttu-id="2928c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2928c-130">System.String</span></span>

### <span data-ttu-id="2928c-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="2928c-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="2928c-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="2928c-132">OUTPUTS</span></span>

### <span data-ttu-id="2928c-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="2928c-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="2928c-134">Notas</span><span class="sxs-lookup"><span data-stu-id="2928c-134">NOTES</span></span>

## <span data-ttu-id="2928c-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2928c-135">RELATED LINKS</span></span>
