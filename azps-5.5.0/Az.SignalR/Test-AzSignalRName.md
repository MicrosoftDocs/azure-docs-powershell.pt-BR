---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: b00a408df2fe1705309152a02484d3b18ea41e9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116377"
---
# <span data-ttu-id="925f5-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="925f5-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="925f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="925f5-102">SYNOPSIS</span></span>
<span data-ttu-id="925f5-103">Verifique a disponibilidade de um nome.</span><span class="sxs-lookup"><span data-stu-id="925f5-103">Check the availability of a name.</span></span> <span data-ttu-id="925f5-104">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="925f5-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="925f5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="925f5-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="925f5-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="925f5-106">DESCRIPTION</span></span>
<span data-ttu-id="925f5-107">Verifique a disponibilidade de um nome.</span><span class="sxs-lookup"><span data-stu-id="925f5-107">Check the availability of a name.</span></span> <span data-ttu-id="925f5-108">Alias: Teste-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="925f5-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="925f5-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="925f5-109">EXAMPLES</span></span>

### <span data-ttu-id="925f5-110">Verifique um nome existente.</span><span class="sxs-lookup"><span data-stu-id="925f5-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="925f5-111">Verifique um nome nãoexistido.</span><span class="sxs-lookup"><span data-stu-id="925f5-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="925f5-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="925f5-112">PARAMETERS</span></span>

### <span data-ttu-id="925f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="925f5-113">-DefaultProfile</span></span>
<span data-ttu-id="925f5-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="925f5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="925f5-115">-Local</span><span class="sxs-lookup"><span data-stu-id="925f5-115">-Location</span></span>
<span data-ttu-id="925f5-116">O local de serviço de Sinalização.</span><span class="sxs-lookup"><span data-stu-id="925f5-116">The SignalR service location.</span></span>

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

### <span data-ttu-id="925f5-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="925f5-117">-Name</span></span>
<span data-ttu-id="925f5-118">O nome do serviço de Sinalização.</span><span class="sxs-lookup"><span data-stu-id="925f5-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="925f5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="925f5-119">CommonParameters</span></span>
<span data-ttu-id="925f5-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="925f5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="925f5-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="925f5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="925f5-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="925f5-122">INPUTS</span></span>

### <span data-ttu-id="925f5-123">System.String</span><span class="sxs-lookup"><span data-stu-id="925f5-123">System.String</span></span>

## <span data-ttu-id="925f5-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="925f5-124">OUTPUTS</span></span>

### <span data-ttu-id="925f5-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="925f5-125">System.Boolean</span></span>

## <span data-ttu-id="925f5-126">Notas</span><span class="sxs-lookup"><span data-stu-id="925f5-126">NOTES</span></span>

## <span data-ttu-id="925f5-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="925f5-127">RELATED LINKS</span></span>
