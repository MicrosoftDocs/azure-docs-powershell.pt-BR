---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: a8e827d678c7ac3b917ee7be09d030b193ffda24
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261256"
---
# <span data-ttu-id="9b06a-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="9b06a-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="9b06a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b06a-102">SYNOPSIS</span></span>
<span data-ttu-id="9b06a-103">Obtém histórico do grupo inteligente</span><span class="sxs-lookup"><span data-stu-id="9b06a-103">Gets smart group history</span></span>

## <span data-ttu-id="9b06a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b06a-104">SYNTAX</span></span>

### <span data-ttu-id="9b06a-105">BySmartGroupId (padrão)</span><span class="sxs-lookup"><span data-stu-id="9b06a-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b06a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9b06a-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b06a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b06a-107">DESCRIPTION</span></span>
<span data-ttu-id="9b06a-108">O cmdlet **Get-AzSmartGroupHistory** Obtém o histórico do grupo inteligente.</span><span class="sxs-lookup"><span data-stu-id="9b06a-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="9b06a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b06a-109">EXAMPLES</span></span>

### <span data-ttu-id="9b06a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9b06a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="9b06a-111">Obtém detalhes do histórico do grupo inteligente.</span><span class="sxs-lookup"><span data-stu-id="9b06a-111">Gets smart group history details.</span></span>

## <span data-ttu-id="9b06a-112">OS</span><span class="sxs-lookup"><span data-stu-id="9b06a-112">PARAMETERS</span></span>

### <span data-ttu-id="9b06a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b06a-113">-DefaultProfile</span></span>
<span data-ttu-id="9b06a-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b06a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b06a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b06a-115">-InputObject</span></span>
<span data-ttu-id="9b06a-116">Objeto de entrada do pipeline.</span><span class="sxs-lookup"><span data-stu-id="9b06a-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="9b06a-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="9b06a-117">-SmartGroupId</span></span>
<span data-ttu-id="9b06a-118">Identificador exclusivo do SmartMode/ResourceId do alerta.</span><span class="sxs-lookup"><span data-stu-id="9b06a-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

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

### <span data-ttu-id="9b06a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b06a-119">CommonParameters</span></span>
<span data-ttu-id="9b06a-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b06a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b06a-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b06a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b06a-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b06a-122">INPUTS</span></span>

### <span data-ttu-id="9b06a-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9b06a-123">None</span></span>

## <span data-ttu-id="9b06a-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b06a-124">OUTPUTS</span></span>

### <span data-ttu-id="9b06a-125">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="9b06a-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="9b06a-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b06a-126">NOTES</span></span>

## <span data-ttu-id="9b06a-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b06a-127">RELATED LINKS</span></span>
