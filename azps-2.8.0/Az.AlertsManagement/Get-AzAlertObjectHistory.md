---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: 8c0df920b8619760cf4a80d9ef6502e82de9a31f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598188"
---
# <span data-ttu-id="d3e59-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="d3e59-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="d3e59-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3e59-102">SYNOPSIS</span></span>
<span data-ttu-id="d3e59-103">Obtém informações do histórico de alertas</span><span class="sxs-lookup"><span data-stu-id="d3e59-103">Gets Alert History information</span></span>

## <span data-ttu-id="d3e59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3e59-104">SYNTAX</span></span>

### <span data-ttu-id="d3e59-105">ByAlertId (padrão)</span><span class="sxs-lookup"><span data-stu-id="d3e59-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3e59-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d3e59-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3e59-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3e59-107">DESCRIPTION</span></span>
<span data-ttu-id="d3e59-108">O cmdlet **Get-AzAlertObjectHistory** tem histórico de alerta.</span><span class="sxs-lookup"><span data-stu-id="d3e59-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="d3e59-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3e59-109">EXAMPLES</span></span>

### <span data-ttu-id="d3e59-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d3e59-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="d3e59-111">Obtém detalhes do histórico de alertas.</span><span class="sxs-lookup"><span data-stu-id="d3e59-111">Gets alert history details.</span></span> 

## <span data-ttu-id="d3e59-112">OS</span><span class="sxs-lookup"><span data-stu-id="d3e59-112">PARAMETERS</span></span>

### <span data-ttu-id="d3e59-113">-Alertid</span><span class="sxs-lookup"><span data-stu-id="d3e59-113">-AlertId</span></span>
<span data-ttu-id="d3e59-114">Identificador exclusivo do alerta/ResourceId do alerta.</span><span class="sxs-lookup"><span data-stu-id="d3e59-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="d3e59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3e59-115">-DefaultProfile</span></span>
<span data-ttu-id="d3e59-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3e59-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3e59-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3e59-117">-InputObject</span></span>
<span data-ttu-id="d3e59-118">Objeto de entrada do pipeline.</span><span class="sxs-lookup"><span data-stu-id="d3e59-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="d3e59-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3e59-119">CommonParameters</span></span>
<span data-ttu-id="d3e59-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3e59-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3e59-121">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3e59-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3e59-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3e59-122">INPUTS</span></span>

### <span data-ttu-id="d3e59-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d3e59-123">None</span></span>

## <span data-ttu-id="d3e59-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3e59-124">OUTPUTS</span></span>

### <span data-ttu-id="d3e59-125">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="d3e59-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="d3e59-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3e59-126">NOTES</span></span>

## <span data-ttu-id="d3e59-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3e59-127">RELATED LINKS</span></span>
