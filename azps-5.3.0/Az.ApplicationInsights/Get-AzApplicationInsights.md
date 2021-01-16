---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
ms.openlocfilehash: 943089433ca7007ef81648846a48ebdd5684bab2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432637"
---
# <span data-ttu-id="e0f58-101">Get-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="e0f58-101">Get-AzApplicationInsights</span></span>

## <span data-ttu-id="e0f58-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0f58-102">SYNOPSIS</span></span>
<span data-ttu-id="e0f58-103">Obter recursos do Application insights</span><span class="sxs-lookup"><span data-stu-id="e0f58-103">Get application insights resources</span></span>

## <span data-ttu-id="e0f58-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0f58-104">SYNTAX</span></span>

### <span data-ttu-id="e0f58-105">ResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e0f58-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzApplicationInsights [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0f58-106">ComponentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0f58-106">ComponentNameParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Full]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0f58-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0f58-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceId] <String> [-Full] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0f58-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0f58-108">DESCRIPTION</span></span>
<span data-ttu-id="e0f58-109">Obter recursos do Application insights em um grupo de recursos ou em um recurso específico</span><span class="sxs-lookup"><span data-stu-id="e0f58-109">Get application insights resources in a resource group or specific resource</span></span>

## <span data-ttu-id="e0f58-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0f58-110">EXAMPLES</span></span>

### <span data-ttu-id="e0f58-111">Exemplo 1 obter recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="e0f58-111">Example 1 Get application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test"

Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test
ResourceGroupName  : testgroup
Name               : test
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 7c8f0641-d307-41bc-b8f2-d30701adb4b3
ApplicationType    : web
Tags               : {}
CreationDate       : 7/5/2017 4:37:22 PM
FlowType           : Redfield
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 1e30d092-4b4b-47c6-ad39-7c10785d80f5
ProvisioningState  : Succeeded
RequestSource      : IbizaAIExtension
SamplingPercentage :
TenantId           : b90b0dec-9b9a-4778-a84e-4ffb73bb17f7
```

<span data-ttu-id="e0f58-112">Obter o recurso insights do aplicativo chamado "Test" no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="e0f58-112">Get application insights resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="e0f58-113">Exemplo 2 obter recurso do Application insights com informações de plano de preço</span><span class="sxs-lookup"><span data-stu-id="e0f58-113">Example 2 Get application insights resource with pricing plan information</span></span>
```
PS C:\> Get-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -IncludePricingPlan

Cap                            : 330
ResetTime                      : 0
StopSendNotificationWhenHitCap : True
CapExpirationTime              :
IsCapped                       : False
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test
ResourceGroupName  : testgroup
Name               : test
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 7c8f0641-d307-41bc-b8f2-d30701adb4b3
ApplicationType    : web
Tags               : {}
CreationDate       : 7/5/2017 4:37:22 PM
FlowType           : Redfield
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 1e30d092-4b4b-47c6-ad39-7c10785d80f5
ProvisioningState  : Succeeded
RequestSource      : IbizaAIExtension
SamplingPercentage :
TenantId           : b90b0dec-9b9a-4778-a84e-4ffb73bb17f7
PricingPlan        : Basic
```

<span data-ttu-id="e0f58-114">Obter um recurso do Application insights e incluir informações de plano de precificação do recurso chamado "teste" no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="e0f58-114">Get application insights resource and include pricing plan information for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="e0f58-115">OS</span><span class="sxs-lookup"><span data-stu-id="e0f58-115">PARAMETERS</span></span>

### <span data-ttu-id="e0f58-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0f58-116">-DefaultProfile</span></span>
<span data-ttu-id="e0f58-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0f58-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0f58-118">-Completo</span><span class="sxs-lookup"><span data-stu-id="e0f58-118">-Full</span></span>
<span data-ttu-id="e0f58-119">Se especificado, ele receberá o plano de preço/Cap diário e status do componente Application insights.</span><span class="sxs-lookup"><span data-stu-id="e0f58-119">If specified, it will get back pricing plan/daily cap and status of the application insights component.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ComponentNameParameterSet, ResourceIdParameterSet
Aliases: IncludeDailyCap, IncludeDailyCapStatus, IncludePricingPlan

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0f58-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0f58-120">-Name</span></span>
<span data-ttu-id="e0f58-121">Nome do recurso do Application insights.</span><span class="sxs-lookup"><span data-stu-id="e0f58-121">Application Insights Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0f58-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0f58-122">-ResourceGroupName</span></span>
<span data-ttu-id="e0f58-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0f58-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0f58-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0f58-124">-ResourceId</span></span>
<span data-ttu-id="e0f58-125">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="e0f58-125">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="e0f58-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0f58-126">CommonParameters</span></span>
<span data-ttu-id="e0f58-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0f58-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0f58-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0f58-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0f58-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0f58-129">INPUTS</span></span>

### <span data-ttu-id="e0f58-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e0f58-130">System.String</span></span>

## <span data-ttu-id="e0f58-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0f58-131">OUTPUTS</span></span>

### <span data-ttu-id="e0f58-132">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="e0f58-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="e0f58-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0f58-133">NOTES</span></span>

## <span data-ttu-id="e0f58-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0f58-134">RELATED LINKS</span></span>
