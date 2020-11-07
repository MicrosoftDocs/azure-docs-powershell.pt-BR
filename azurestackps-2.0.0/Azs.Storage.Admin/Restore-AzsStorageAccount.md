---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/restore-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 81b6a6dc960e9364d6d3e54f6e6394e17559b7f8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777131"
---
# <span data-ttu-id="d716d-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d716d-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="d716d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d716d-102">SYNOPSIS</span></span>


## <span data-ttu-id="d716d-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d716d-103">SYNTAX</span></span>

```
Restore-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-NewAccountName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d716d-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d716d-104">DESCRIPTION</span></span>


## <span data-ttu-id="d716d-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d716d-105">EXAMPLES</span></span>

### <span data-ttu-id="d716d-106">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="d716d-106">Example 1:</span></span>
```powershell
PS C:\> Restore-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 
```

<span data-ttu-id="d716d-107">Desexcluir uma conta de armazenamento excluída.</span><span class="sxs-lookup"><span data-stu-id="d716d-107">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="d716d-108">OS</span><span class="sxs-lookup"><span data-stu-id="d716d-108">PARAMETERS</span></span>

### <span data-ttu-id="d716d-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d716d-109">-AsJob</span></span>


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

### <span data-ttu-id="d716d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d716d-110">-DefaultProfile</span></span>


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

### <span data-ttu-id="d716d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d716d-111">-Force</span></span>


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

### <span data-ttu-id="d716d-112">-Local</span><span class="sxs-lookup"><span data-stu-id="d716d-112">-Location</span></span>


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

### <span data-ttu-id="d716d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d716d-113">-Name</span></span>


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

### <span data-ttu-id="d716d-114">-NewAccountName</span><span class="sxs-lookup"><span data-stu-id="d716d-114">-NewAccountName</span></span>


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

### <span data-ttu-id="d716d-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d716d-115">-NoWait</span></span>


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

### <span data-ttu-id="d716d-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d716d-116">-PassThru</span></span>


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

### <span data-ttu-id="d716d-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d716d-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="d716d-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d716d-118">-Confirm</span></span>
<span data-ttu-id="d716d-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d716d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d716d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d716d-120">-WhatIf</span></span>
<span data-ttu-id="d716d-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d716d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d716d-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d716d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d716d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d716d-123">CommonParameters</span></span>
<span data-ttu-id="d716d-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d716d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d716d-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d716d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d716d-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d716d-126">INPUTS</span></span>

## <span data-ttu-id="d716d-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d716d-127">OUTPUTS</span></span>

### <span data-ttu-id="d716d-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d716d-128">System.Boolean</span></span>



## <span data-ttu-id="d716d-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d716d-129">NOTES</span></span>

## <span data-ttu-id="d716d-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d716d-130">RELATED LINKS</span></span>

