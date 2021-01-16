---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 7e879cd4e513ebdad297933269e373c625f2e407
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272058"
---
# <span data-ttu-id="d1a64-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d1a64-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="d1a64-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1a64-102">SYNOPSIS</span></span>
<span data-ttu-id="d1a64-103">Obter conta de armazenamento vinculado do Application insights</span><span class="sxs-lookup"><span data-stu-id="d1a64-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="d1a64-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1a64-104">SYNTAX</span></span>

### <span data-ttu-id="d1a64-105">ByResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d1a64-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a64-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a64-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a64-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a64-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1a64-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d1a64-108">DESCRIPTION</span></span>
<span data-ttu-id="d1a64-109">Obter conta de armazenamento vinculado do Application insights</span><span class="sxs-lookup"><span data-stu-id="d1a64-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="d1a64-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1a64-110">EXAMPLES</span></span>

### <span data-ttu-id="d1a64-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d1a64-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="d1a64-112">Obter uma conta de armazenamento vinculada associada ao componente "ComponentName"</span><span class="sxs-lookup"><span data-stu-id="d1a64-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="d1a64-113">OS</span><span class="sxs-lookup"><span data-stu-id="d1a64-113">PARAMETERS</span></span>

### <span data-ttu-id="d1a64-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="d1a64-114">-ComponentName</span></span>
<span data-ttu-id="d1a64-115">Nome do componente</span><span class="sxs-lookup"><span data-stu-id="d1a64-115">Component Name</span></span>

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

### <span data-ttu-id="d1a64-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1a64-116">-DefaultProfile</span></span>
<span data-ttu-id="d1a64-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a64-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1a64-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1a64-118">-InputObject</span></span>
<span data-ttu-id="d1a64-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="d1a64-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="d1a64-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1a64-120">-ResourceGroupName</span></span>
<span data-ttu-id="d1a64-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d1a64-121">Resource Group Name</span></span>

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

### <span data-ttu-id="d1a64-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1a64-122">-ResourceId</span></span>
<span data-ttu-id="d1a64-123">ResourceId do componente</span><span class="sxs-lookup"><span data-stu-id="d1a64-123">Component ResourceId</span></span>

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

### <span data-ttu-id="d1a64-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1a64-124">CommonParameters</span></span>
<span data-ttu-id="d1a64-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1a64-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1a64-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1a64-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1a64-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d1a64-127">INPUTS</span></span>

### <span data-ttu-id="d1a64-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d1a64-128">System.String</span></span>

### <span data-ttu-id="d1a64-129">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="d1a64-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="d1a64-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d1a64-130">OUTPUTS</span></span>

### <span data-ttu-id="d1a64-131">Microsoft. Azure. Commands. ApplicationInsights. Models. PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="d1a64-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="d1a64-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d1a64-132">NOTES</span></span>

## <span data-ttu-id="d1a64-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1a64-133">RELATED LINKS</span></span>
