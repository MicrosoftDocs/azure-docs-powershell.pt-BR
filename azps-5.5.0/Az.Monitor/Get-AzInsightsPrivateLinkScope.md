---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: d5986694ad0064265bbd4bad6e1efc378683ce97
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117529"
---
# <span data-ttu-id="d59d9-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d59d9-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="d59d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d59d9-102">SYNOPSIS</span></span>
<span data-ttu-id="d59d9-103">Obter escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="d59d9-103">Get private link scope</span></span>

## <span data-ttu-id="d59d9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d59d9-104">SYNTAX</span></span>

### <span data-ttu-id="d59d9-105">ByResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d59d9-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d59d9-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d59d9-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d59d9-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d59d9-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d59d9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d59d9-108">DESCRIPTION</span></span>
<span data-ttu-id="d59d9-109">Listar ou obter escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="d59d9-109">List or get private link scope</span></span> 

## <span data-ttu-id="d59d9-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d59d9-110">EXAMPLES</span></span>

### <span data-ttu-id="d59d9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d59d9-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="d59d9-112">Listar escopos de vínculo privado no grupo de recursos "rg_name"</span><span class="sxs-lookup"><span data-stu-id="d59d9-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="d59d9-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d59d9-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="d59d9-114">Obter escopo de link privado com o nome "scope_name" no grupo de recursos "rg_name"</span><span class="sxs-lookup"><span data-stu-id="d59d9-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="d59d9-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d59d9-115">PARAMETERS</span></span>

### <span data-ttu-id="d59d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d59d9-116">-DefaultProfile</span></span>
<span data-ttu-id="d59d9-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d59d9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d59d9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d59d9-118">-Name</span></span>
<span data-ttu-id="d59d9-119">Nome do escopo do link particular</span><span class="sxs-lookup"><span data-stu-id="d59d9-119">Private Link Scope Name</span></span>

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

### <span data-ttu-id="d59d9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d59d9-120">-ResourceGroupName</span></span>
<span data-ttu-id="d59d9-121">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d59d9-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="d59d9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d59d9-122">-ResourceId</span></span>
<span data-ttu-id="d59d9-123">ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="d59d9-123">Resource Id</span></span>

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

### <span data-ttu-id="d59d9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d59d9-124">CommonParameters</span></span>
<span data-ttu-id="d59d9-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d59d9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d59d9-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d59d9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d59d9-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="d59d9-127">INPUTS</span></span>

### <span data-ttu-id="d59d9-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d59d9-128">System.String</span></span>

## <span data-ttu-id="d59d9-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="d59d9-129">OUTPUTS</span></span>

### <span data-ttu-id="d59d9-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d59d9-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="d59d9-131">Notas</span><span class="sxs-lookup"><span data-stu-id="d59d9-131">NOTES</span></span>

## <span data-ttu-id="d59d9-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d59d9-132">RELATED LINKS</span></span>
