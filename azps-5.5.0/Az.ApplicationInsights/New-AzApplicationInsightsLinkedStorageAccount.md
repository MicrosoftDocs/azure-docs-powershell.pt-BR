---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 652a5668bd641ae1b68093f431e0aa0963aca50b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112284"
---
# <span data-ttu-id="891b4-101">New-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="891b4-101">New-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="891b4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="891b4-102">SYNOPSIS</span></span>
<span data-ttu-id="891b4-103">Criar uma conta de armazenamento vinculada de insights de aplicativos</span><span class="sxs-lookup"><span data-stu-id="891b4-103">Create an application insights linked storage account</span></span>

## <span data-ttu-id="891b4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="891b4-104">SYNTAX</span></span>

### <span data-ttu-id="891b4-105">ByResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="891b4-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="891b4-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="891b4-106">ByInputObjectParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="891b4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="891b4-107">ByResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="891b4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="891b4-108">DESCRIPTION</span></span>
<span data-ttu-id="891b4-109">Criar uma conta de armazenamento vinculada de insights de aplicativos</span><span class="sxs-lookup"><span data-stu-id="891b4-109">Create an application insights linked storage account</span></span>

## <span data-ttu-id="891b4-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="891b4-110">EXAMPLES</span></span>

### <span data-ttu-id="891b4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="891b4-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | New-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="891b4-112">Criar contas de armazenamento $account em componente "componentName"</span><span class="sxs-lookup"><span data-stu-id="891b4-112">Create linked storage account $account under component "componentName"</span></span>

## <span data-ttu-id="891b4-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="891b4-113">PARAMETERS</span></span>

### <span data-ttu-id="891b4-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="891b4-114">-ComponentName</span></span>
<span data-ttu-id="891b4-115">Nome do Componente</span><span class="sxs-lookup"><span data-stu-id="891b4-115">Component Name</span></span>

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

### <span data-ttu-id="891b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="891b4-116">-DefaultProfile</span></span>
<span data-ttu-id="891b4-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="891b4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="891b4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="891b4-118">-InputObject</span></span>
<span data-ttu-id="891b4-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="891b4-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="891b4-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="891b4-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="891b4-121">ResourceId da Conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="891b4-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="891b4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="891b4-122">-ResourceGroupName</span></span>
<span data-ttu-id="891b4-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="891b4-123">Resource Group Name</span></span>

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

### <span data-ttu-id="891b4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="891b4-124">-ResourceId</span></span>
<span data-ttu-id="891b4-125">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="891b4-125">Component ResourceId</span></span>

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

### <span data-ttu-id="891b4-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="891b4-126">-Confirm</span></span>
<span data-ttu-id="891b4-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="891b4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="891b4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="891b4-128">-WhatIf</span></span>
<span data-ttu-id="891b4-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="891b4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="891b4-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="891b4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="891b4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="891b4-131">CommonParameters</span></span>
<span data-ttu-id="891b4-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="891b4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="891b4-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="891b4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="891b4-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="891b4-134">INPUTS</span></span>

### <span data-ttu-id="891b4-135">System.String</span><span class="sxs-lookup"><span data-stu-id="891b4-135">System.String</span></span>

### <span data-ttu-id="891b4-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="891b4-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="891b4-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="891b4-137">OUTPUTS</span></span>

### <span data-ttu-id="891b4-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="891b4-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="891b4-139">Notas</span><span class="sxs-lookup"><span data-stu-id="891b4-139">NOTES</span></span>

## <span data-ttu-id="891b4-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="891b4-140">RELATED LINKS</span></span>
