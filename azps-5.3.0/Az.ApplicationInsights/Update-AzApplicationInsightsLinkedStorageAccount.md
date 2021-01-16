---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ef27923fbffc92a0190419cc5949c0b841b95dc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272041"
---
# <span data-ttu-id="fbca9-101">Update-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fbca9-101">Update-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="fbca9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fbca9-102">SYNOPSIS</span></span>
<span data-ttu-id="fbca9-103">Atualizar a conta de armazenamento vinculado do Application insights</span><span class="sxs-lookup"><span data-stu-id="fbca9-103">Update application insights linked storage account</span></span>

## <span data-ttu-id="fbca9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbca9-104">SYNTAX</span></span>

### <span data-ttu-id="fbca9-105">ByResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fbca9-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fbca9-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbca9-106">ByInputObjectParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fbca9-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbca9-107">ByResourceIdParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbca9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fbca9-108">DESCRIPTION</span></span>
<span data-ttu-id="fbca9-109">Atualizar a conta de armazenamento vinculado do Application insights</span><span class="sxs-lookup"><span data-stu-id="fbca9-109">Update application insights linked storage account</span></span>

## <span data-ttu-id="fbca9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fbca9-110">EXAMPLES</span></span>

### <span data-ttu-id="fbca9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fbca9-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Update-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="fbca9-112">Atualize a conta de armazenamento vinculado em Component "ComponentName" para associar-se a $account</span><span class="sxs-lookup"><span data-stu-id="fbca9-112">Update linked storage account under component "componentName" to associate with $account</span></span>

## <span data-ttu-id="fbca9-113">OS</span><span class="sxs-lookup"><span data-stu-id="fbca9-113">PARAMETERS</span></span>

### <span data-ttu-id="fbca9-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="fbca9-114">-ComponentName</span></span>
<span data-ttu-id="fbca9-115">Nome do componente</span><span class="sxs-lookup"><span data-stu-id="fbca9-115">Component Name</span></span>

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

### <span data-ttu-id="fbca9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbca9-116">-DefaultProfile</span></span>
<span data-ttu-id="fbca9-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fbca9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbca9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbca9-118">-InputObject</span></span>
<span data-ttu-id="fbca9-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="fbca9-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="fbca9-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="fbca9-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="fbca9-121">ResourceId da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="fbca9-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="fbca9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbca9-122">-ResourceGroupName</span></span>
<span data-ttu-id="fbca9-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fbca9-123">Resource Group Name</span></span>

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

### <span data-ttu-id="fbca9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbca9-124">-ResourceId</span></span>
<span data-ttu-id="fbca9-125">ResourceId do componente</span><span class="sxs-lookup"><span data-stu-id="fbca9-125">Component ResourceId</span></span>

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

### <span data-ttu-id="fbca9-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fbca9-126">-Confirm</span></span>
<span data-ttu-id="fbca9-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbca9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbca9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbca9-128">-WhatIf</span></span>
<span data-ttu-id="fbca9-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fbca9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbca9-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fbca9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbca9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbca9-131">CommonParameters</span></span>
<span data-ttu-id="fbca9-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbca9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbca9-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbca9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbca9-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fbca9-134">INPUTS</span></span>

### <span data-ttu-id="fbca9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="fbca9-135">System.String</span></span>

### <span data-ttu-id="fbca9-136">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="fbca9-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="fbca9-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fbca9-137">OUTPUTS</span></span>

### <span data-ttu-id="fbca9-138">Microsoft. Azure. Commands. ApplicationInsights. Models. PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="fbca9-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="fbca9-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fbca9-139">NOTES</span></span>

## <span data-ttu-id="fbca9-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fbca9-140">RELATED LINKS</span></span>
