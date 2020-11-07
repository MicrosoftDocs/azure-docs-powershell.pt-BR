---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/start-azsreclaimstoragecapacity
schema: 2.0.0
ms.openlocfilehash: bb2eecb93a7a18559dc6fbe58cd5f07c737e16b5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945155"
---
# <span data-ttu-id="2307e-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="2307e-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="2307e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2307e-102">SYNOPSIS</span></span>


## <span data-ttu-id="2307e-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2307e-103">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2307e-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2307e-104">DESCRIPTION</span></span>


## <span data-ttu-id="2307e-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2307e-105">EXAMPLES</span></span>

### <span data-ttu-id="2307e-106">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="2307e-106">Example 1:</span></span>
```powershell
PS C:\> Start-AzsReclaimStorageCapacity
```

<span data-ttu-id="2307e-107">Iniciar a coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="2307e-107">Start garbage collection.</span></span>

## <span data-ttu-id="2307e-108">OS</span><span class="sxs-lookup"><span data-stu-id="2307e-108">PARAMETERS</span></span>

### <span data-ttu-id="2307e-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2307e-109">-AsJob</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2307e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2307e-110">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2307e-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2307e-111">-Force</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2307e-112">-Local</span><span class="sxs-lookup"><span data-stu-id="2307e-112">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2307e-113">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2307e-113">-NoWait</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2307e-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2307e-114">-PassThru</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2307e-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2307e-115">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2307e-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2307e-116">-Confirm</span></span>
<span data-ttu-id="2307e-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2307e-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2307e-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2307e-118">-WhatIf</span></span>
<span data-ttu-id="2307e-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2307e-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2307e-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2307e-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2307e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2307e-121">CommonParameters</span></span>
<span data-ttu-id="2307e-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2307e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2307e-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2307e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2307e-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2307e-124">INPUTS</span></span>

## <span data-ttu-id="2307e-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2307e-125">OUTPUTS</span></span>

### <span data-ttu-id="2307e-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2307e-126">System.Boolean</span></span>



## <span data-ttu-id="2307e-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2307e-127">NOTES</span></span>

## <span data-ttu-id="2307e-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2307e-128">RELATED LINKS</span></span>

