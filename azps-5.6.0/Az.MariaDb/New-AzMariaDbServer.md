---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/new-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
ms.openlocfilehash: ccd05d8c0a7678b16831659fb0ca119adf94ddae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886616"
---
# <span data-ttu-id="7c1b0-101">New-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="7c1b0-101">New-AzMariaDbServer</span></span>

## <span data-ttu-id="7c1b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c1b0-102">SYNOPSIS</span></span>
<span data-ttu-id="7c1b0-103">Cria um novo MariaDB.</span><span class="sxs-lookup"><span data-stu-id="7c1b0-103">Creates a new MariaDB.</span></span>

## <span data-ttu-id="7c1b0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7c1b0-104">SYNTAX</span></span>

```
New-AzMariaDbServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUsername <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7c1b0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7c1b0-105">DESCRIPTION</span></span>
<span data-ttu-id="7c1b0-106">Cria um novo MariaDB.</span><span class="sxs-lookup"><span data-stu-id="7c1b0-106">Creates a new MariaDB.</span></span>

## <span data-ttu-id="7c1b0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c1b0-107">EXAMPLES</span></span>

### <span data-ttu-id="7c1b0-108">Exemplo 1: Criar um novo MariaDB</span><span class="sxs-lookup"><span data-stu-id="7c1b0-108">Example 1: Create a new MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbServer -Name mariadb-aassd-01 -ResourceGroupName lucas-manual-test -Sku 'B_Gen5_1' -Location eastus
cmdlet New-AzMariaDbServer at command pipeline position 1
Supply values for the following parameters:
AdministratorUsername: adminuser
AdministratorLoginPassword: ************

Name             Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----             -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-aassd-01 eastus   adminuser          10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="7c1b0-109">Este comando cria um novo MariaDB.</span><span class="sxs-lookup"><span data-stu-id="7c1b0-109">This command creates a new MariaDB.</span></span>

## <span data-ttu-id="7c1b0-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7c1b0-110">PARAMETERS</span></span>

### <span data-ttu-id="7c1b0-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="7c1b0-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="7c1b0-112">Senha do administrador, deve ser SecureString.</span><span class="sxs-lookup"><span data-stu-id="7c1b0-112">Password of administrator, should be SecureString.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c1b0-113">-AdministratorUsername</span><span class="sxs-lookup"><span data-stu-id="7c1b0-113">-AdministratorUsername</span></span>
<span data-ttu-id="7c1b0-114">Nome de usuário do administrador.</span><span class="sxs-lookup"><span data-stu-id="7c1b0-114">Username of administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c1b0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c1b0-115">-AsJob</span></span>
<span data-ttu-id="7c1b0-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="7c1b0-116">Run the command as a job</span></span>

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

### <span data-ttu-id="7c1b0-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="7c1b0-117">-BackupRetentionDay</span></span>
<span data-ttu-id="7c1b0-118">Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="7c1b0-118">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="7c1b0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c1b0-119">-DefaultProfile</span></span>
<span data-ttu-id="7c1b0-120">região DefaultParameters As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7c1b0-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c1b0-121">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="7c1b0-121">-GeoRedundantBackup</span></span>
<span data-ttu-id="7c1b0-122">Habilitar Geo-redundante ou não para backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="7c1b0-122">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c1b0-123">-Location</span><span class="sxs-lookup"><span data-stu-id="7c1b0-123">-Location</span></span>
<span data-ttu-id="7c1b0-124">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="7c1b0-124">The location the resource resides in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c1b0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7c1b0-125">-Name</span></span>
<span data-ttu-id="7c1b0-126">Nome do servidor MariaDB.</span><span class="sxs-lookup"><span data-stu-id="7c1b0-126">MariaDB server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c1b0-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7c1b0-127">-NoWait</span></span>
<span data-ttu-id="7c1b0-128">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="7c1b0-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7c1b0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c1b0-129">-ResourceGroupName</span></span>
<span data-ttu-id="7c1b0-130">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="7c1b0-130">The name of the resource group that contains the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c1b0-131">-Sku</span><span class="sxs-lookup"><span data-stu-id="7c1b0-131">-Sku</span></span>
<span data-ttu-id="7c1b0-132">O nome do sku, normalmente, camada + família + núcleos, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="7c1b0-132">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c1b0-133">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="7c1b0-133">-SslEnforcement</span></span>
<span data-ttu-id="7c1b0-134">Habilitar a imposição ssl ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="7c1b0-134">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c1b0-135">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="7c1b0-135">-StorageAutogrow</span></span>
<span data-ttu-id="7c1b0-136">Habilitar o Crescimento Automático de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7c1b0-136">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c1b0-137">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="7c1b0-137">-StorageInMb</span></span>
<span data-ttu-id="7c1b0-138">Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="7c1b0-138">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="7c1b0-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c1b0-139">-SubscriptionId</span></span>
<span data-ttu-id="7c1b0-140">A ID da assinatura faz parte do URI para cada chamada de serviço</span><span class="sxs-lookup"><span data-stu-id="7c1b0-140">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="7c1b0-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="7c1b0-141">-Tag</span></span>
<span data-ttu-id="7c1b0-142">Metadados específicos do aplicativo na forma de pares de valores-chave.</span><span class="sxs-lookup"><span data-stu-id="7c1b0-142">Application-specific metadata in the form of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c1b0-143">-Version</span><span class="sxs-lookup"><span data-stu-id="7c1b0-143">-Version</span></span>
<span data-ttu-id="7c1b0-144">Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="7c1b0-144">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c1b0-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c1b0-145">-Confirm</span></span>
<span data-ttu-id="7c1b0-146">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c1b0-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c1b0-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c1b0-147">-WhatIf</span></span>
<span data-ttu-id="7c1b0-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7c1b0-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c1b0-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7c1b0-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c1b0-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c1b0-150">CommonParameters</span></span>
<span data-ttu-id="7c1b0-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c1b0-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c1b0-152">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c1b0-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c1b0-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c1b0-153">INPUTS</span></span>

## <span data-ttu-id="7c1b0-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7c1b0-154">OUTPUTS</span></span>

### <span data-ttu-id="7c1b0-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="7c1b0-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="7c1b0-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="7c1b0-156">NOTES</span></span>

<span data-ttu-id="7c1b0-157">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7c1b0-157">ALIASES</span></span>

## <span data-ttu-id="7c1b0-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c1b0-158">RELATED LINKS</span></span>

