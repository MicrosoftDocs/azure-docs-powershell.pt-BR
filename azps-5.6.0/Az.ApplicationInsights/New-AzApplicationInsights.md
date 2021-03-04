---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: db0ad78a942905846f764bb5d72a8ef3b209b6a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886110"
---
# <span data-ttu-id="8863c-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8863c-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="8863c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8863c-102">SYNOPSIS</span></span>
<span data-ttu-id="8863c-103">Criar um novo recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="8863c-103">Create a new application insights resource</span></span>

## <span data-ttu-id="8863c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8863c-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8863c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8863c-105">DESCRIPTION</span></span>
<span data-ttu-id="8863c-106">Criar um novo recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="8863c-106">Create a new application insights resource</span></span>

## <span data-ttu-id="8863c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8863c-107">EXAMPLES</span></span>

### <span data-ttu-id="8863c-108">Exemplo 1 Criar um novo recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="8863c-108">Example 1 Create a new application insights resource</span></span>
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

<span data-ttu-id="8863c-109">Adicionar um novo recurso de insights de aplicativo chamado "test" no grupo de recursos "testgroup" com o tipo "java"</span><span class="sxs-lookup"><span data-stu-id="8863c-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java"</span></span>

## <span data-ttu-id="8863c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8863c-110">PARAMETERS</span></span>

### <span data-ttu-id="8863c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8863c-111">-DefaultProfile</span></span>
<span data-ttu-id="8863c-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8863c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8863c-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="8863c-113">-Kind</span></span>
<span data-ttu-id="8863c-114">Tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8863c-114">Application kind.</span></span>

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

### <span data-ttu-id="8863c-115">-Location</span><span class="sxs-lookup"><span data-stu-id="8863c-115">-Location</span></span>
<span data-ttu-id="8863c-116">Local do recurso Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8863c-116">Application Insights Resource Location.</span></span>

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

### <span data-ttu-id="8863c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8863c-117">-Name</span></span>
<span data-ttu-id="8863c-118">Nome do recurso Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8863c-118">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="8863c-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="8863c-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="8863c-120">O tipo de acesso à rede para acessar a ingestão do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8863c-120">The network access type for accessing Application Insights ingestion.</span></span> <span data-ttu-id="8863c-121">O valor deve ser 'Habilitado' ou 'Desabilitado'</span><span class="sxs-lookup"><span data-stu-id="8863c-121">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="8863c-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="8863c-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="8863c-123">O tipo de acesso à rede para acessar a consulta Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8863c-123">The network access type for accessing Application Insights query.</span></span> <span data-ttu-id="8863c-124">O valor deve ser 'Habilitado' ou 'Desabilitado'</span><span class="sxs-lookup"><span data-stu-id="8863c-124">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="8863c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8863c-125">-ResourceGroupName</span></span>
<span data-ttu-id="8863c-126">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="8863c-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="8863c-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8863c-127">-RetentionInDays</span></span>
<span data-ttu-id="8863c-128">Retenção em dias, 90 por padrão.</span><span class="sxs-lookup"><span data-stu-id="8863c-128">Retention In Days, 90 by default.</span></span>

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

### <span data-ttu-id="8863c-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="8863c-129">-Tag</span></span>
<span data-ttu-id="8863c-130">Marcas de componente.</span><span class="sxs-lookup"><span data-stu-id="8863c-130">Component Tags.</span></span>

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

### <span data-ttu-id="8863c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8863c-131">-Confirm</span></span>
<span data-ttu-id="8863c-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8863c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8863c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8863c-133">-WhatIf</span></span>
<span data-ttu-id="8863c-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8863c-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8863c-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8863c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8863c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8863c-136">CommonParameters</span></span>
<span data-ttu-id="8863c-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8863c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8863c-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8863c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8863c-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8863c-139">INPUTS</span></span>

### <span data-ttu-id="8863c-140">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8863c-140">None</span></span>

## <span data-ttu-id="8863c-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8863c-141">OUTPUTS</span></span>

### <span data-ttu-id="8863c-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8863c-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="8863c-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="8863c-143">NOTES</span></span>

## <span data-ttu-id="8863c-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8863c-144">RELATED LINKS</span></span>
