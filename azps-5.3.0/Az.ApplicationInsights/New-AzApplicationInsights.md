---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: 3faa93ced76fee1a1023011e1570c3819f6c2013
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272060"
---
# <span data-ttu-id="5136d-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="5136d-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="5136d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5136d-102">SYNOPSIS</span></span>
<span data-ttu-id="5136d-103">Criar um novo recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="5136d-103">Create a new application insights resource</span></span>

## <span data-ttu-id="5136d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5136d-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5136d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5136d-105">DESCRIPTION</span></span>
<span data-ttu-id="5136d-106">Criar um novo recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="5136d-106">Create a new application insights resource</span></span>

## <span data-ttu-id="5136d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5136d-107">EXAMPLES</span></span>

### <span data-ttu-id="5136d-108">Exemplo 1 criar um novo recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="5136d-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test1027
ResourceGroupName  : testgroup
Name               : test1027
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 8323fb13-32aa-46af-b467-8355cf4f8f98
ApplicationType    : web
Tags               : {}
CreationDate       : 10/27/2017 4:56:40 PM
FlowType           :
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 083112ed-ed9b-464e-a9b0-8cf126fbfced
ProvisioningState  : Succeeded
RequestSource      : AzurePowerShell
SamplingPercentage :
TenantId           : {subid}
PublicNetworkAccessForIngestion : Enabled
PublicNetworkAccessForQuery     : Enabled
PrivateLinkScopedResources      :
```

<span data-ttu-id="5136d-109">Adicionar um novo recurso do Application insights chamado "Test" no grupo de recursos "grupo de teste" com o tipo "Java"</span><span class="sxs-lookup"><span data-stu-id="5136d-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java"</span></span>

## <span data-ttu-id="5136d-110">OS</span><span class="sxs-lookup"><span data-stu-id="5136d-110">PARAMETERS</span></span>

### <span data-ttu-id="5136d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5136d-111">-DefaultProfile</span></span>
<span data-ttu-id="5136d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5136d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5136d-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="5136d-113">-Kind</span></span>
<span data-ttu-id="5136d-114">Tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5136d-114">Application kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationKind
Accepted values: web, other, Node.js, java

Required: False
Position: Named
Default value: web
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5136d-115">-Local</span><span class="sxs-lookup"><span data-stu-id="5136d-115">-Location</span></span>
<span data-ttu-id="5136d-116">Localização de recursos do Application insights.</span><span class="sxs-lookup"><span data-stu-id="5136d-116">Application Insights Resource Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5136d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5136d-117">-Name</span></span>
<span data-ttu-id="5136d-118">Nome do recurso do Application insights.</span><span class="sxs-lookup"><span data-stu-id="5136d-118">Application Insights Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5136d-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="5136d-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="5136d-120">O tipo de acesso à rede para acessar a inclusão de insights do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5136d-120">The network access type for accessing Application Insights ingestion.</span></span> <span data-ttu-id="5136d-121">O valor deve ser ' Enabled ' ou ' disabled '</span><span class="sxs-lookup"><span data-stu-id="5136d-121">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5136d-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="5136d-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="5136d-123">O tipo de acesso à rede para acessar a consulta do Application insights.</span><span class="sxs-lookup"><span data-stu-id="5136d-123">The network access type for accessing Application Insights query.</span></span> <span data-ttu-id="5136d-124">O valor deve ser ' Enabled ' ou ' disabled '</span><span class="sxs-lookup"><span data-stu-id="5136d-124">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5136d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5136d-125">-ResourceGroupName</span></span>
<span data-ttu-id="5136d-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5136d-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5136d-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="5136d-127">-RetentionInDays</span></span>
<span data-ttu-id="5136d-128">Retenção em dias, 90 por padrão.</span><span class="sxs-lookup"><span data-stu-id="5136d-128">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5136d-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="5136d-129">-Tag</span></span>
<span data-ttu-id="5136d-130">Marcas de componente.</span><span class="sxs-lookup"><span data-stu-id="5136d-130">Component Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5136d-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5136d-131">-Confirm</span></span>
<span data-ttu-id="5136d-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5136d-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5136d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5136d-133">-WhatIf</span></span>
<span data-ttu-id="5136d-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5136d-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5136d-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5136d-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5136d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5136d-136">CommonParameters</span></span>
<span data-ttu-id="5136d-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5136d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5136d-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5136d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5136d-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5136d-139">INPUTS</span></span>

### <span data-ttu-id="5136d-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5136d-140">None</span></span>

## <span data-ttu-id="5136d-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5136d-141">OUTPUTS</span></span>

### <span data-ttu-id="5136d-142">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="5136d-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="5136d-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5136d-143">NOTES</span></span>

## <span data-ttu-id="5136d-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5136d-144">RELATED LINKS</span></span>
