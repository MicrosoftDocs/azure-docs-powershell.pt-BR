---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/update-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 50391bcd4356f24db6107a64ee5bdec9827407f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887916"
---
# <span data-ttu-id="f4743-101">Update-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f4743-101">Update-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="f4743-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4743-102">SYNOPSIS</span></span>
<span data-ttu-id="f4743-103">Atualizar a conta de armazenamento vinculada de insights do aplicativo</span><span class="sxs-lookup"><span data-stu-id="f4743-103">Update application insights linked storage account</span></span>

## <span data-ttu-id="f4743-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f4743-104">SYNTAX</span></span>

### <span data-ttu-id="f4743-105">ByResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f4743-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4743-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4743-106">ByInputObjectParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4743-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4743-107">ByResourceIdParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4743-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f4743-108">DESCRIPTION</span></span>
<span data-ttu-id="f4743-109">Atualizar a conta de armazenamento vinculada de insights do aplicativo</span><span class="sxs-lookup"><span data-stu-id="f4743-109">Update application insights linked storage account</span></span>

## <span data-ttu-id="f4743-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4743-110">EXAMPLES</span></span>

### <span data-ttu-id="f4743-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f4743-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Update-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="f4743-112">Atualizar conta de armazenamento vinculado em componente "componentName" para associar a $account</span><span class="sxs-lookup"><span data-stu-id="f4743-112">Update linked storage account under component "componentName" to associate with $account</span></span>

## <span data-ttu-id="f4743-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f4743-113">PARAMETERS</span></span>

### <span data-ttu-id="f4743-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="f4743-114">-ComponentName</span></span>
<span data-ttu-id="f4743-115">Nome do componente</span><span class="sxs-lookup"><span data-stu-id="f4743-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4743-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4743-116">-DefaultProfile</span></span>
<span data-ttu-id="f4743-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f4743-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4743-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4743-118">-InputObject</span></span>
<span data-ttu-id="f4743-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f4743-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4743-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="f4743-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="f4743-121">ResourceId da Conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="f4743-121">Storage Account ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4743-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4743-122">-ResourceGroupName</span></span>
<span data-ttu-id="f4743-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="f4743-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4743-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4743-124">-ResourceId</span></span>
<span data-ttu-id="f4743-125">ResourceId de componente</span><span class="sxs-lookup"><span data-stu-id="f4743-125">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4743-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4743-126">-Confirm</span></span>
<span data-ttu-id="f4743-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4743-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4743-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4743-128">-WhatIf</span></span>
<span data-ttu-id="f4743-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f4743-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4743-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f4743-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4743-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4743-131">CommonParameters</span></span>
<span data-ttu-id="f4743-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4743-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4743-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4743-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4743-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4743-134">INPUTS</span></span>

### <span data-ttu-id="f4743-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f4743-135">System.String</span></span>

### <span data-ttu-id="f4743-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f4743-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="f4743-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f4743-137">OUTPUTS</span></span>

### <span data-ttu-id="f4743-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="f4743-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="f4743-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="f4743-139">NOTES</span></span>

## <span data-ttu-id="f4743-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4743-140">RELATED LINKS</span></span>
