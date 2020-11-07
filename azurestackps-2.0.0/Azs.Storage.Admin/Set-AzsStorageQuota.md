---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: b89bef906cf54378719c7c6b83dcaff484ced282
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775973"
---
# <span data-ttu-id="c440b-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="c440b-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="c440b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c440b-102">SYNOPSIS</span></span>


## <span data-ttu-id="c440b-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c440b-103">SYNTAX</span></span>

### <span data-ttu-id="c440b-104">Nome (padrão)</span><span class="sxs-lookup"><span data-stu-id="c440b-104">Name (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>] [-CapacityInGb <Int32>]
 [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c440b-105">Quotaobject</span><span class="sxs-lookup"><span data-stu-id="c440b-105">QuotaObject</span></span>
```
Set-AzsStorageQuota -QuotaObject <IStorageQuota> [-Location <String>] [-SubscriptionId <String>]
 [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c440b-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c440b-106">DESCRIPTION</span></span>


## <span data-ttu-id="c440b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c440b-107">EXAMPLES</span></span>

### <span data-ttu-id="c440b-108">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="c440b-108">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -NumberOfStorageAccounts 11 -CapacityInGb 22
```

<span data-ttu-id="c440b-109">Atualize uma cota de armazenamento existente por nome.</span><span class="sxs-lookup"><span data-stu-id="c440b-109">Update an existing storage quota by name.</span></span>

### <span data-ttu-id="c440b-110">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="c440b-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestUpdateStorageQuota' | Set-AzsStorageQuota -NumberOfStorageAccounts 22 -CapacityInGb 33
```

<span data-ttu-id="c440b-111">Atualize uma cota de armazenamento existente por tubulação.</span><span class="sxs-lookup"><span data-stu-id="c440b-111">Update an existing storage quota by piping.</span></span>

## <span data-ttu-id="c440b-112">OS</span><span class="sxs-lookup"><span data-stu-id="c440b-112">PARAMETERS</span></span>

### <span data-ttu-id="c440b-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="c440b-113">-CapacityInGb</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c440b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c440b-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="c440b-115">-Local</span><span class="sxs-lookup"><span data-stu-id="c440b-115">-Location</span></span>


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

### <span data-ttu-id="c440b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c440b-116">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Name
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c440b-117">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="c440b-117">-NumberOfStorageAccounts</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c440b-118">-Quotaobject</span><span class="sxs-lookup"><span data-stu-id="c440b-118">-QuotaObject</span></span>
<span data-ttu-id="c440b-119">Para construir, consulte a seção observações para as propriedades QUOTAobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c440b-119">To construct, see NOTES section for QUOTAOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota
Parameter Sets: QuotaObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c440b-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c440b-120">-SubscriptionId</span></span>


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

### <span data-ttu-id="c440b-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c440b-121">-Confirm</span></span>
<span data-ttu-id="c440b-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c440b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c440b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c440b-123">-WhatIf</span></span>
<span data-ttu-id="c440b-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c440b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c440b-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c440b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c440b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c440b-126">CommonParameters</span></span>
<span data-ttu-id="c440b-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c440b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c440b-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c440b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c440b-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c440b-129">INPUTS</span></span>

### <span data-ttu-id="c440b-130">Microsoft. Azure. PowerShell. cmdlets. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="c440b-130">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>

## <span data-ttu-id="c440b-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c440b-131">OUTPUTS</span></span>

### <span data-ttu-id="c440b-132">Microsoft. Azure. PowerShell. cmdlets. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="c440b-132">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="c440b-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c440b-133">NOTES</span></span>

<span data-ttu-id="c440b-134">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="c440b-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c440b-135">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c440b-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c440b-136">QUOTAobject <IStorageQuota> :</span><span class="sxs-lookup"><span data-stu-id="c440b-136">QUOTAOBJECT <IStorageQuota>:</span></span> 
  - <span data-ttu-id="c440b-137">`[CapacityInGb <Int32?>]`: Capacidade máxima (GB).</span><span class="sxs-lookup"><span data-stu-id="c440b-137">`[CapacityInGb <Int32?>]`: Maximum capacity (GB).</span></span>
  - <span data-ttu-id="c440b-138">`[NumberOfStorageAccounts <Int32?>]`: Número total de contas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c440b-138">`[NumberOfStorageAccounts <Int32?>]`: Total number of storage accounts.</span></span>

## <span data-ttu-id="c440b-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c440b-139">RELATED LINKS</span></span>

