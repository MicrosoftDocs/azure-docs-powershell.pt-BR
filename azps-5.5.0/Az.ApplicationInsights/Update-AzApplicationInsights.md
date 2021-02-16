---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: f34868c31a99e67596d244a1f69224db5c25349a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127140"
---
# <span data-ttu-id="05a46-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="05a46-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="05a46-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="05a46-102">SYNOPSIS</span></span>
<span data-ttu-id="05a46-103">atualizar um recurso de ideias de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="05a46-103">update an existing application insights resource</span></span>

## <span data-ttu-id="05a46-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05a46-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05a46-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="05a46-105">DESCRIPTION</span></span>
<span data-ttu-id="05a46-106">atualizar um recurso de ideias de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="05a46-106">update an existing application insights resource</span></span>

## <span data-ttu-id="05a46-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="05a46-107">EXAMPLES</span></span>

### <span data-ttu-id="05a46-108">Exemplo 1 Componente atualizar informações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="05a46-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="05a46-109">componente atualizar insights do aplicativo "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery ambos como "Desabilitados"</span><span class="sxs-lookup"><span data-stu-id="05a46-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="05a46-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05a46-110">PARAMETERS</span></span>

### <span data-ttu-id="05a46-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05a46-111">-DefaultProfile</span></span>
<span data-ttu-id="05a46-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="05a46-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05a46-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="05a46-113">-Name</span></span>
<span data-ttu-id="05a46-114">Nome do recurso Informações do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="05a46-114">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="05a46-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="05a46-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="05a46-116">O tipo de acesso à rede para acessar a ingestão de Informações do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="05a46-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="05a46-117">O valor deve ser "Habilitado" ou "Desabilitado"</span><span class="sxs-lookup"><span data-stu-id="05a46-117">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="05a46-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="05a46-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="05a46-119">O tipo de acesso à rede para acessar a consulta Informações do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="05a46-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="05a46-120">O valor deve ser "Habilitado" ou "Desabilitado"</span><span class="sxs-lookup"><span data-stu-id="05a46-120">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="05a46-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05a46-121">-ResourceGroupName</span></span>
<span data-ttu-id="05a46-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="05a46-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="05a46-123">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="05a46-123">-RetentionInDays</span></span>
<span data-ttu-id="05a46-124">Retenção em dias, 90 por padrão.</span><span class="sxs-lookup"><span data-stu-id="05a46-124">Retention In Days, 90 by default.</span></span>

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

### <span data-ttu-id="05a46-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="05a46-125">-Tag</span></span>
<span data-ttu-id="05a46-126">Marcas de componentes.</span><span class="sxs-lookup"><span data-stu-id="05a46-126">Component Tags.</span></span>

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

### <span data-ttu-id="05a46-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="05a46-127">-Confirm</span></span>
<span data-ttu-id="05a46-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05a46-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05a46-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05a46-129">-WhatIf</span></span>
<span data-ttu-id="05a46-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="05a46-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05a46-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="05a46-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05a46-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05a46-132">CommonParameters</span></span>
<span data-ttu-id="05a46-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05a46-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05a46-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05a46-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05a46-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="05a46-135">INPUTS</span></span>

### <span data-ttu-id="05a46-136">System.String</span><span class="sxs-lookup"><span data-stu-id="05a46-136">System.String</span></span>

## <span data-ttu-id="05a46-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="05a46-137">OUTPUTS</span></span>

### <span data-ttu-id="05a46-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="05a46-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="05a46-139">Notas</span><span class="sxs-lookup"><span data-stu-id="05a46-139">NOTES</span></span>

## <span data-ttu-id="05a46-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05a46-140">RELATED LINKS</span></span>
