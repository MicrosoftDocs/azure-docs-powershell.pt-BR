---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 6bb6a422af88c0d7cd911e575e9d49bcdafcd3d8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125661"
---
# <span data-ttu-id="2c64a-101">Remove-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c64a-101">Remove-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="2c64a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c64a-102">SYNOPSIS</span></span>
<span data-ttu-id="2c64a-103">Excluir conta de armazenamento vinculado do Application insights</span><span class="sxs-lookup"><span data-stu-id="2c64a-103">Delete application insights linked storage account</span></span>

## <span data-ttu-id="2c64a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c64a-104">SYNTAX</span></span>

### <span data-ttu-id="2c64a-105">ByResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2c64a-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c64a-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c64a-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c64a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c64a-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c64a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c64a-108">DESCRIPTION</span></span>
<span data-ttu-id="2c64a-109">Excluir conta de armazenamento vinculado do Application insights</span><span class="sxs-lookup"><span data-stu-id="2c64a-109">Delete application insights linked storage account</span></span>

## <span data-ttu-id="2c64a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c64a-110">EXAMPLES</span></span>

### <span data-ttu-id="2c64a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2c64a-111">Example 1</span></span>
```powershell
Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Remove-AzApplicationInsightsLinkedStorageAccount
```

<span data-ttu-id="2c64a-112">Excluir conta de armazenamento vinculado associado ao componente "ComponentName" do Application insights</span><span class="sxs-lookup"><span data-stu-id="2c64a-112">Delete linked storage account associated with application insights component "componentName"</span></span>

## <span data-ttu-id="2c64a-113">OS</span><span class="sxs-lookup"><span data-stu-id="2c64a-113">PARAMETERS</span></span>

### <span data-ttu-id="2c64a-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="2c64a-114">-ComponentName</span></span>
<span data-ttu-id="2c64a-115">Nome do componente</span><span class="sxs-lookup"><span data-stu-id="2c64a-115">Component Name</span></span>

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

### <span data-ttu-id="2c64a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c64a-116">-DefaultProfile</span></span>
<span data-ttu-id="2c64a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c64a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c64a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c64a-118">-InputObject</span></span>
<span data-ttu-id="2c64a-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="2c64a-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="2c64a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c64a-120">-ResourceGroupName</span></span>
<span data-ttu-id="2c64a-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2c64a-121">Resource Group Name</span></span>

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

### <span data-ttu-id="2c64a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c64a-122">-ResourceId</span></span>
<span data-ttu-id="2c64a-123">ResourceId do componente</span><span class="sxs-lookup"><span data-stu-id="2c64a-123">Component ResourceId</span></span>

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

### <span data-ttu-id="2c64a-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2c64a-124">-Confirm</span></span>
<span data-ttu-id="2c64a-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c64a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c64a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c64a-126">-WhatIf</span></span>
<span data-ttu-id="2c64a-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2c64a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c64a-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c64a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c64a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c64a-129">CommonParameters</span></span>
<span data-ttu-id="2c64a-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c64a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c64a-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c64a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c64a-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c64a-132">INPUTS</span></span>

### <span data-ttu-id="2c64a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2c64a-133">System.String</span></span>

### <span data-ttu-id="2c64a-134">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="2c64a-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="2c64a-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c64a-135">OUTPUTS</span></span>

### <span data-ttu-id="2c64a-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2c64a-136">System.Boolean</span></span>

## <span data-ttu-id="2c64a-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c64a-137">NOTES</span></span>

## <span data-ttu-id="2c64a-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c64a-138">RELATED LINKS</span></span>
