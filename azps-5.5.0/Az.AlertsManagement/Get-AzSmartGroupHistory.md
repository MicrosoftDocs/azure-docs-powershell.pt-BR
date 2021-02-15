---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: a8e827d678c7ac3b917ee7be09d030b193ffda24
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114868"
---
# <span data-ttu-id="fa982-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="fa982-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="fa982-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa982-102">SYNOPSIS</span></span>
<span data-ttu-id="fa982-103">Obtém histórico de grupos inteligentes</span><span class="sxs-lookup"><span data-stu-id="fa982-103">Gets smart group history</span></span>

## <span data-ttu-id="fa982-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa982-104">SYNTAX</span></span>

### <span data-ttu-id="fa982-105">BySmartGroupId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fa982-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa982-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fa982-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa982-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa982-107">DESCRIPTION</span></span>
<span data-ttu-id="fa982-108">**O cmdlet Get-AzSmartGroupHistory** obtém o histórico de grupos inteligentes.</span><span class="sxs-lookup"><span data-stu-id="fa982-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="fa982-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fa982-109">EXAMPLES</span></span>

### <span data-ttu-id="fa982-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fa982-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="fa982-111">Obtém detalhes do histórico de grupos inteligentes.</span><span class="sxs-lookup"><span data-stu-id="fa982-111">Gets smart group history details.</span></span>

## <span data-ttu-id="fa982-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa982-112">PARAMETERS</span></span>

### <span data-ttu-id="fa982-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa982-113">-DefaultProfile</span></span>
<span data-ttu-id="fa982-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fa982-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa982-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa982-115">-InputObject</span></span>
<span data-ttu-id="fa982-116">Objeto de entrada do pipeline.</span><span class="sxs-lookup"><span data-stu-id="fa982-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa982-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="fa982-117">-SmartGroupId</span></span>
<span data-ttu-id="fa982-118">Identificador exclusivo de alerta SmartGroup/ResourceId.</span><span class="sxs-lookup"><span data-stu-id="fa982-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa982-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa982-119">CommonParameters</span></span>
<span data-ttu-id="fa982-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa982-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa982-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa982-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa982-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="fa982-122">INPUTS</span></span>

### <span data-ttu-id="fa982-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fa982-123">None</span></span>

## <span data-ttu-id="fa982-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="fa982-124">OUTPUTS</span></span>

### <span data-ttu-id="fa982-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="fa982-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="fa982-126">Notas</span><span class="sxs-lookup"><span data-stu-id="fa982-126">NOTES</span></span>

## <span data-ttu-id="fa982-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa982-127">RELATED LINKS</span></span>
