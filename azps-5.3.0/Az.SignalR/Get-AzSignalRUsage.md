---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428732"
---
# <span data-ttu-id="dde7b-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="dde7b-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="dde7b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dde7b-102">SYNOPSIS</span></span>
<span data-ttu-id="dde7b-103">Obter a cota de uso de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="dde7b-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="dde7b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dde7b-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dde7b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dde7b-105">DESCRIPTION</span></span>
<span data-ttu-id="dde7b-106">Obter a cota de uso de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="dde7b-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="dde7b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dde7b-107">EXAMPLES</span></span>

### <span data-ttu-id="dde7b-108">Obter a cota de uso ao inserir o local</span><span class="sxs-lookup"><span data-stu-id="dde7b-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="dde7b-109">OS</span><span class="sxs-lookup"><span data-stu-id="dde7b-109">PARAMETERS</span></span>

### <span data-ttu-id="dde7b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dde7b-110">-DefaultProfile</span></span>
<span data-ttu-id="dde7b-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dde7b-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dde7b-112">-Local</span><span class="sxs-lookup"><span data-stu-id="dde7b-112">-Location</span></span>
<span data-ttu-id="dde7b-113">O local do serviço de sinal de sinal.</span><span class="sxs-lookup"><span data-stu-id="dde7b-113">The SignalR service location.</span></span>

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

### <span data-ttu-id="dde7b-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dde7b-114">CommonParameters</span></span>
<span data-ttu-id="dde7b-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dde7b-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dde7b-116">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dde7b-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dde7b-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dde7b-117">INPUTS</span></span>

### <span data-ttu-id="dde7b-118">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="dde7b-118">None</span></span>

## <span data-ttu-id="dde7b-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dde7b-119">OUTPUTS</span></span>

### <span data-ttu-id="dde7b-120">Microsoft. Azure. Commands. Signalr. Models. PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="dde7b-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="dde7b-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dde7b-121">NOTES</span></span>

## <span data-ttu-id="dde7b-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dde7b-122">RELATED LINKS</span></span>
