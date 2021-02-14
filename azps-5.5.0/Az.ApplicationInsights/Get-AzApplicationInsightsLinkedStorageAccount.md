---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 7e879cd4e513ebdad297933269e373c625f2e407
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115538"
---
# <span data-ttu-id="a138c-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a138c-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="a138c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a138c-102">SYNOPSIS</span></span>
<span data-ttu-id="a138c-103">Obter uma conta de armazenamento vinculada de insights de aplicativos</span><span class="sxs-lookup"><span data-stu-id="a138c-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="a138c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a138c-104">SYNTAX</span></span>

### <span data-ttu-id="a138c-105">ByResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a138c-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a138c-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a138c-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a138c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a138c-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a138c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a138c-108">DESCRIPTION</span></span>
<span data-ttu-id="a138c-109">Obter uma conta de armazenamento vinculada de insights de aplicativos</span><span class="sxs-lookup"><span data-stu-id="a138c-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="a138c-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a138c-110">EXAMPLES</span></span>

### <span data-ttu-id="a138c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a138c-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="a138c-112">Obter conta de armazenamento vinculada associada ao componente "componentName"</span><span class="sxs-lookup"><span data-stu-id="a138c-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="a138c-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a138c-113">PARAMETERS</span></span>

### <span data-ttu-id="a138c-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="a138c-114">-ComponentName</span></span>
<span data-ttu-id="a138c-115">Nome do Componente</span><span class="sxs-lookup"><span data-stu-id="a138c-115">Component Name</span></span>

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

### <span data-ttu-id="a138c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a138c-116">-DefaultProfile</span></span>
<span data-ttu-id="a138c-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a138c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a138c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a138c-118">-InputObject</span></span>
<span data-ttu-id="a138c-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a138c-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="a138c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a138c-120">-ResourceGroupName</span></span>
<span data-ttu-id="a138c-121">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="a138c-121">Resource Group Name</span></span>

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

### <span data-ttu-id="a138c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a138c-122">-ResourceId</span></span>
<span data-ttu-id="a138c-123">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="a138c-123">Component ResourceId</span></span>

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

### <span data-ttu-id="a138c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a138c-124">CommonParameters</span></span>
<span data-ttu-id="a138c-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a138c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a138c-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a138c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a138c-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="a138c-127">INPUTS</span></span>

### <span data-ttu-id="a138c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a138c-128">System.String</span></span>

### <span data-ttu-id="a138c-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a138c-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="a138c-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="a138c-130">OUTPUTS</span></span>

### <span data-ttu-id="a138c-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="a138c-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="a138c-132">Notas</span><span class="sxs-lookup"><span data-stu-id="a138c-132">NOTES</span></span>

## <span data-ttu-id="a138c-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a138c-133">RELATED LINKS</span></span>
