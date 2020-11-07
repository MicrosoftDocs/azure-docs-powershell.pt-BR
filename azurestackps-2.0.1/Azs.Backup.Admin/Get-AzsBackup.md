---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackup
schema: 2.0.0
ms.openlocfilehash: 2c2d517da3be62ff407ca17577edefcf7322ad55
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945355"
---
# <span data-ttu-id="7198e-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="7198e-101">Get-AzsBackup</span></span>

## <span data-ttu-id="7198e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7198e-102">SYNOPSIS</span></span>
<span data-ttu-id="7198e-103">Retorna um backup de um local com base em nome.</span><span class="sxs-lookup"><span data-stu-id="7198e-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="7198e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7198e-104">SYNTAX</span></span>

### <span data-ttu-id="7198e-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="7198e-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7198e-106">Obter</span><span class="sxs-lookup"><span data-stu-id="7198e-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7198e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7198e-107">GetViaIdentity</span></span>
```
Get-AzsBackup -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7198e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7198e-108">DESCRIPTION</span></span>
<span data-ttu-id="7198e-109">Retorna um backup de um local com base em nome.</span><span class="sxs-lookup"><span data-stu-id="7198e-109">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="7198e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7198e-110">EXAMPLES</span></span>

### <span data-ttu-id="7198e-111">Exemplo 1: lista de backups</span><span class="sxs-lookup"><span data-stu-id="7198e-111">Example 1: List Backups</span></span>
```powershell
PS C:\> Get-AzsBackup

```

<span data-ttu-id="7198e-112">Obter informações sbout todos os backups do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="7198e-112">Get information sbout all Azure Stack backups.</span></span>

### <span data-ttu-id="7198e-113">Exemplo 2: obter backup específico</span><span class="sxs-lookup"><span data-stu-id="7198e-113">Example 2: Get specific backup</span></span>
```powershell
PS C:\> Get-AzsBackup -Name 'backupName'

```

<span data-ttu-id="7198e-114">Obter informações para o backup de pilha do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="7198e-114">Get information for the the specified Azure Stack backup.</span></span>

## <span data-ttu-id="7198e-115">OS</span><span class="sxs-lookup"><span data-stu-id="7198e-115">PARAMETERS</span></span>

### <span data-ttu-id="7198e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7198e-116">-DefaultProfile</span></span>
<span data-ttu-id="7198e-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7198e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7198e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7198e-118">-InputObject</span></span>
<span data-ttu-id="7198e-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="7198e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="7198e-120">-Local</span><span class="sxs-lookup"><span data-stu-id="7198e-120">-Location</span></span>
<span data-ttu-id="7198e-121">Nome do local de backup.</span><span class="sxs-lookup"><span data-stu-id="7198e-121">Name of the backup location.</span></span>

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

### <span data-ttu-id="7198e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7198e-122">-Name</span></span>
<span data-ttu-id="7198e-123">Nome do backup.</span><span class="sxs-lookup"><span data-stu-id="7198e-123">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7198e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7198e-124">-ResourceGroupName</span></span>
<span data-ttu-id="7198e-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7198e-125">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7198e-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="7198e-126">-Skip</span></span>
<span data-ttu-id="7198e-127">Parâmetro de ignorar OData.</span><span class="sxs-lookup"><span data-stu-id="7198e-127">OData skip parameter.</span></span>

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

### <span data-ttu-id="7198e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7198e-128">-SubscriptionId</span></span>
<span data-ttu-id="7198e-129">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7198e-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7198e-130">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="7198e-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7198e-131">-Início</span><span class="sxs-lookup"><span data-stu-id="7198e-131">-Top</span></span>
<span data-ttu-id="7198e-132">Parâmetro de topo do OData.</span><span class="sxs-lookup"><span data-stu-id="7198e-132">OData top parameter.</span></span>

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

### <span data-ttu-id="7198e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7198e-133">CommonParameters</span></span>
<span data-ttu-id="7198e-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7198e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7198e-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7198e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7198e-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7198e-136">INPUTS</span></span>

### <span data-ttu-id="7198e-137">Microsoft. Azure. PowerShell. cmdlets. BackupAdmin. Models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="7198e-137">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="7198e-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7198e-138">OUTPUTS</span></span>

### <span data-ttu-id="7198e-139">Microsoft. Azure. PowerShell. cmdlets. BackupAdmin. Models. Api20180901. IBackup</span><span class="sxs-lookup"><span data-stu-id="7198e-139">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackup</span></span>



## <span data-ttu-id="7198e-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7198e-140">NOTES</span></span>

<span data-ttu-id="7198e-141">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="7198e-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7198e-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7198e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7198e-143">INPUTobject <IBackupAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="7198e-143">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7198e-144">`[Backup <String>]`: Nome do backup.</span><span class="sxs-lookup"><span data-stu-id="7198e-144">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="7198e-145">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="7198e-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7198e-146">`[Location <String>]`: Nome do local de backup.</span><span class="sxs-lookup"><span data-stu-id="7198e-146">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="7198e-147">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7198e-147">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="7198e-148">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7198e-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7198e-149">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="7198e-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7198e-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7198e-150">RELATED LINKS</span></span>

