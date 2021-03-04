---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: 31b72f68151132fc4dca1bddd18c1a15b6a36f3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886513"
---
# <span data-ttu-id="78142-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="78142-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="78142-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78142-102">SYNOPSIS</span></span>
<span data-ttu-id="78142-103">Obtém informações do Histórico de Alertas</span><span class="sxs-lookup"><span data-stu-id="78142-103">Gets Alert History information</span></span>

## <span data-ttu-id="78142-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="78142-104">SYNTAX</span></span>

### <span data-ttu-id="78142-105">ByAlertId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="78142-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78142-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="78142-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78142-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="78142-107">DESCRIPTION</span></span>
<span data-ttu-id="78142-108">O cmdlet **Get-AzAlertObjectHistory** obtém histórico de alerta.</span><span class="sxs-lookup"><span data-stu-id="78142-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="78142-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78142-109">EXAMPLES</span></span>

### <span data-ttu-id="78142-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="78142-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="78142-111">Obtém detalhes do histórico de alertas.</span><span class="sxs-lookup"><span data-stu-id="78142-111">Gets alert history details.</span></span> 

## <span data-ttu-id="78142-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="78142-112">PARAMETERS</span></span>

### <span data-ttu-id="78142-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="78142-113">-AlertId</span></span>
<span data-ttu-id="78142-114">Identificador exclusivo de Alerta/ResourceId de alerta.</span><span class="sxs-lookup"><span data-stu-id="78142-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78142-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78142-115">-DefaultProfile</span></span>
<span data-ttu-id="78142-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78142-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78142-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78142-117">-InputObject</span></span>
<span data-ttu-id="78142-118">Objeto input do pipeline.</span><span class="sxs-lookup"><span data-stu-id="78142-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="78142-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78142-119">CommonParameters</span></span>
<span data-ttu-id="78142-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78142-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78142-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78142-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78142-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78142-122">INPUTS</span></span>

### <span data-ttu-id="78142-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="78142-123">None</span></span>

## <span data-ttu-id="78142-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="78142-124">OUTPUTS</span></span>

### <span data-ttu-id="78142-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="78142-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="78142-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="78142-126">NOTES</span></span>

## <span data-ttu-id="78142-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78142-127">RELATED LINKS</span></span>
