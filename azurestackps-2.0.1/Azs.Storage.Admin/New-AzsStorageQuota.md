---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/new-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: bd97eff2a0ed37c309ad0b50927f8231a2da27a6
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945165"
---
# <span data-ttu-id="10d09-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="10d09-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="10d09-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10d09-102">SYNOPSIS</span></span>


## <span data-ttu-id="10d09-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10d09-103">SYNTAX</span></span>

### <span data-ttu-id="10d09-104">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="10d09-104">CreateExpanded (Default)</span></span>
```
New-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>] [-CapacityInGb <Int32>]
 [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="10d09-105">Criados</span><span class="sxs-lookup"><span data-stu-id="10d09-105">Create</span></span>
```
New-AzsStorageQuota -Name <String> -QuotaObject <IStorageQuota> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="10d09-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="10d09-106">DESCRIPTION</span></span>


## <span data-ttu-id="10d09-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10d09-107">EXAMPLES</span></span>

### <span data-ttu-id="10d09-108">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="10d09-108">Example 1:</span></span>
```powershell
PS C:\> New-AzsStorageQuota -Name TestQuota -CapacityInGb 123 -NumberOfStorageAccounts 456
```

<span data-ttu-id="10d09-109">Criar uma nova cota de armazenamento com valores especificados.</span><span class="sxs-lookup"><span data-stu-id="10d09-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="10d09-110">OS</span><span class="sxs-lookup"><span data-stu-id="10d09-110">PARAMETERS</span></span>

### <span data-ttu-id="10d09-111">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="10d09-111">-CapacityInGb</span></span>


```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="10d09-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10d09-112">-DefaultProfile</span></span>


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

### <span data-ttu-id="10d09-113">-Local</span><span class="sxs-lookup"><span data-stu-id="10d09-113">-Location</span></span>


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

### <span data-ttu-id="10d09-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="10d09-114">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="10d09-115">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="10d09-115">-NumberOfStorageAccounts</span></span>


```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="10d09-116">-Quotaobject</span><span class="sxs-lookup"><span data-stu-id="10d09-116">-QuotaObject</span></span>
<span data-ttu-id="10d09-117">Para construir, consulte a seção observações para as propriedades QUOTAobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="10d09-117">To construct, see NOTES section for QUOTAOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="10d09-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="10d09-118">-SubscriptionId</span></span>


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

### <span data-ttu-id="10d09-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="10d09-119">-Confirm</span></span>
<span data-ttu-id="10d09-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10d09-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10d09-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10d09-121">-WhatIf</span></span>
<span data-ttu-id="10d09-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="10d09-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10d09-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="10d09-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10d09-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10d09-124">CommonParameters</span></span>
<span data-ttu-id="10d09-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10d09-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10d09-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10d09-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10d09-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="10d09-127">INPUTS</span></span>

### <span data-ttu-id="10d09-128">Microsoft. Azure. PowerShell. cmdlets. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="10d09-128">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>

## <span data-ttu-id="10d09-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="10d09-129">OUTPUTS</span></span>

### <span data-ttu-id="10d09-130">Microsoft. Azure. PowerShell. cmdlets. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="10d09-130">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="10d09-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="10d09-131">NOTES</span></span>

<span data-ttu-id="10d09-132">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="10d09-132">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="10d09-133">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="10d09-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="10d09-134">QUOTAobject <IStorageQuota> :</span><span class="sxs-lookup"><span data-stu-id="10d09-134">QUOTAOBJECT <IStorageQuota>:</span></span> 
  - <span data-ttu-id="10d09-135">`[CapacityInGb <Int32?>]`: Capacidade máxima (GB).</span><span class="sxs-lookup"><span data-stu-id="10d09-135">`[CapacityInGb <Int32?>]`: Maximum capacity (GB).</span></span>
  - <span data-ttu-id="10d09-136">`[NumberOfStorageAccounts <Int32?>]`: Número total de contas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="10d09-136">`[NumberOfStorageAccounts <Int32?>]`: Total number of storage accounts.</span></span>

## <span data-ttu-id="10d09-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10d09-137">RELATED LINKS</span></span>

