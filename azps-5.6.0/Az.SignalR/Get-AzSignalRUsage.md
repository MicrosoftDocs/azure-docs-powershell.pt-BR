---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 16d528497532f026961941963049c61a470ad188
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885822"
---
# <span data-ttu-id="d7a5c-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="d7a5c-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="d7a5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7a5c-102">SYNOPSIS</span></span>
<span data-ttu-id="d7a5c-103">Obter a cota de uso de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="d7a5c-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="d7a5c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d7a5c-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7a5c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d7a5c-105">DESCRIPTION</span></span>
<span data-ttu-id="d7a5c-106">Obter a cota de uso de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="d7a5c-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="d7a5c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7a5c-107">EXAMPLES</span></span>

### <span data-ttu-id="d7a5c-108">Obter a cota de uso ao inserir o local</span><span class="sxs-lookup"><span data-stu-id="d7a5c-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="d7a5c-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d7a5c-109">PARAMETERS</span></span>

### <span data-ttu-id="d7a5c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7a5c-110">-DefaultProfile</span></span>
<span data-ttu-id="d7a5c-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7a5c-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7a5c-112">-Location</span><span class="sxs-lookup"><span data-stu-id="d7a5c-112">-Location</span></span>
<span data-ttu-id="d7a5c-113">O local do serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="d7a5c-113">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7a5c-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7a5c-114">CommonParameters</span></span>
<span data-ttu-id="d7a5c-115">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7a5c-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7a5c-116">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7a5c-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7a5c-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7a5c-117">INPUTS</span></span>

### <span data-ttu-id="d7a5c-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d7a5c-118">None</span></span>

## <span data-ttu-id="d7a5c-119">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d7a5c-119">OUTPUTS</span></span>

### <span data-ttu-id="d7a5c-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="d7a5c-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="d7a5c-121">NOTES</span><span class="sxs-lookup"><span data-stu-id="d7a5c-121">NOTES</span></span>

## <span data-ttu-id="d7a5c-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7a5c-122">RELATED LINKS</span></span>
