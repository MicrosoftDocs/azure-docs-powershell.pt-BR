---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/remove-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: 258c7057b8f78ea6de1db506d23c60f679e1ca39
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775974"
---
# <span data-ttu-id="1484a-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="1484a-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="1484a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1484a-102">SYNOPSIS</span></span>


## <span data-ttu-id="1484a-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1484a-103">SYNTAX</span></span>

### <span data-ttu-id="1484a-104">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="1484a-104">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1484a-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1484a-105">DeleteViaIdentity</span></span>
```
Remove-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1484a-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1484a-106">DESCRIPTION</span></span>


## <span data-ttu-id="1484a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1484a-107">EXAMPLES</span></span>

### <span data-ttu-id="1484a-108">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="1484a-108">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsStorageQuota -Name 'TestQuota'
```

<span data-ttu-id="1484a-109">Remova uma cota de armazenamento por nome.</span><span class="sxs-lookup"><span data-stu-id="1484a-109">Remove a storage quota by name.</span></span>

### <span data-ttu-id="1484a-110">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="1484a-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestQuota' | Remove-AzsStorageQuota
```

<span data-ttu-id="1484a-111">Remova uma cota de armazenamento por tubulação.</span><span class="sxs-lookup"><span data-stu-id="1484a-111">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="1484a-112">OS</span><span class="sxs-lookup"><span data-stu-id="1484a-112">PARAMETERS</span></span>

### <span data-ttu-id="1484a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1484a-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="1484a-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1484a-114">-InputObject</span></span>
<span data-ttu-id="1484a-115">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="1484a-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="1484a-116">-Local</span><span class="sxs-lookup"><span data-stu-id="1484a-116">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1484a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="1484a-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1484a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1484a-118">-PassThru</span></span>


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

### <span data-ttu-id="1484a-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1484a-119">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1484a-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1484a-120">-Confirm</span></span>
<span data-ttu-id="1484a-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1484a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1484a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1484a-122">-WhatIf</span></span>
<span data-ttu-id="1484a-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1484a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1484a-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1484a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1484a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1484a-125">CommonParameters</span></span>
<span data-ttu-id="1484a-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1484a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1484a-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1484a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1484a-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1484a-128">INPUTS</span></span>

### <span data-ttu-id="1484a-129">Microsoft. Azure. PowerShell. cmdlets. StorageAdmin. Models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="1484a-129">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="1484a-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1484a-130">OUTPUTS</span></span>

### <span data-ttu-id="1484a-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1484a-131">System.Boolean</span></span>



## <span data-ttu-id="1484a-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1484a-132">NOTES</span></span>

<span data-ttu-id="1484a-133">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="1484a-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1484a-134">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1484a-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1484a-135">INPUTobject <IStorageAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="1484a-135">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="1484a-136">`[AccountId <String>]`: ID da conta de armazenamento interno, que não está visível para locatário.</span><span class="sxs-lookup"><span data-stu-id="1484a-136">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="1484a-137">`[AsyncOperationId <String>]`: ID da operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="1484a-137">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="1484a-138">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="1484a-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1484a-139">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="1484a-139">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="1484a-140">`[QuotaName <String>]`: O nome da cota de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1484a-140">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="1484a-141">`[ResourceGroup <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1484a-141">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="1484a-142">`[ServiceName <String>]`: Nome do serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1484a-142">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="1484a-143">`[SubscriptionId <String>]`: ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="1484a-143">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="1484a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1484a-144">RELATED LINKS</span></span>
