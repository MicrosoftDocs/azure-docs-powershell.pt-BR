---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 652a5668bd641ae1b68093f431e0aa0963aca50b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118145"
---
# <span data-ttu-id="39144-101">New-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39144-101">New-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="39144-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="39144-102">SYNOPSIS</span></span>
<span data-ttu-id="39144-103">Criar uma conta de armazenamento vinculada do Application insights</span><span class="sxs-lookup"><span data-stu-id="39144-103">Create an application insights linked storage account</span></span>

## <span data-ttu-id="39144-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39144-104">SYNTAX</span></span>

### <span data-ttu-id="39144-105">ByResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="39144-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39144-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39144-106">ByInputObjectParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39144-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39144-107">ByResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39144-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="39144-108">DESCRIPTION</span></span>
<span data-ttu-id="39144-109">Criar uma conta de armazenamento vinculada do Application insights</span><span class="sxs-lookup"><span data-stu-id="39144-109">Create an application insights linked storage account</span></span>

## <span data-ttu-id="39144-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="39144-110">EXAMPLES</span></span>

### <span data-ttu-id="39144-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="39144-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | New-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="39144-112">Criar conta de armazenamento vinculado $account em componente "ComponentName"</span><span class="sxs-lookup"><span data-stu-id="39144-112">Create linked storage account $account under component "componentName"</span></span>

## <span data-ttu-id="39144-113">OS</span><span class="sxs-lookup"><span data-stu-id="39144-113">PARAMETERS</span></span>

### <span data-ttu-id="39144-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="39144-114">-ComponentName</span></span>
<span data-ttu-id="39144-115">Nome do componente</span><span class="sxs-lookup"><span data-stu-id="39144-115">Component Name</span></span>

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

### <span data-ttu-id="39144-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39144-116">-DefaultProfile</span></span>
<span data-ttu-id="39144-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="39144-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39144-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39144-118">-InputObject</span></span>
<span data-ttu-id="39144-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="39144-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="39144-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="39144-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="39144-121">ResourceId da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="39144-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="39144-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39144-122">-ResourceGroupName</span></span>
<span data-ttu-id="39144-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="39144-123">Resource Group Name</span></span>

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

### <span data-ttu-id="39144-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39144-124">-ResourceId</span></span>
<span data-ttu-id="39144-125">ResourceId do componente</span><span class="sxs-lookup"><span data-stu-id="39144-125">Component ResourceId</span></span>

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

### <span data-ttu-id="39144-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="39144-126">-Confirm</span></span>
<span data-ttu-id="39144-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39144-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39144-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39144-128">-WhatIf</span></span>
<span data-ttu-id="39144-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="39144-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39144-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="39144-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39144-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39144-131">CommonParameters</span></span>
<span data-ttu-id="39144-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39144-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39144-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39144-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39144-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="39144-134">INPUTS</span></span>

### <span data-ttu-id="39144-135">System. String</span><span class="sxs-lookup"><span data-stu-id="39144-135">System.String</span></span>

### <span data-ttu-id="39144-136">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="39144-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="39144-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="39144-137">OUTPUTS</span></span>

### <span data-ttu-id="39144-138">Microsoft. Azure. Commands. ApplicationInsights. Models. PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="39144-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="39144-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="39144-139">NOTES</span></span>

## <span data-ttu-id="39144-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39144-140">RELATED LINKS</span></span>
