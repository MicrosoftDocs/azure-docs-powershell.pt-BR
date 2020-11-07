---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
ms.openlocfilehash: 3b9ca8c4aa236b690bbe0dfe09c35f0ebc8a5b22
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948174"
---
# <span data-ttu-id="3dc42-101">New-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="3dc42-101">New-AzMySqlServer</span></span>

## <span data-ttu-id="3dc42-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3dc42-102">SYNOPSIS</span></span>
<span data-ttu-id="3dc42-103">Cria um novo servidor.</span><span class="sxs-lookup"><span data-stu-id="3dc42-103">Creates a new server.</span></span>

## <span data-ttu-id="3dc42-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3dc42-104">SYNTAX</span></span>

```
New-AzMySqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3dc42-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3dc42-105">DESCRIPTION</span></span>
<span data-ttu-id="3dc42-106">Cria um novo servidor.</span><span class="sxs-lookup"><span data-stu-id="3dc42-106">Creates a new server.</span></span>

## <span data-ttu-id="3dc42-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3dc42-107">EXAMPLES</span></span>

### <span data-ttu-id="3dc42-108">Exemplo 1: criar um novo servidor MySql</span><span class="sxs-lookup"><span data-stu-id="3dc42-108">Example 1: Create a new MySql server</span></span>
```powershell
PS C:\> New-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Location eastus -AdministratorUser mysql_test -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="3dc42-109">Esses cmdlets criam um novo servidor MySql.</span><span class="sxs-lookup"><span data-stu-id="3dc42-109">These cmdlets create a new MySql server.</span></span>

## <span data-ttu-id="3dc42-110">OS</span><span class="sxs-lookup"><span data-stu-id="3dc42-110">PARAMETERS</span></span>

### <span data-ttu-id="3dc42-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="3dc42-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="3dc42-112">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="3dc42-112">The location the resource resides in.</span></span>

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

### <span data-ttu-id="3dc42-113">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="3dc42-113">-AdministratorUserName</span></span>
<span data-ttu-id="3dc42-114">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="3dc42-114">The location the resource resides in.</span></span>

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

### <span data-ttu-id="3dc42-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3dc42-115">-AsJob</span></span>
<span data-ttu-id="3dc42-116">Executar o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="3dc42-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="3dc42-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="3dc42-117">-BackupRetentionDay</span></span>
<span data-ttu-id="3dc42-118">Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="3dc42-118">Backup retention days for the server.</span></span>
<span data-ttu-id="3dc42-119">A contagem de dias está entre 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="3dc42-119">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="3dc42-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dc42-120">-DefaultProfile</span></span>
<span data-ttu-id="3dc42-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc42-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dc42-122">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="3dc42-122">-GeoRedundantBackup</span></span>
<span data-ttu-id="3dc42-123">Habilite a redundância geográfica ou não para o backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="3dc42-123">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc42-124">-Local</span><span class="sxs-lookup"><span data-stu-id="3dc42-124">-Location</span></span>
<span data-ttu-id="3dc42-125">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="3dc42-125">The location the resource resides in.</span></span>

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

### <span data-ttu-id="3dc42-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="3dc42-126">-Name</span></span>
<span data-ttu-id="3dc42-127">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="3dc42-127">The name of the server.</span></span>

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

### <span data-ttu-id="3dc42-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3dc42-128">-NoWait</span></span>
<span data-ttu-id="3dc42-129">Executar o comando de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="3dc42-129">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="3dc42-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dc42-130">-ResourceGroupName</span></span>
<span data-ttu-id="3dc42-131">O nome do grupo de recursos que contém o recurso, você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="3dc42-131">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3dc42-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="3dc42-132">-Sku</span></span>
<span data-ttu-id="3dc42-133">O nome do SKU, geralmente, a camada + família + núcleos, por exemplo B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="3dc42-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="3dc42-134">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="3dc42-134">-SslEnforcement</span></span>
<span data-ttu-id="3dc42-135">Habilite a imposição de SSL ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="3dc42-135">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc42-136">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="3dc42-136">-StorageAutogrow</span></span>
<span data-ttu-id="3dc42-137">Habilite o aumento automático do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3dc42-137">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc42-138">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="3dc42-138">-StorageInMb</span></span>
<span data-ttu-id="3dc42-139">Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="3dc42-139">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="3dc42-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3dc42-140">-SubscriptionId</span></span>
<span data-ttu-id="3dc42-141">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc42-141">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="3dc42-142">-Marca</span><span class="sxs-lookup"><span data-stu-id="3dc42-142">-Tag</span></span>
<span data-ttu-id="3dc42-143">Metadados específicos do aplicativo na forma de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="3dc42-143">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="3dc42-144">-Versão</span><span class="sxs-lookup"><span data-stu-id="3dc42-144">-Version</span></span>
<span data-ttu-id="3dc42-145">Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="3dc42-145">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc42-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3dc42-146">-Confirm</span></span>
<span data-ttu-id="3dc42-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dc42-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dc42-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dc42-148">-WhatIf</span></span>
<span data-ttu-id="3dc42-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3dc42-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dc42-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3dc42-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dc42-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc42-151">CommonParameters</span></span>
<span data-ttu-id="3dc42-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dc42-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc42-153">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3dc42-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc42-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3dc42-154">INPUTS</span></span>

## <span data-ttu-id="3dc42-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3dc42-155">OUTPUTS</span></span>

### <span data-ttu-id="3dc42-156">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="3dc42-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="3dc42-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3dc42-157">NOTES</span></span>

<span data-ttu-id="3dc42-158">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3dc42-158">ALIASES</span></span>

## <span data-ttu-id="3dc42-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3dc42-159">RELATED LINKS</span></span>

