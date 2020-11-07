---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 0b06ef857a7c035b7069b7a8b33db2d1763091e2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93947008"
---
# <span data-ttu-id="d72c0-101">Set-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="d72c0-101">Set-AzsStorageSettings</span></span>

## <span data-ttu-id="d72c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d72c0-102">SYNOPSIS</span></span>


## <span data-ttu-id="d72c0-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d72c0-103">SYNTAX</span></span>

```
Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays <Int32> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Force] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d72c0-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d72c0-104">DESCRIPTION</span></span>


## <span data-ttu-id="d72c0-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d72c0-105">EXAMPLES</span></span>

### <span data-ttu-id="d72c0-106">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="d72c0-106">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays 1
```

<span data-ttu-id="d72c0-107">Atualize as configurações de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d72c0-107">Update the storage settings.</span></span>

## <span data-ttu-id="d72c0-108">OS</span><span class="sxs-lookup"><span data-stu-id="d72c0-108">PARAMETERS</span></span>

### <span data-ttu-id="d72c0-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d72c0-109">-DefaultProfile</span></span>


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

### <span data-ttu-id="d72c0-110">-Force</span><span class="sxs-lookup"><span data-stu-id="d72c0-110">-Force</span></span>


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

### <span data-ttu-id="d72c0-111">-Local</span><span class="sxs-lookup"><span data-stu-id="d72c0-111">-Location</span></span>


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

### <span data-ttu-id="d72c0-112">-RetentionPeriodForDeletedStorageAccountsInDays</span><span class="sxs-lookup"><span data-stu-id="d72c0-112">-RetentionPeriodForDeletedStorageAccountsInDays</span></span>


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

### <span data-ttu-id="d72c0-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d72c0-113">-SubscriptionId</span></span>


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

### <span data-ttu-id="d72c0-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d72c0-114">-Confirm</span></span>
<span data-ttu-id="d72c0-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d72c0-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d72c0-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d72c0-116">-WhatIf</span></span>
<span data-ttu-id="d72c0-117">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d72c0-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d72c0-118">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d72c0-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d72c0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d72c0-119">CommonParameters</span></span>
<span data-ttu-id="d72c0-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d72c0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d72c0-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d72c0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d72c0-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d72c0-122">INPUTS</span></span>

## <span data-ttu-id="d72c0-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d72c0-123">OUTPUTS</span></span>

### <span data-ttu-id="d72c0-124">Microsoft. Azure. PowerShell. cmdlets. StorageAdmin. Models. Api201908Preview. ISettings</span><span class="sxs-lookup"><span data-stu-id="d72c0-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="d72c0-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d72c0-125">NOTES</span></span>

## <span data-ttu-id="d72c0-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d72c0-126">RELATED LINKS</span></span>

