---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: bf2062ab320c02bbb3f29c038161ddcb4342675f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259958"
---
# <span data-ttu-id="40aa7-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="40aa7-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="40aa7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40aa7-102">SYNOPSIS</span></span>
<span data-ttu-id="40aa7-103">Obtém informações do histórico de alertas</span><span class="sxs-lookup"><span data-stu-id="40aa7-103">Gets Alert History information</span></span>

## <span data-ttu-id="40aa7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40aa7-104">SYNTAX</span></span>

### <span data-ttu-id="40aa7-105">ByAlertId (padrão)</span><span class="sxs-lookup"><span data-stu-id="40aa7-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40aa7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="40aa7-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40aa7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40aa7-107">DESCRIPTION</span></span>
<span data-ttu-id="40aa7-108">O cmdlet **Get-AzAlertObjectHistory** tem histórico de alerta.</span><span class="sxs-lookup"><span data-stu-id="40aa7-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="40aa7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40aa7-109">EXAMPLES</span></span>

### <span data-ttu-id="40aa7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="40aa7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="40aa7-111">Obtém detalhes do histórico de alertas.</span><span class="sxs-lookup"><span data-stu-id="40aa7-111">Gets alert history details.</span></span> 

## <span data-ttu-id="40aa7-112">OS</span><span class="sxs-lookup"><span data-stu-id="40aa7-112">PARAMETERS</span></span>

### <span data-ttu-id="40aa7-113">-Alertid</span><span class="sxs-lookup"><span data-stu-id="40aa7-113">-AlertId</span></span>
<span data-ttu-id="40aa7-114">Identificador exclusivo do alerta/ResourceId do alerta.</span><span class="sxs-lookup"><span data-stu-id="40aa7-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="40aa7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40aa7-115">-DefaultProfile</span></span>
<span data-ttu-id="40aa7-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40aa7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40aa7-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40aa7-117">-InputObject</span></span>
<span data-ttu-id="40aa7-118">Objeto de entrada do pipeline.</span><span class="sxs-lookup"><span data-stu-id="40aa7-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="40aa7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40aa7-119">CommonParameters</span></span>
<span data-ttu-id="40aa7-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40aa7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40aa7-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40aa7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40aa7-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40aa7-122">INPUTS</span></span>

### <span data-ttu-id="40aa7-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="40aa7-123">None</span></span>

## <span data-ttu-id="40aa7-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40aa7-124">OUTPUTS</span></span>

### <span data-ttu-id="40aa7-125">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="40aa7-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="40aa7-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40aa7-126">NOTES</span></span>

## <span data-ttu-id="40aa7-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40aa7-127">RELATED LINKS</span></span>
