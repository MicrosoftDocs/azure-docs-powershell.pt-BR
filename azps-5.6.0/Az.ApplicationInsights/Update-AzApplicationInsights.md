---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: ac5e8bbc65a8435042d9f525cd1a3d35fa050398
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901366"
---
# <span data-ttu-id="c7fa9-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c7fa9-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="c7fa9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="c7fa9-103">atualizar um recurso de insights de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="c7fa9-103">update an existing application insights resource</span></span>

## <span data-ttu-id="c7fa9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c7fa9-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7fa9-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c7fa9-105">DESCRIPTION</span></span>
<span data-ttu-id="c7fa9-106">atualizar um recurso de insights de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="c7fa9-106">update an existing application insights resource</span></span>

## <span data-ttu-id="c7fa9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7fa9-107">EXAMPLES</span></span>

### <span data-ttu-id="c7fa9-108">Exemplo 1 Atualizar componente de insights do aplicativo</span><span class="sxs-lookup"><span data-stu-id="c7fa9-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="c7fa9-109">atualizar o componente de insights do aplicativo "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery ambos como "Desabilitados"</span><span class="sxs-lookup"><span data-stu-id="c7fa9-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="c7fa9-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c7fa9-110">PARAMETERS</span></span>

### <span data-ttu-id="c7fa9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7fa9-111">-DefaultProfile</span></span>
<span data-ttu-id="c7fa9-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c7fa9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7fa9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c7fa9-113">-Name</span></span>
<span data-ttu-id="c7fa9-114">Nome do recurso Application Insights.</span><span class="sxs-lookup"><span data-stu-id="c7fa9-114">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="c7fa9-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="c7fa9-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="c7fa9-116">O tipo de acesso à rede para acessar a ingestão do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="c7fa9-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="c7fa9-117">O valor deve ser 'Habilitado' ou 'Desabilitado'</span><span class="sxs-lookup"><span data-stu-id="c7fa9-117">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7fa9-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="c7fa9-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="c7fa9-119">O tipo de acesso à rede para acessar a consulta Application Insights.</span><span class="sxs-lookup"><span data-stu-id="c7fa9-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="c7fa9-120">O valor deve ser 'Habilitado' ou 'Desabilitado'</span><span class="sxs-lookup"><span data-stu-id="c7fa9-120">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7fa9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7fa9-121">-ResourceGroupName</span></span>
<span data-ttu-id="c7fa9-122">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="c7fa9-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="c7fa9-123">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="c7fa9-123">-RetentionInDays</span></span>
<span data-ttu-id="c7fa9-124">Retenção em dias, 90 por padrão.</span><span class="sxs-lookup"><span data-stu-id="c7fa9-124">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7fa9-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="c7fa9-125">-Tag</span></span>
<span data-ttu-id="c7fa9-126">Marcas de componente.</span><span class="sxs-lookup"><span data-stu-id="c7fa9-126">Component Tags.</span></span>

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

### <span data-ttu-id="c7fa9-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7fa9-127">-Confirm</span></span>
<span data-ttu-id="c7fa9-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7fa9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7fa9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7fa9-129">-WhatIf</span></span>
<span data-ttu-id="c7fa9-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c7fa9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7fa9-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c7fa9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7fa9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7fa9-132">CommonParameters</span></span>
<span data-ttu-id="c7fa9-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7fa9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7fa9-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7fa9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7fa9-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7fa9-135">INPUTS</span></span>

### <span data-ttu-id="c7fa9-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c7fa9-136">System.String</span></span>

## <span data-ttu-id="c7fa9-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c7fa9-137">OUTPUTS</span></span>

### <span data-ttu-id="c7fa9-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c7fa9-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="c7fa9-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="c7fa9-139">NOTES</span></span>

## <span data-ttu-id="c7fa9-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7fa9-140">RELATED LINKS</span></span>
