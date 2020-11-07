---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947586"
---
# <span data-ttu-id="b0d3f-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="b0d3f-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="b0d3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0d3f-102">SYNOPSIS</span></span>
<span data-ttu-id="b0d3f-103">Obter a cota de uso de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="b0d3f-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="b0d3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0d3f-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0d3f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0d3f-105">DESCRIPTION</span></span>
<span data-ttu-id="b0d3f-106">Obter a cota de uso de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="b0d3f-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="b0d3f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0d3f-107">EXAMPLES</span></span>

### <span data-ttu-id="b0d3f-108">Obter a cota de uso ao inserir o local</span><span class="sxs-lookup"><span data-stu-id="b0d3f-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="b0d3f-109">OS</span><span class="sxs-lookup"><span data-stu-id="b0d3f-109">PARAMETERS</span></span>

### <span data-ttu-id="b0d3f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d3f-110">-DefaultProfile</span></span>
<span data-ttu-id="b0d3f-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0d3f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0d3f-112">-Local</span><span class="sxs-lookup"><span data-stu-id="b0d3f-112">-Location</span></span>
<span data-ttu-id="b0d3f-113">O local do serviço de sinal de sinal.</span><span class="sxs-lookup"><span data-stu-id="b0d3f-113">The SignalR service location.</span></span>

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

### <span data-ttu-id="b0d3f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d3f-114">CommonParameters</span></span>
<span data-ttu-id="b0d3f-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0d3f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d3f-116">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0d3f-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d3f-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0d3f-117">INPUTS</span></span>

### <span data-ttu-id="b0d3f-118">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b0d3f-118">None</span></span>

## <span data-ttu-id="b0d3f-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0d3f-119">OUTPUTS</span></span>

### <span data-ttu-id="b0d3f-120">Microsoft. Azure. Commands. Signalr. Models. PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="b0d3f-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="b0d3f-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0d3f-121">NOTES</span></span>

## <span data-ttu-id="b0d3f-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0d3f-122">RELATED LINKS</span></span>
