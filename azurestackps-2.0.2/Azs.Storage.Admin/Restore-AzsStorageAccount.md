---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/restore-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 81b6a6dc960e9364d6d3e54f6e6394e17559b7f8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93947009"
---
# <span data-ttu-id="320eb-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="320eb-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="320eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="320eb-102">SYNOPSIS</span></span>


## <span data-ttu-id="320eb-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="320eb-103">SYNTAX</span></span>

```
Restore-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-NewAccountName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="320eb-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="320eb-104">DESCRIPTION</span></span>


## <span data-ttu-id="320eb-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="320eb-105">EXAMPLES</span></span>

### <span data-ttu-id="320eb-106">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="320eb-106">Example 1:</span></span>
```powershell
PS C:\> Restore-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 
```

<span data-ttu-id="320eb-107">Desexcluir uma conta de armazenamento excluída.</span><span class="sxs-lookup"><span data-stu-id="320eb-107">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="320eb-108">OS</span><span class="sxs-lookup"><span data-stu-id="320eb-108">PARAMETERS</span></span>

### <span data-ttu-id="320eb-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="320eb-109">-AsJob</span></span>


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

### <span data-ttu-id="320eb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="320eb-110">-DefaultProfile</span></span>


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

### <span data-ttu-id="320eb-111">-Force</span><span class="sxs-lookup"><span data-stu-id="320eb-111">-Force</span></span>


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

### <span data-ttu-id="320eb-112">-Local</span><span class="sxs-lookup"><span data-stu-id="320eb-112">-Location</span></span>


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

### <span data-ttu-id="320eb-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="320eb-113">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="320eb-114">-NewAccountName</span><span class="sxs-lookup"><span data-stu-id="320eb-114">-NewAccountName</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="320eb-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="320eb-115">-NoWait</span></span>


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

### <span data-ttu-id="320eb-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="320eb-116">-PassThru</span></span>


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

### <span data-ttu-id="320eb-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="320eb-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="320eb-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="320eb-118">-Confirm</span></span>
<span data-ttu-id="320eb-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="320eb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="320eb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="320eb-120">-WhatIf</span></span>
<span data-ttu-id="320eb-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="320eb-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="320eb-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="320eb-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="320eb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="320eb-123">CommonParameters</span></span>
<span data-ttu-id="320eb-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="320eb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="320eb-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="320eb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="320eb-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="320eb-126">INPUTS</span></span>

## <span data-ttu-id="320eb-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="320eb-127">OUTPUTS</span></span>

### <span data-ttu-id="320eb-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="320eb-128">System.Boolean</span></span>



## <span data-ttu-id="320eb-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="320eb-129">NOTES</span></span>

## <span data-ttu-id="320eb-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="320eb-130">RELATED LINKS</span></span>

