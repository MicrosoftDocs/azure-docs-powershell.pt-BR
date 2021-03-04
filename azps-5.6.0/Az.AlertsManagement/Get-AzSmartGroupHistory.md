---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: 7a581d81938a647d845d2220b27347c1b42fcb03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886510"
---
# <span data-ttu-id="03bb5-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="03bb5-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="03bb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03bb5-102">SYNOPSIS</span></span>
<span data-ttu-id="03bb5-103">Obtém histórico de grupo inteligente</span><span class="sxs-lookup"><span data-stu-id="03bb5-103">Gets smart group history</span></span>

## <span data-ttu-id="03bb5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="03bb5-104">SYNTAX</span></span>

### <span data-ttu-id="03bb5-105">BySmartGroupId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="03bb5-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03bb5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="03bb5-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="03bb5-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="03bb5-107">DESCRIPTION</span></span>
<span data-ttu-id="03bb5-108">O cmdlet **Get-AzSmartGroupHistory** obtém o histórico de grupo inteligente.</span><span class="sxs-lookup"><span data-stu-id="03bb5-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="03bb5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03bb5-109">EXAMPLES</span></span>

### <span data-ttu-id="03bb5-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="03bb5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="03bb5-111">Obtém detalhes do histórico do grupo inteligente.</span><span class="sxs-lookup"><span data-stu-id="03bb5-111">Gets smart group history details.</span></span>

## <span data-ttu-id="03bb5-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="03bb5-112">PARAMETERS</span></span>

### <span data-ttu-id="03bb5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03bb5-113">-DefaultProfile</span></span>
<span data-ttu-id="03bb5-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="03bb5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03bb5-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03bb5-115">-InputObject</span></span>
<span data-ttu-id="03bb5-116">Objeto input do pipeline.</span><span class="sxs-lookup"><span data-stu-id="03bb5-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="03bb5-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="03bb5-117">-SmartGroupId</span></span>
<span data-ttu-id="03bb5-118">Identificador exclusivo do SmartGroup/ResourceId de alerta.</span><span class="sxs-lookup"><span data-stu-id="03bb5-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

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

### <span data-ttu-id="03bb5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03bb5-119">CommonParameters</span></span>
<span data-ttu-id="03bb5-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03bb5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03bb5-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03bb5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03bb5-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03bb5-122">INPUTS</span></span>

### <span data-ttu-id="03bb5-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="03bb5-123">None</span></span>

## <span data-ttu-id="03bb5-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="03bb5-124">OUTPUTS</span></span>

### <span data-ttu-id="03bb5-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="03bb5-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="03bb5-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="03bb5-126">NOTES</span></span>

## <span data-ttu-id="03bb5-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03bb5-127">RELATED LINKS</span></span>
