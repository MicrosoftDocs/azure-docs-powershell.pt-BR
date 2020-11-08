---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
ms.openlocfilehash: e6416fd67091fc86a5fe9844d3b1d366aaa6cb58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124589"
---
# <span data-ttu-id="1a13f-101">New-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="1a13f-101">New-AzMariaDbServer</span></span>

## <span data-ttu-id="1a13f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a13f-102">SYNOPSIS</span></span>
<span data-ttu-id="1a13f-103">Cria um novo MariaDB.</span><span class="sxs-lookup"><span data-stu-id="1a13f-103">Creates a new MariaDB.</span></span>

## <span data-ttu-id="1a13f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a13f-104">SYNTAX</span></span>

```
New-AzMariaDbServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUsername <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1a13f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1a13f-105">DESCRIPTION</span></span>
<span data-ttu-id="1a13f-106">Cria um novo MariaDB.</span><span class="sxs-lookup"><span data-stu-id="1a13f-106">Creates a new MariaDB.</span></span>

## <span data-ttu-id="1a13f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a13f-107">EXAMPLES</span></span>

### <span data-ttu-id="1a13f-108">Exemplo 1: criar um novo MariaDB</span><span class="sxs-lookup"><span data-stu-id="1a13f-108">Example 1: Create a new MariaDB</span></span>
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

<span data-ttu-id="1a13f-109">Esse comando cria um novo MariaDB.</span><span class="sxs-lookup"><span data-stu-id="1a13f-109">This command creates a new MariaDB.</span></span>

## <span data-ttu-id="1a13f-110">OS</span><span class="sxs-lookup"><span data-stu-id="1a13f-110">PARAMETERS</span></span>

### <span data-ttu-id="1a13f-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="1a13f-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="1a13f-112">A senha do administrador deve ser SecureString.</span><span class="sxs-lookup"><span data-stu-id="1a13f-112">Password of administrator, should be SecureString.</span></span>

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

### <span data-ttu-id="1a13f-113">-AdministratorUsername</span><span class="sxs-lookup"><span data-stu-id="1a13f-113">-AdministratorUsername</span></span>
<span data-ttu-id="1a13f-114">Nome de usuário do administrador.</span><span class="sxs-lookup"><span data-stu-id="1a13f-114">Username of administrator.</span></span>

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

### <span data-ttu-id="1a13f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a13f-115">-AsJob</span></span>
<span data-ttu-id="1a13f-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="1a13f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1a13f-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="1a13f-117">-BackupRetentionDay</span></span>
<span data-ttu-id="1a13f-118">Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="1a13f-118">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="1a13f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a13f-119">-DefaultProfile</span></span>
<span data-ttu-id="1a13f-120">Region Defaultparameters as credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1a13f-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a13f-121">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="1a13f-121">-GeoRedundantBackup</span></span>
<span data-ttu-id="1a13f-122">Habilite a redundância geográfica ou não para o backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="1a13f-122">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="1a13f-123">-Local</span><span class="sxs-lookup"><span data-stu-id="1a13f-123">-Location</span></span>
<span data-ttu-id="1a13f-124">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="1a13f-124">The location the resource resides in.</span></span>

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

### <span data-ttu-id="1a13f-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a13f-125">-Name</span></span>
<span data-ttu-id="1a13f-126">Nome do servidor MariaDB.</span><span class="sxs-lookup"><span data-stu-id="1a13f-126">MariaDB server name.</span></span>

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

### <span data-ttu-id="1a13f-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="1a13f-127">-NoWait</span></span>
<span data-ttu-id="1a13f-128">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="1a13f-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1a13f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a13f-129">-ResourceGroupName</span></span>
<span data-ttu-id="1a13f-130">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="1a13f-130">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="1a13f-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="1a13f-131">-Sku</span></span>
<span data-ttu-id="1a13f-132">O nome do SKU, geralmente, a camada + família + núcleos, por exemplo B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="1a13f-132">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="1a13f-133">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="1a13f-133">-SslEnforcement</span></span>
<span data-ttu-id="1a13f-134">Habilite a imposição de SSL ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="1a13f-134">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="1a13f-135">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="1a13f-135">-StorageAutogrow</span></span>
<span data-ttu-id="1a13f-136">Habilite o aumento automático do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1a13f-136">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="1a13f-137">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="1a13f-137">-StorageInMb</span></span>
<span data-ttu-id="1a13f-138">Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="1a13f-138">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="1a13f-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1a13f-139">-SubscriptionId</span></span>
<span data-ttu-id="1a13f-140">A ID da assinatura faz parte do URI para cada chamada de serviço</span><span class="sxs-lookup"><span data-stu-id="1a13f-140">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="1a13f-141">-Marca</span><span class="sxs-lookup"><span data-stu-id="1a13f-141">-Tag</span></span>
<span data-ttu-id="1a13f-142">Metadados específicos do aplicativo na forma de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="1a13f-142">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="1a13f-143">-Versão</span><span class="sxs-lookup"><span data-stu-id="1a13f-143">-Version</span></span>
<span data-ttu-id="1a13f-144">Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="1a13f-144">Server version.</span></span>

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

### <span data-ttu-id="1a13f-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1a13f-145">-Confirm</span></span>
<span data-ttu-id="1a13f-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a13f-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a13f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a13f-147">-WhatIf</span></span>
<span data-ttu-id="1a13f-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1a13f-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a13f-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1a13f-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a13f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a13f-150">CommonParameters</span></span>
<span data-ttu-id="1a13f-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a13f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a13f-152">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a13f-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a13f-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1a13f-153">INPUTS</span></span>

## <span data-ttu-id="1a13f-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1a13f-154">OUTPUTS</span></span>

### <span data-ttu-id="1a13f-155">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="1a13f-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="1a13f-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1a13f-156">NOTES</span></span>

<span data-ttu-id="1a13f-157">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1a13f-157">ALIASES</span></span>

## <span data-ttu-id="1a13f-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a13f-158">RELATED LINKS</span></span>

