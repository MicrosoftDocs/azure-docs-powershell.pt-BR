---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: b00a408df2fe1705309152a02484d3b18ea41e9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94283739"
---
# <span data-ttu-id="bc6d8-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="bc6d8-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="bc6d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc6d8-102">SYNOPSIS</span></span>
<span data-ttu-id="bc6d8-103">Verifique a disponibilidade de um nome.</span><span class="sxs-lookup"><span data-stu-id="bc6d8-103">Check the availability of a name.</span></span> <span data-ttu-id="bc6d8-104">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="bc6d8-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="bc6d8-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc6d8-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc6d8-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc6d8-106">DESCRIPTION</span></span>
<span data-ttu-id="bc6d8-107">Verifique a disponibilidade de um nome.</span><span class="sxs-lookup"><span data-stu-id="bc6d8-107">Check the availability of a name.</span></span> <span data-ttu-id="bc6d8-108">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="bc6d8-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="bc6d8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc6d8-109">EXAMPLES</span></span>

### <span data-ttu-id="bc6d8-110">Verifique um nome existente.</span><span class="sxs-lookup"><span data-stu-id="bc6d8-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="bc6d8-111">Verifique um nome inexistente.</span><span class="sxs-lookup"><span data-stu-id="bc6d8-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="bc6d8-112">OS</span><span class="sxs-lookup"><span data-stu-id="bc6d8-112">PARAMETERS</span></span>

### <span data-ttu-id="bc6d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc6d8-113">-DefaultProfile</span></span>
<span data-ttu-id="bc6d8-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc6d8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc6d8-115">-Local</span><span class="sxs-lookup"><span data-stu-id="bc6d8-115">-Location</span></span>
<span data-ttu-id="bc6d8-116">O local do serviço de sinal de sinal.</span><span class="sxs-lookup"><span data-stu-id="bc6d8-116">The SignalR service location.</span></span>

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

### <span data-ttu-id="bc6d8-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc6d8-117">-Name</span></span>
<span data-ttu-id="bc6d8-118">O nome do serviço do Signalr.</span><span class="sxs-lookup"><span data-stu-id="bc6d8-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="bc6d8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc6d8-119">CommonParameters</span></span>
<span data-ttu-id="bc6d8-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc6d8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc6d8-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc6d8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc6d8-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc6d8-122">INPUTS</span></span>

### <span data-ttu-id="bc6d8-123">System. String</span><span class="sxs-lookup"><span data-stu-id="bc6d8-123">System.String</span></span>

## <span data-ttu-id="bc6d8-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc6d8-124">OUTPUTS</span></span>

### <span data-ttu-id="bc6d8-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bc6d8-125">System.Boolean</span></span>

## <span data-ttu-id="bc6d8-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc6d8-126">NOTES</span></span>

## <span data-ttu-id="bc6d8-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc6d8-127">RELATED LINKS</span></span>
