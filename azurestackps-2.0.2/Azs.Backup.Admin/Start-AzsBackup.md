---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/start-azsbackup
schema: 2.0.0
ms.openlocfilehash: 37fc3ddb1c878bc8b6b1e14d920a5747edce0cd3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93947034"
---
# <span data-ttu-id="2c33c-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="2c33c-101">Start-AzsBackup</span></span>

## <span data-ttu-id="2c33c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c33c-102">SYNOPSIS</span></span>
<span data-ttu-id="2c33c-103">Fazer backup de um local específico.</span><span class="sxs-lookup"><span data-stu-id="2c33c-103">Back up a specific location.</span></span>

## <span data-ttu-id="2c33c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c33c-104">SYNTAX</span></span>

### <span data-ttu-id="2c33c-105">Criar (padrão)</span><span class="sxs-lookup"><span data-stu-id="2c33c-105">Create (Default)</span></span>
```
Start-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2c33c-106">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2c33c-106">CreateViaIdentity</span></span>
```
Start-AzsBackup -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2c33c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c33c-107">DESCRIPTION</span></span>
<span data-ttu-id="2c33c-108">Fazer backup de um local específico.</span><span class="sxs-lookup"><span data-stu-id="2c33c-108">Back up a specific location.</span></span>

## <span data-ttu-id="2c33c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c33c-109">EXAMPLES</span></span>

### <span data-ttu-id="2c33c-110">Exemplo 1: iniciar azurestack backup</span><span class="sxs-lookup"><span data-stu-id="2c33c-110">Example 1: Start azurestack backup</span></span>
```powershell
PS C:\>Start-AzsBackup

```

<span data-ttu-id="2c33c-111">Inicie um backup do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="2c33c-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="2c33c-112">OS</span><span class="sxs-lookup"><span data-stu-id="2c33c-112">PARAMETERS</span></span>

### <span data-ttu-id="2c33c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c33c-113">-AsJob</span></span>
<span data-ttu-id="2c33c-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="2c33c-114">Run the command as a job</span></span>

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

### <span data-ttu-id="2c33c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c33c-115">-DefaultProfile</span></span>
<span data-ttu-id="2c33c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c33c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c33c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c33c-117">-InputObject</span></span>
<span data-ttu-id="2c33c-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2c33c-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="2c33c-119">-Local</span><span class="sxs-lookup"><span data-stu-id="2c33c-119">-Location</span></span>
<span data-ttu-id="2c33c-120">Nome do local de backup.</span><span class="sxs-lookup"><span data-stu-id="2c33c-120">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2c33c-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2c33c-121">-NoWait</span></span>
<span data-ttu-id="2c33c-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="2c33c-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2c33c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c33c-123">-ResourceGroupName</span></span>
<span data-ttu-id="2c33c-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2c33c-124">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2c33c-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c33c-125">-SubscriptionId</span></span>
<span data-ttu-id="2c33c-126">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2c33c-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2c33c-127">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="2c33c-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2c33c-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2c33c-128">-Confirm</span></span>
<span data-ttu-id="2c33c-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c33c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c33c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c33c-130">-WhatIf</span></span>
<span data-ttu-id="2c33c-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2c33c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c33c-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c33c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c33c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c33c-133">CommonParameters</span></span>
<span data-ttu-id="2c33c-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c33c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c33c-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c33c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c33c-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c33c-136">INPUTS</span></span>

### <span data-ttu-id="2c33c-137">Microsoft. Azure. PowerShell. cmdlets. BackupAdmin. Models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="2c33c-137">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="2c33c-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c33c-138">OUTPUTS</span></span>

### <span data-ttu-id="2c33c-139">Microsoft. Azure. PowerShell. cmdlets. BackupAdmin. Models. Api20180901. IBackup</span><span class="sxs-lookup"><span data-stu-id="2c33c-139">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackup</span></span>



## <span data-ttu-id="2c33c-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c33c-140">NOTES</span></span>

<span data-ttu-id="2c33c-141">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="2c33c-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2c33c-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2c33c-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2c33c-143">INPUTobject <IBackupAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="2c33c-143">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2c33c-144">`[Backup <String>]`: Nome do backup.</span><span class="sxs-lookup"><span data-stu-id="2c33c-144">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="2c33c-145">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="2c33c-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2c33c-146">`[Location <String>]`: Nome do local de backup.</span><span class="sxs-lookup"><span data-stu-id="2c33c-146">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="2c33c-147">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2c33c-147">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="2c33c-148">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2c33c-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2c33c-149">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="2c33c-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2c33c-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c33c-150">RELATED LINKS</span></span>

