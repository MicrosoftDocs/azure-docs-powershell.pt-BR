---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
ms.openlocfilehash: b3bb193b47acf0f77851e5b9f4549d455a568b15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116666"
---
# <span data-ttu-id="9697b-101">Get-AzSmartGroup</span><span class="sxs-lookup"><span data-stu-id="9697b-101">Get-AzSmartGroup</span></span>

## <span data-ttu-id="9697b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9697b-102">SYNOPSIS</span></span>
<span data-ttu-id="9697b-103">Obtém informações sobre Grupos Inteligentes</span><span class="sxs-lookup"><span data-stu-id="9697b-103">Gets Smart Groups information</span></span>

## <span data-ttu-id="9697b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9697b-104">SYNTAX</span></span>

### <span data-ttu-id="9697b-105">SmartGroupsListByFilter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9697b-105">SmartGroupsListByFilter (Default)</span></span>
```
Get-AzSmartGroup [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9697b-106">SmartGroupById</span><span class="sxs-lookup"><span data-stu-id="9697b-106">SmartGroupById</span></span>
```
Get-AzSmartGroup -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9697b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9697b-107">DESCRIPTION</span></span>
<span data-ttu-id="9697b-108">**O cmdlet Get-AzSmartGroup** obtém informações sobre grupos inteligentes.</span><span class="sxs-lookup"><span data-stu-id="9697b-108">**Get-AzSmartGroup** cmdlet gets smart groups information.</span></span>

## <span data-ttu-id="9697b-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9697b-109">EXAMPLES</span></span>

### <span data-ttu-id="9697b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9697b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroup -TimeRange "1h"
```

<span data-ttu-id="9697b-111">Listar todos os grupos inteligentes formados na última 1 hora.</span><span class="sxs-lookup"><span data-stu-id="9697b-111">List all smart groups formed in last 1 hour.</span></span> <span data-ttu-id="9697b-112">Use Format-List para obter os detalhes completos de cada grupo inteligente na lista.</span><span class="sxs-lookup"><span data-stu-id="9697b-112">Use Format-List to get the complete details of each smart group in list.</span></span>

### <span data-ttu-id="9697b-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9697b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSmartGroup -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="9697b-114">Obter detalhes do Grupo Inteligente por ID (GUID) ou ID do Recurso (ID de ARM completa)</span><span class="sxs-lookup"><span data-stu-id="9697b-114">Get Smart Group details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="9697b-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9697b-115">PARAMETERS</span></span>

### <span data-ttu-id="9697b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9697b-116">-DefaultProfile</span></span>
<span data-ttu-id="9697b-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9697b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9697b-118">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="9697b-118">-SmartGroupId</span></span>
<span data-ttu-id="9697b-119">Identificador exclusivo do SmartGroup/ResourceId do SmartGroup.</span><span class="sxs-lookup"><span data-stu-id="9697b-119">Unique Identifier of SmartGroup / ResourceId of SmartGroup.</span></span>

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

### <span data-ttu-id="9697b-120">-SortBy</span><span class="sxs-lookup"><span data-stu-id="9697b-120">-SortBy</span></span>
<span data-ttu-id="9697b-121">Propriedade de alerta a ser usada durante a classificação</span><span class="sxs-lookup"><span data-stu-id="9697b-121">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="9697b-122">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="9697b-122">-SortOrder</span></span>
<span data-ttu-id="9697b-123">Ordem de Classificação</span><span class="sxs-lookup"><span data-stu-id="9697b-123">Sort Order</span></span>

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

### <span data-ttu-id="9697b-124">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="9697b-124">-TimeRange</span></span>
<span data-ttu-id="9697b-125">Valores de intervalo de tempo suportados - 1h, 1d, 7d, 30d (Padrão é 1d)</span><span class="sxs-lookup"><span data-stu-id="9697b-125">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="9697b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9697b-126">CommonParameters</span></span>
<span data-ttu-id="9697b-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9697b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9697b-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9697b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9697b-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="9697b-129">INPUTS</span></span>

### <span data-ttu-id="9697b-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9697b-130">None</span></span>

## <span data-ttu-id="9697b-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="9697b-131">OUTPUTS</span></span>

### <span data-ttu-id="9697b-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="9697b-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="9697b-133">Notas</span><span class="sxs-lookup"><span data-stu-id="9697b-133">NOTES</span></span>

## <span data-ttu-id="9697b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9697b-134">RELATED LINKS</span></span>
