---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 0ddf99277834e69a55b009abcb4b683eebb7a4ec
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945327"
---
# <span data-ttu-id="56bf4-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56bf4-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="56bf4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="56bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="56bf4-103">Retorna a conta de armazenamento solicitada.</span><span class="sxs-lookup"><span data-stu-id="56bf4-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="56bf4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56bf4-104">SYNTAX</span></span>

### <span data-ttu-id="56bf4-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="56bf4-105">List (Default)</span></span>
```
Get-AzsStorageAccount [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>] [-Summary]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="56bf4-106">Obter</span><span class="sxs-lookup"><span data-stu-id="56bf4-106">Get</span></span>
```
Get-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="56bf4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="56bf4-107">GetViaIdentity</span></span>
```
Get-AzsStorageAccount -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="56bf4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="56bf4-108">DESCRIPTION</span></span>
<span data-ttu-id="56bf4-109">Retorna a conta de armazenamento solicitada.</span><span class="sxs-lookup"><span data-stu-id="56bf4-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="56bf4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56bf4-110">EXAMPLES</span></span>

### <span data-ttu-id="56bf4-111">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="56bf4-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Summary
```

<span data-ttu-id="56bf4-112">Obter uma lista de contas de armazenamento (resumo).</span><span class="sxs-lookup"><span data-stu-id="56bf4-112">Get a list of storage accounts (summary).</span></span>

### <span data-ttu-id="56bf4-113">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="56bf4-113">Example 2:</span></span>
```powershell
PS C:\> $storageAccount = Get-AzsStorageAccount
PS C:\> $storageAccount | Select Location,Name,AccountStatus,HealthState,Kind | ft
```

<span data-ttu-id="56bf4-114">Obtenha uma lista de contas de armazenamento com detalhes e imprima o status.</span><span class="sxs-lookup"><span data-stu-id="56bf4-114">Get a list of storage account with details and print the status.</span></span>

### <span data-ttu-id="56bf4-115">Exemplo 3:</span><span class="sxs-lookup"><span data-stu-id="56bf4-115">Example 3:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 | fl *
```

<span data-ttu-id="56bf4-116">Obter detalhes da conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="56bf4-116">Get details of the specified storage account.</span></span>

## <span data-ttu-id="56bf4-117">OS</span><span class="sxs-lookup"><span data-stu-id="56bf4-117">PARAMETERS</span></span>

### <span data-ttu-id="56bf4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56bf4-118">-DefaultProfile</span></span>
<span data-ttu-id="56bf4-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="56bf4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56bf4-120">-Filtro</span><span class="sxs-lookup"><span data-stu-id="56bf4-120">-Filter</span></span>
<span data-ttu-id="56bf4-121">Cadeia de caracteres de filtro</span><span class="sxs-lookup"><span data-stu-id="56bf4-121">Filter string</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="56bf4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56bf4-122">-InputObject</span></span>
<span data-ttu-id="56bf4-123">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="56bf4-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="56bf4-124">-Local</span><span class="sxs-lookup"><span data-stu-id="56bf4-124">-Location</span></span>
<span data-ttu-id="56bf4-125">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="56bf4-125">Resource location.</span></span>

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

### <span data-ttu-id="56bf4-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="56bf4-126">-Name</span></span>
<span data-ttu-id="56bf4-127">ID da conta de armazenamento interna, que não está visível para Tenant.</span><span class="sxs-lookup"><span data-stu-id="56bf4-127">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccountId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="56bf4-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56bf4-128">-SubscriptionId</span></span>
<span data-ttu-id="56bf4-129">ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="56bf4-129">Subscription Id.</span></span>

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

### <span data-ttu-id="56bf4-130">-Resumo</span><span class="sxs-lookup"><span data-stu-id="56bf4-130">-Summary</span></span>
<span data-ttu-id="56bf4-131">Alternar se as informações detalhadas ou resumo são retornadas.</span><span class="sxs-lookup"><span data-stu-id="56bf4-131">Switch for whether summary or detailed information is returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: $false
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="56bf4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56bf4-132">CommonParameters</span></span>
<span data-ttu-id="56bf4-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56bf4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56bf4-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56bf4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56bf4-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="56bf4-135">INPUTS</span></span>

### <span data-ttu-id="56bf4-136">Microsoft. Azure. PowerShell. cmdlets. StorageAdmin. Models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="56bf4-136">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="56bf4-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="56bf4-137">OUTPUTS</span></span>

### <span data-ttu-id="56bf4-138">Microsoft. Azure. PowerShell. cmdlets. StorageAdmin. Models. Api201908Preview. IStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56bf4-138">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageAccount</span></span>



## <span data-ttu-id="56bf4-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="56bf4-139">NOTES</span></span>

<span data-ttu-id="56bf4-140">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="56bf4-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="56bf4-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="56bf4-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="56bf4-142">INPUTobject <IStorageAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="56bf4-142">INPUTOBJECT <IStorageAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="56bf4-143">`[AccountId <String>]`: ID da conta de armazenamento interno, que não está visível para locatário.</span><span class="sxs-lookup"><span data-stu-id="56bf4-143">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="56bf4-144">`[AsyncOperationId <String>]`: ID da operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="56bf4-144">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="56bf4-145">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="56bf4-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="56bf4-146">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="56bf4-146">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="56bf4-147">`[QuotaName <String>]`: O nome da cota de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="56bf4-147">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="56bf4-148">`[ResourceGroup <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="56bf4-148">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="56bf4-149">`[ServiceName <String>]`: Nome do serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="56bf4-149">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="56bf4-150">`[SubscriptionId <String>]`: ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="56bf4-150">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="56bf4-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56bf4-151">RELATED LINKS</span></span>

