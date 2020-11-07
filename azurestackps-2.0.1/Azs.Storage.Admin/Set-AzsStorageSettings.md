---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 0b06ef857a7c035b7069b7a8b33db2d1763091e2
ms.sourcegitcommit: 5523170e571fbd1dc93bd0fa4223aba3b324d3b0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/25/2020
ms.locfileid: "93945389"
---
# <span data-ttu-id="88251-101">Set-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="88251-101">Set-AzsStorageSettings</span></span>

## <span data-ttu-id="88251-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88251-102">SYNOPSIS</span></span>


## <span data-ttu-id="88251-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88251-103">SYNTAX</span></span>

```
Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays <Int32> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Force] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="88251-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88251-104">DESCRIPTION</span></span>


## <span data-ttu-id="88251-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88251-105">EXAMPLES</span></span>

### <span data-ttu-id="88251-106">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="88251-106">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays 1
```

<span data-ttu-id="88251-107">Atualize as configurações de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="88251-107">Update the storage settings.</span></span>

## <span data-ttu-id="88251-108">OS</span><span class="sxs-lookup"><span data-stu-id="88251-108">PARAMETERS</span></span>

### <span data-ttu-id="88251-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88251-109">-DefaultProfile</span></span>


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

### <span data-ttu-id="88251-110">-Force</span><span class="sxs-lookup"><span data-stu-id="88251-110">-Force</span></span>


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

### <span data-ttu-id="88251-111">-Local</span><span class="sxs-lookup"><span data-stu-id="88251-111">-Location</span></span>


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

### <span data-ttu-id="88251-112">-RetentionPeriodForDeletedStorageAccountsInDays</span><span class="sxs-lookup"><span data-stu-id="88251-112">-RetentionPeriodForDeletedStorageAccountsInDays</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="88251-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="88251-113">-SubscriptionId</span></span>


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

### <span data-ttu-id="88251-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="88251-114">-Confirm</span></span>
<span data-ttu-id="88251-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88251-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88251-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88251-116">-WhatIf</span></span>
<span data-ttu-id="88251-117">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="88251-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88251-118">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="88251-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88251-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88251-119">CommonParameters</span></span>
<span data-ttu-id="88251-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88251-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88251-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88251-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88251-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88251-122">INPUTS</span></span>

## <span data-ttu-id="88251-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88251-123">OUTPUTS</span></span>

### <span data-ttu-id="88251-124">Microsoft. Azure. PowerShell. cmdlets. StorageAdmin. Models. Api201908Preview. ISettings</span><span class="sxs-lookup"><span data-stu-id="88251-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="88251-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88251-125">NOTES</span></span>

## <span data-ttu-id="88251-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88251-126">RELATED LINKS</span></span>

