---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
ms.openlocfilehash: b3bb193b47acf0f77851e5b9f4549d455a568b15
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116287"
---
# <span data-ttu-id="4b788-101">Get-AzSmartGroup</span><span class="sxs-lookup"><span data-stu-id="4b788-101">Get-AzSmartGroup</span></span>

## <span data-ttu-id="4b788-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b788-102">SYNOPSIS</span></span>
<span data-ttu-id="4b788-103">Obtém informações sobre grupos inteligentes</span><span class="sxs-lookup"><span data-stu-id="4b788-103">Gets Smart Groups information</span></span>

## <span data-ttu-id="4b788-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b788-104">SYNTAX</span></span>

### <span data-ttu-id="4b788-105">SmartGroupsListByFilter (padrão)</span><span class="sxs-lookup"><span data-stu-id="4b788-105">SmartGroupsListByFilter (Default)</span></span>
```
Get-AzSmartGroup [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b788-106">SmartGroupById</span><span class="sxs-lookup"><span data-stu-id="4b788-106">SmartGroupById</span></span>
```
Get-AzSmartGroup -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b788-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b788-107">DESCRIPTION</span></span>
<span data-ttu-id="4b788-108">O cmdlet **Get-AzSmartGroup** Obtém informações de grupos inteligentes.</span><span class="sxs-lookup"><span data-stu-id="4b788-108">**Get-AzSmartGroup** cmdlet gets smart groups information.</span></span>

## <span data-ttu-id="4b788-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b788-109">EXAMPLES</span></span>

### <span data-ttu-id="4b788-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4b788-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroup -TimeRange "1h"
```

<span data-ttu-id="4b788-111">Listar todos os grupos inteligentes formados na última vez em 1 hora.</span><span class="sxs-lookup"><span data-stu-id="4b788-111">List all smart groups formed in last 1 hour.</span></span> <span data-ttu-id="4b788-112">Use Format-List para obter os detalhes completos de cada grupo inteligente na lista.</span><span class="sxs-lookup"><span data-stu-id="4b788-112">Use Format-List to get the complete details of each smart group in list.</span></span>

### <span data-ttu-id="4b788-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4b788-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSmartGroup -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="4b788-114">Obter detalhes do grupo inteligente por ID (GUID) ou ID do recurso (ID do braço completo)</span><span class="sxs-lookup"><span data-stu-id="4b788-114">Get Smart Group details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="4b788-115">OS</span><span class="sxs-lookup"><span data-stu-id="4b788-115">PARAMETERS</span></span>

### <span data-ttu-id="4b788-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b788-116">-DefaultProfile</span></span>
<span data-ttu-id="4b788-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b788-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b788-118">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="4b788-118">-SmartGroupId</span></span>
<span data-ttu-id="4b788-119">Identificador exclusivo do SmartMode/resourceer do Smart.</span><span class="sxs-lookup"><span data-stu-id="4b788-119">Unique Identifier of SmartGroup / ResourceId of SmartGroup.</span></span>

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

### <span data-ttu-id="4b788-120">-ClassificarPor</span><span class="sxs-lookup"><span data-stu-id="4b788-120">-SortBy</span></span>
<span data-ttu-id="4b788-121">Propriedade de alerta a ser usada durante a classificação</span><span class="sxs-lookup"><span data-stu-id="4b788-121">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="4b788-122">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="4b788-122">-SortOrder</span></span>
<span data-ttu-id="4b788-123">Ordem de classificação</span><span class="sxs-lookup"><span data-stu-id="4b788-123">Sort Order</span></span>

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

### <span data-ttu-id="4b788-124">-Intervalo de</span><span class="sxs-lookup"><span data-stu-id="4b788-124">-TimeRange</span></span>
<span data-ttu-id="4b788-125">Valores de intervalo de tempo com suporte-1h, 1D, 7D, 30D (o padrão é 1d)</span><span class="sxs-lookup"><span data-stu-id="4b788-125">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="4b788-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b788-126">CommonParameters</span></span>
<span data-ttu-id="4b788-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b788-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b788-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b788-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b788-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b788-129">INPUTS</span></span>

### <span data-ttu-id="4b788-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4b788-130">None</span></span>

## <span data-ttu-id="4b788-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b788-131">OUTPUTS</span></span>

### <span data-ttu-id="4b788-132">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="4b788-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="4b788-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b788-133">NOTES</span></span>

## <span data-ttu-id="4b788-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b788-134">RELATED LINKS</span></span>
