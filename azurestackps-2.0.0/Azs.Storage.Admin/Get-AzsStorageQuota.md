---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: ed5261a9b6d65918fce0fd90c8f2db0ff42baa3a
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/22/2020
ms.locfileid: "93945085"
---
# <span data-ttu-id="7cdf0-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="7cdf0-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="7cdf0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7cdf0-102">SYNOPSIS</span></span>


## <span data-ttu-id="7cdf0-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7cdf0-103">SYNTAX</span></span>

### <span data-ttu-id="7cdf0-104">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="7cdf0-104">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="7cdf0-105">Obter</span><span class="sxs-lookup"><span data-stu-id="7cdf0-105">Get</span></span>
```
Get-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7cdf0-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7cdf0-106">GetViaIdentity</span></span>
```
Get-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7cdf0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7cdf0-107">DESCRIPTION</span></span>


## <span data-ttu-id="7cdf0-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7cdf0-108">EXAMPLES</span></span>

### <span data-ttu-id="7cdf0-109">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="7cdf0-109">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota
```

<span data-ttu-id="7cdf0-110">Obter a lista de cotas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-110">Get the list of storage quotas.</span></span>

### <span data-ttu-id="7cdf0-111">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="7cdf0-111">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'Default Quota'
```

<span data-ttu-id="7cdf0-112">Obter detalhes da cota de armazenamento especificada por nome.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-112">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="7cdf0-113">OS</span><span class="sxs-lookup"><span data-stu-id="7cdf0-113">PARAMETERS</span></span>

### <span data-ttu-id="7cdf0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cdf0-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="7cdf0-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cdf0-115">-InputObject</span></span>
<span data-ttu-id="7cdf0-116">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-116">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: System.String
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="7cdf0-117">-Local</span><span class="sxs-lookup"><span data-stu-id="7cdf0-117">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7cdf0-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="7cdf0-118">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7cdf0-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7cdf0-119">-SubscriptionId</span></span>


```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7cdf0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cdf0-120">CommonParameters</span></span>
<span data-ttu-id="7cdf0-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cdf0-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7cdf0-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cdf0-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7cdf0-123">INPUTS</span></span>

### <span data-ttu-id="7cdf0-124">Microsoft. Azure. PowerShell. cmdlets. StorageAdmin. Models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="7cdf0-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="7cdf0-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7cdf0-125">OUTPUTS</span></span>

### <span data-ttu-id="7cdf0-126">Microsoft. Azure. PowerShell. cmdlets. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="7cdf0-126">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="7cdf0-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7cdf0-127">NOTES</span></span>

<span data-ttu-id="7cdf0-128">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-128">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7cdf0-129">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-129">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7cdf0-130">INPUTobject <IStorageAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="7cdf0-130">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="7cdf0-131">`[AccountId <String>]`: ID da conta de armazenamento interno, que não está visível para locatário.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-131">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="7cdf0-132">`[AsyncOperationId <String>]`: ID da operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-132">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="7cdf0-133">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="7cdf0-133">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7cdf0-134">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-134">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="7cdf0-135">`[QuotaName <String>]`: O nome da cota de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-135">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="7cdf0-136">`[ResourceGroup <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-136">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="7cdf0-137">`[ServiceName <String>]`: Nome do serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-137">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="7cdf0-138">`[SubscriptionId <String>]`: ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-138">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="7cdf0-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7cdf0-139">RELATED LINKS</span></span>

