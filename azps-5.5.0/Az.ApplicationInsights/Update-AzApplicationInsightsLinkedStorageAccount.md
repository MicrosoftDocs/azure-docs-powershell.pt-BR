---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ef27923fbffc92a0190419cc5949c0b841b95dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112273"
---
# <span data-ttu-id="bdd3f-101">Update-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdd3f-101">Update-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="bdd3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bdd3f-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd3f-103">Atualizar conta de armazenamento vinculada do insights do aplicativo</span><span class="sxs-lookup"><span data-stu-id="bdd3f-103">Update application insights linked storage account</span></span>

## <span data-ttu-id="bdd3f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bdd3f-104">SYNTAX</span></span>

### <span data-ttu-id="bdd3f-105">ByResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bdd3f-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdd3f-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdd3f-106">ByInputObjectParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdd3f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdd3f-107">ByResourceIdParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdd3f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="bdd3f-108">DESCRIPTION</span></span>
<span data-ttu-id="bdd3f-109">Atualizar conta de armazenamento vinculada do insights do aplicativo</span><span class="sxs-lookup"><span data-stu-id="bdd3f-109">Update application insights linked storage account</span></span>

## <span data-ttu-id="bdd3f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bdd3f-110">EXAMPLES</span></span>

### <span data-ttu-id="bdd3f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bdd3f-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Update-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="bdd3f-112">Atualizar a conta de armazenamento vinculada em "componentName" do componente para associar ao $account</span><span class="sxs-lookup"><span data-stu-id="bdd3f-112">Update linked storage account under component "componentName" to associate with $account</span></span>

## <span data-ttu-id="bdd3f-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bdd3f-113">PARAMETERS</span></span>

### <span data-ttu-id="bdd3f-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="bdd3f-114">-ComponentName</span></span>
<span data-ttu-id="bdd3f-115">Nome do Componente</span><span class="sxs-lookup"><span data-stu-id="bdd3f-115">Component Name</span></span>

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

### <span data-ttu-id="bdd3f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdd3f-116">-DefaultProfile</span></span>
<span data-ttu-id="bdd3f-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bdd3f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdd3f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdd3f-118">-InputObject</span></span>
<span data-ttu-id="bdd3f-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="bdd3f-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="bdd3f-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="bdd3f-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="bdd3f-121">ResourceId da Conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="bdd3f-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="bdd3f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdd3f-122">-ResourceGroupName</span></span>
<span data-ttu-id="bdd3f-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="bdd3f-123">Resource Group Name</span></span>

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

### <span data-ttu-id="bdd3f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdd3f-124">-ResourceId</span></span>
<span data-ttu-id="bdd3f-125">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdd3f-125">Component ResourceId</span></span>

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

### <span data-ttu-id="bdd3f-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bdd3f-126">-Confirm</span></span>
<span data-ttu-id="bdd3f-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdd3f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdd3f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdd3f-128">-WhatIf</span></span>
<span data-ttu-id="bdd3f-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bdd3f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdd3f-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bdd3f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdd3f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd3f-131">CommonParameters</span></span>
<span data-ttu-id="bdd3f-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdd3f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd3f-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bdd3f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd3f-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="bdd3f-134">INPUTS</span></span>

### <span data-ttu-id="bdd3f-135">System.String</span><span class="sxs-lookup"><span data-stu-id="bdd3f-135">System.String</span></span>

### <span data-ttu-id="bdd3f-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="bdd3f-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="bdd3f-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="bdd3f-137">OUTPUTS</span></span>

### <span data-ttu-id="bdd3f-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="bdd3f-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="bdd3f-139">Notas</span><span class="sxs-lookup"><span data-stu-id="bdd3f-139">NOTES</span></span>

## <span data-ttu-id="bdd3f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bdd3f-140">RELATED LINKS</span></span>
