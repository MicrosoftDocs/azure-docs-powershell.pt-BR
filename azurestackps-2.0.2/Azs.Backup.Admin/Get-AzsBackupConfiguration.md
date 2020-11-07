---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: 3a9fedc637f8400b952d823a98dfe0abaa1d40d3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93947041"
---
# <span data-ttu-id="c939a-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="c939a-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="c939a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c939a-102">SYNOPSIS</span></span>
<span data-ttu-id="c939a-103">Retorna um local de backup específico com base no nome.</span><span class="sxs-lookup"><span data-stu-id="c939a-103">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="c939a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c939a-104">SYNTAX</span></span>

### <span data-ttu-id="c939a-105">Get (padrão)</span><span class="sxs-lookup"><span data-stu-id="c939a-105">Get (Default)</span></span>
```
Get-AzsBackupConfiguration [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c939a-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c939a-106">GetViaIdentity</span></span>
```
Get-AzsBackupConfiguration -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c939a-107">Programação</span><span class="sxs-lookup"><span data-stu-id="c939a-107">List</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c939a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c939a-108">DESCRIPTION</span></span>
<span data-ttu-id="c939a-109">Retorna um local de backup específico com base no nome.</span><span class="sxs-lookup"><span data-stu-id="c939a-109">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="c939a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c939a-110">EXAMPLES</span></span>

### <span data-ttu-id="c939a-111">Exemplo 1: Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="c939a-111">Example 1: Get-AzsBackupConfiguration</span></span>
```powershell
PS C:\> Get-AzsBackupConfiguration

```

<span data-ttu-id="c939a-112">Obtenha a configuração de backup do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="c939a-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="c939a-113">OS</span><span class="sxs-lookup"><span data-stu-id="c939a-113">PARAMETERS</span></span>

### <span data-ttu-id="c939a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c939a-114">-DefaultProfile</span></span>
<span data-ttu-id="c939a-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c939a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c939a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c939a-116">-InputObject</span></span>
<span data-ttu-id="c939a-117">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c939a-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c939a-118">-Local</span><span class="sxs-lookup"><span data-stu-id="c939a-118">-Location</span></span>
<span data-ttu-id="c939a-119">Nome do local de backup.</span><span class="sxs-lookup"><span data-stu-id="c939a-119">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c939a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c939a-120">-ResourceGroupName</span></span>
<span data-ttu-id="c939a-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c939a-121">Name of the resource group.</span></span>

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

### <span data-ttu-id="c939a-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="c939a-122">-Skip</span></span>
<span data-ttu-id="c939a-123">Parâmetro de ignorar OData.</span><span class="sxs-lookup"><span data-stu-id="c939a-123">OData skip parameter.</span></span>

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

### <span data-ttu-id="c939a-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c939a-124">-SubscriptionId</span></span>
<span data-ttu-id="c939a-125">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c939a-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c939a-126">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c939a-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c939a-127">-Início</span><span class="sxs-lookup"><span data-stu-id="c939a-127">-Top</span></span>
<span data-ttu-id="c939a-128">Parâmetro de topo do OData.</span><span class="sxs-lookup"><span data-stu-id="c939a-128">OData top parameter.</span></span>

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

### <span data-ttu-id="c939a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c939a-129">CommonParameters</span></span>
<span data-ttu-id="c939a-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c939a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c939a-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c939a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c939a-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c939a-132">INPUTS</span></span>

### <span data-ttu-id="c939a-133">Microsoft. Azure. PowerShell. cmdlets. BackupAdmin. Models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="c939a-133">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="c939a-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c939a-134">OUTPUTS</span></span>

### <span data-ttu-id="c939a-135">Microsoft. Azure. PowerShell. cmdlets. BackupAdmin. Models. Api20180901. IBackupLocation</span><span class="sxs-lookup"><span data-stu-id="c939a-135">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>

## <span data-ttu-id="c939a-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c939a-136">NOTES</span></span>

<span data-ttu-id="c939a-137">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="c939a-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c939a-138">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c939a-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c939a-139">INPUTobject <IBackupAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="c939a-139">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c939a-140">`[Backup <String>]`: Nome do backup.</span><span class="sxs-lookup"><span data-stu-id="c939a-140">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="c939a-141">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="c939a-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c939a-142">`[Location <String>]`: Nome do local de backup.</span><span class="sxs-lookup"><span data-stu-id="c939a-142">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="c939a-143">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c939a-143">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="c939a-144">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c939a-144">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c939a-145">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c939a-145">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c939a-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c939a-146">RELATED LINKS</span></span>

