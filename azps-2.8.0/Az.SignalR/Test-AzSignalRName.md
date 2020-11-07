---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: 21fbee422b898b5e5cf448f4a8f1913777268964
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772402"
---
# <span data-ttu-id="28a9d-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="28a9d-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="28a9d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28a9d-102">SYNOPSIS</span></span>
<span data-ttu-id="28a9d-103">Verifique a disponibilidade de um nome.</span><span class="sxs-lookup"><span data-stu-id="28a9d-103">Check the availability of a name.</span></span> <span data-ttu-id="28a9d-104">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="28a9d-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="28a9d-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28a9d-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="28a9d-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="28a9d-106">DESCRIPTION</span></span>
<span data-ttu-id="28a9d-107">Verifique a disponibilidade de um nome.</span><span class="sxs-lookup"><span data-stu-id="28a9d-107">Check the availability of a name.</span></span> <span data-ttu-id="28a9d-108">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="28a9d-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="28a9d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28a9d-109">EXAMPLES</span></span>

### <span data-ttu-id="28a9d-110">Verifique um nome existente.</span><span class="sxs-lookup"><span data-stu-id="28a9d-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="28a9d-111">Verifique um nome inexistente.</span><span class="sxs-lookup"><span data-stu-id="28a9d-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="28a9d-112">OS</span><span class="sxs-lookup"><span data-stu-id="28a9d-112">PARAMETERS</span></span>

### <span data-ttu-id="28a9d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a9d-113">-DefaultProfile</span></span>
<span data-ttu-id="28a9d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28a9d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28a9d-115">-Local</span><span class="sxs-lookup"><span data-stu-id="28a9d-115">-Location</span></span>
<span data-ttu-id="28a9d-116">O local do serviço de sinal de sinal.</span><span class="sxs-lookup"><span data-stu-id="28a9d-116">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a9d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="28a9d-117">-Name</span></span>
<span data-ttu-id="28a9d-118">O nome do serviço do Signalr.</span><span class="sxs-lookup"><span data-stu-id="28a9d-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="28a9d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a9d-119">CommonParameters</span></span>
<span data-ttu-id="28a9d-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28a9d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28a9d-121">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28a9d-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a9d-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="28a9d-122">INPUTS</span></span>

### <span data-ttu-id="28a9d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="28a9d-123">System.String</span></span>

## <span data-ttu-id="28a9d-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="28a9d-124">OUTPUTS</span></span>

### <span data-ttu-id="28a9d-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="28a9d-125">System.Boolean</span></span>

## <span data-ttu-id="28a9d-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="28a9d-126">NOTES</span></span>

## <span data-ttu-id="28a9d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28a9d-127">RELATED LINKS</span></span>
