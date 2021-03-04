---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/get-azsmartgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
ms.openlocfilehash: 52060a4d7624981ee29749c4f0dba3cc8a38fda5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890900"
---
# <span data-ttu-id="007d2-101">Get-AzSmartGroup</span><span class="sxs-lookup"><span data-stu-id="007d2-101">Get-AzSmartGroup</span></span>

## <span data-ttu-id="007d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="007d2-102">SYNOPSIS</span></span>
<span data-ttu-id="007d2-103">Obtém informações de Grupos Inteligentes</span><span class="sxs-lookup"><span data-stu-id="007d2-103">Gets Smart Groups information</span></span>

## <span data-ttu-id="007d2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="007d2-104">SYNTAX</span></span>

### <span data-ttu-id="007d2-105">SmartGroupsListByFilter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="007d2-105">SmartGroupsListByFilter (Default)</span></span>
```
Get-AzSmartGroup [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="007d2-106">SmartGroupById</span><span class="sxs-lookup"><span data-stu-id="007d2-106">SmartGroupById</span></span>
```
Get-AzSmartGroup -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="007d2-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="007d2-107">DESCRIPTION</span></span>
<span data-ttu-id="007d2-108">O cmdlet **Get-AzSmartGroup** obtém informações de grupos inteligentes.</span><span class="sxs-lookup"><span data-stu-id="007d2-108">**Get-AzSmartGroup** cmdlet gets smart groups information.</span></span>

## <span data-ttu-id="007d2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="007d2-109">EXAMPLES</span></span>

### <span data-ttu-id="007d2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="007d2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroup -TimeRange "1h"
```

<span data-ttu-id="007d2-111">Listar todos os grupos inteligentes formados na última 1 hora.</span><span class="sxs-lookup"><span data-stu-id="007d2-111">List all smart groups formed in last 1 hour.</span></span> <span data-ttu-id="007d2-112">Use Format-List para obter os detalhes completos de cada grupo inteligente na lista.</span><span class="sxs-lookup"><span data-stu-id="007d2-112">Use Format-List to get the complete details of each smart group in list.</span></span>

### <span data-ttu-id="007d2-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="007d2-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSmartGroup -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="007d2-114">Obter detalhes do Grupo Inteligente por ID (GUID) ou ID de Recurso (Complete ARM Id)</span><span class="sxs-lookup"><span data-stu-id="007d2-114">Get Smart Group details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="007d2-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="007d2-115">PARAMETERS</span></span>

### <span data-ttu-id="007d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="007d2-116">-DefaultProfile</span></span>
<span data-ttu-id="007d2-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="007d2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="007d2-118">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="007d2-118">-SmartGroupId</span></span>
<span data-ttu-id="007d2-119">Identificador exclusivo do SmartGroup/ResourceId do SmartGroup.</span><span class="sxs-lookup"><span data-stu-id="007d2-119">Unique Identifier of SmartGroup / ResourceId of SmartGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="007d2-120">-SortBy</span><span class="sxs-lookup"><span data-stu-id="007d2-120">-SortBy</span></span>
<span data-ttu-id="007d2-121">Propriedade Alert a ser usada durante a classificação</span><span class="sxs-lookup"><span data-stu-id="007d2-121">Alert property to use while sorting</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="007d2-122">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="007d2-122">-SortOrder</span></span>
<span data-ttu-id="007d2-123">Ordem de Classificação</span><span class="sxs-lookup"><span data-stu-id="007d2-123">Sort Order</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="007d2-124">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="007d2-124">-TimeRange</span></span>
<span data-ttu-id="007d2-125">Valores de intervalo de tempo suportados - 1h, 1d, 7d, 30d (Padrão é 1d)</span><span class="sxs-lookup"><span data-stu-id="007d2-125">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="007d2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="007d2-126">CommonParameters</span></span>
<span data-ttu-id="007d2-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="007d2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="007d2-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="007d2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="007d2-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="007d2-129">INPUTS</span></span>

### <span data-ttu-id="007d2-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="007d2-130">None</span></span>

## <span data-ttu-id="007d2-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="007d2-131">OUTPUTS</span></span>

### <span data-ttu-id="007d2-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="007d2-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="007d2-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="007d2-133">NOTES</span></span>

## <span data-ttu-id="007d2-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="007d2-134">RELATED LINKS</span></span>
