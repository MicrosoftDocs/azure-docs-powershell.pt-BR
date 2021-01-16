---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: f34868c31a99e67596d244a1f69224db5c25349a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272036"
---
# <span data-ttu-id="14ede-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="14ede-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="14ede-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14ede-102">SYNOPSIS</span></span>
<span data-ttu-id="14ede-103">atualizar um recurso do insights do aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="14ede-103">update an existing application insights resource</span></span>

## <span data-ttu-id="14ede-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14ede-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14ede-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14ede-105">DESCRIPTION</span></span>
<span data-ttu-id="14ede-106">atualizar um recurso do insights do aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="14ede-106">update an existing application insights resource</span></span>

## <span data-ttu-id="14ede-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14ede-107">EXAMPLES</span></span>

### <span data-ttu-id="14ede-108">Exemplo 1 componente de informações de atualização do aplicativo</span><span class="sxs-lookup"><span data-stu-id="14ede-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="14ede-109">Atualize o componente insights do Application insights "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery ambas para "Disabled"</span><span class="sxs-lookup"><span data-stu-id="14ede-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="14ede-110">OS</span><span class="sxs-lookup"><span data-stu-id="14ede-110">PARAMETERS</span></span>

### <span data-ttu-id="14ede-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14ede-111">-DefaultProfile</span></span>
<span data-ttu-id="14ede-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14ede-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14ede-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="14ede-113">-Name</span></span>
<span data-ttu-id="14ede-114">Nome do recurso do Application insights.</span><span class="sxs-lookup"><span data-stu-id="14ede-114">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="14ede-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="14ede-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="14ede-116">O tipo de acesso à rede para acessar a inclusão de insights do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="14ede-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="14ede-117">O valor deve ser ' Enabled ' ou ' disabled '</span><span class="sxs-lookup"><span data-stu-id="14ede-117">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="14ede-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="14ede-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="14ede-119">O tipo de acesso à rede para acessar a consulta do Application insights.</span><span class="sxs-lookup"><span data-stu-id="14ede-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="14ede-120">O valor deve ser ' Enabled ' ou ' disabled '</span><span class="sxs-lookup"><span data-stu-id="14ede-120">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="14ede-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14ede-121">-ResourceGroupName</span></span>
<span data-ttu-id="14ede-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="14ede-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="14ede-123">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="14ede-123">-RetentionInDays</span></span>
<span data-ttu-id="14ede-124">Retenção em dias, 90 por padrão.</span><span class="sxs-lookup"><span data-stu-id="14ede-124">Retention In Days, 90 by default.</span></span>

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

### <span data-ttu-id="14ede-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="14ede-125">-Tag</span></span>
<span data-ttu-id="14ede-126">Marcas de componente.</span><span class="sxs-lookup"><span data-stu-id="14ede-126">Component Tags.</span></span>

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

### <span data-ttu-id="14ede-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="14ede-127">-Confirm</span></span>
<span data-ttu-id="14ede-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14ede-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14ede-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14ede-129">-WhatIf</span></span>
<span data-ttu-id="14ede-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14ede-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14ede-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14ede-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14ede-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14ede-132">CommonParameters</span></span>
<span data-ttu-id="14ede-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14ede-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14ede-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14ede-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14ede-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14ede-135">INPUTS</span></span>

### <span data-ttu-id="14ede-136">System. String</span><span class="sxs-lookup"><span data-stu-id="14ede-136">System.String</span></span>

## <span data-ttu-id="14ede-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14ede-137">OUTPUTS</span></span>

### <span data-ttu-id="14ede-138">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="14ede-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="14ede-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14ede-139">NOTES</span></span>

## <span data-ttu-id="14ede-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14ede-140">RELATED LINKS</span></span>
