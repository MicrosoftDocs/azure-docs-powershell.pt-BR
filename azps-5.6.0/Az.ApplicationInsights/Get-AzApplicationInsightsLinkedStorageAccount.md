---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: a059209e993f17ffb5eed1b29d1854f8387f3d8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887040"
---
# <span data-ttu-id="7d843-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7d843-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="7d843-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d843-102">SYNOPSIS</span></span>
<span data-ttu-id="7d843-103">Obter conta de armazenamento vinculada de insights de aplicativos</span><span class="sxs-lookup"><span data-stu-id="7d843-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="7d843-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7d843-104">SYNTAX</span></span>

### <span data-ttu-id="7d843-105">ByResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7d843-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d843-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d843-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d843-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d843-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d843-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7d843-108">DESCRIPTION</span></span>
<span data-ttu-id="7d843-109">Obter conta de armazenamento vinculada de insights de aplicativos</span><span class="sxs-lookup"><span data-stu-id="7d843-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="7d843-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d843-110">EXAMPLES</span></span>

### <span data-ttu-id="7d843-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7d843-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="7d843-112">Obter conta de armazenamento vinculada associada ao componente "componentName"</span><span class="sxs-lookup"><span data-stu-id="7d843-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="7d843-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7d843-113">PARAMETERS</span></span>

### <span data-ttu-id="7d843-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="7d843-114">-ComponentName</span></span>
<span data-ttu-id="7d843-115">Nome do componente</span><span class="sxs-lookup"><span data-stu-id="7d843-115">Component Name</span></span>

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

### <span data-ttu-id="7d843-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d843-116">-DefaultProfile</span></span>
<span data-ttu-id="7d843-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d843-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d843-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d843-118">-InputObject</span></span>
<span data-ttu-id="7d843-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7d843-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="7d843-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d843-120">-ResourceGroupName</span></span>
<span data-ttu-id="7d843-121">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7d843-121">Resource Group Name</span></span>

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

### <span data-ttu-id="7d843-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d843-122">-ResourceId</span></span>
<span data-ttu-id="7d843-123">ResourceId de componente</span><span class="sxs-lookup"><span data-stu-id="7d843-123">Component ResourceId</span></span>

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

### <span data-ttu-id="7d843-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d843-124">CommonParameters</span></span>
<span data-ttu-id="7d843-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d843-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d843-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d843-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d843-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d843-127">INPUTS</span></span>

### <span data-ttu-id="7d843-128">System.String</span><span class="sxs-lookup"><span data-stu-id="7d843-128">System.String</span></span>

### <span data-ttu-id="7d843-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7d843-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="7d843-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7d843-130">OUTPUTS</span></span>

### <span data-ttu-id="7d843-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="7d843-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="7d843-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="7d843-132">NOTES</span></span>

## <span data-ttu-id="7d843-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d843-133">RELATED LINKS</span></span>
