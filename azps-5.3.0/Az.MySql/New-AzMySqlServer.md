---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
ms.openlocfilehash: 683ca81587ff7c71f1406eb7a4accef37aac794d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427091"
---
# <span data-ttu-id="02f44-101">New-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="02f44-101">New-AzMySqlServer</span></span>

## <span data-ttu-id="02f44-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02f44-102">SYNOPSIS</span></span>
<span data-ttu-id="02f44-103">Cria um novo servidor.</span><span class="sxs-lookup"><span data-stu-id="02f44-103">Creates a new server.</span></span>

## <span data-ttu-id="02f44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02f44-104">SYNTAX</span></span>

```
New-AzMySqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="02f44-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02f44-105">DESCRIPTION</span></span>
<span data-ttu-id="02f44-106">Cria um novo servidor.</span><span class="sxs-lookup"><span data-stu-id="02f44-106">Creates a new server.</span></span>

## <span data-ttu-id="02f44-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02f44-107">EXAMPLES</span></span>

### <span data-ttu-id="02f44-108">Exemplo 1: criar um novo servidor MySql</span><span class="sxs-lookup"><span data-stu-id="02f44-108">Example 1: Create a new MySql server</span></span>
```powershell
PS C:\> New-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Location eastus -AdministratorUser mysql_test -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="02f44-109">Esses cmdlets criam um novo servidor MySql.</span><span class="sxs-lookup"><span data-stu-id="02f44-109">These cmdlets create a new MySql server.</span></span>

## <span data-ttu-id="02f44-110">OS</span><span class="sxs-lookup"><span data-stu-id="02f44-110">PARAMETERS</span></span>

### <span data-ttu-id="02f44-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="02f44-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="02f44-112">A senha do administrador.</span><span class="sxs-lookup"><span data-stu-id="02f44-112">The password of the administrator.</span></span>
<span data-ttu-id="02f44-113">No mínimo 8 caracteres e no máximo 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="02f44-113">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="02f44-114">A senha deve conter caracteres de três das seguintes categorias: letras maiúsculas em inglês, letras minúsculas, números e caracteres não alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="02f44-114">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="02f44-115">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="02f44-115">-AdministratorUserName</span></span>
<span data-ttu-id="02f44-116">Nome de usuário de administrador do servidor.</span><span class="sxs-lookup"><span data-stu-id="02f44-116">Administrator username for the server.</span></span>
<span data-ttu-id="02f44-117">Uma vez definido, ele não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="02f44-117">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="02f44-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02f44-118">-AsJob</span></span>
<span data-ttu-id="02f44-119">Executar o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="02f44-119">Run the command as a job.</span></span>

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

### <span data-ttu-id="02f44-120">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="02f44-120">-BackupRetentionDay</span></span>
<span data-ttu-id="02f44-121">Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="02f44-121">Backup retention days for the server.</span></span>
<span data-ttu-id="02f44-122">A contagem de dias está entre 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="02f44-122">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="02f44-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02f44-123">-DefaultProfile</span></span>
<span data-ttu-id="02f44-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02f44-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02f44-125">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="02f44-125">-GeoRedundantBackup</span></span>
<span data-ttu-id="02f44-126">Habilite a redundância geográfica ou não para o backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="02f44-126">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="02f44-127">-Local</span><span class="sxs-lookup"><span data-stu-id="02f44-127">-Location</span></span>
<span data-ttu-id="02f44-128">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="02f44-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="02f44-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="02f44-129">-Name</span></span>
<span data-ttu-id="02f44-130">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="02f44-130">The name of the server.</span></span>

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

### <span data-ttu-id="02f44-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="02f44-131">-NoWait</span></span>
<span data-ttu-id="02f44-132">Executar o comando de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="02f44-132">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="02f44-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02f44-133">-ResourceGroupName</span></span>
<span data-ttu-id="02f44-134">O nome do grupo de recursos que contém o recurso, você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="02f44-134">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="02f44-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="02f44-135">-Sku</span></span>
<span data-ttu-id="02f44-136">O nome do SKU, geralmente, a camada + família + núcleos, por exemplo B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="02f44-136">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="02f44-137">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="02f44-137">-SslEnforcement</span></span>
<span data-ttu-id="02f44-138">Habilite a imposição de SSL ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="02f44-138">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="02f44-139">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="02f44-139">-StorageAutogrow</span></span>
<span data-ttu-id="02f44-140">Habilite o aumento automático do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="02f44-140">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="02f44-141">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="02f44-141">-StorageInMb</span></span>
<span data-ttu-id="02f44-142">Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="02f44-142">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="02f44-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02f44-143">-SubscriptionId</span></span>
<span data-ttu-id="02f44-144">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="02f44-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="02f44-145">-Marca</span><span class="sxs-lookup"><span data-stu-id="02f44-145">-Tag</span></span>
<span data-ttu-id="02f44-146">Metadados específicos do aplicativo na forma de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="02f44-146">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="02f44-147">-Versão</span><span class="sxs-lookup"><span data-stu-id="02f44-147">-Version</span></span>
<span data-ttu-id="02f44-148">Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="02f44-148">Server version.</span></span>

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

### <span data-ttu-id="02f44-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="02f44-149">-Confirm</span></span>
<span data-ttu-id="02f44-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02f44-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02f44-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02f44-151">-WhatIf</span></span>
<span data-ttu-id="02f44-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="02f44-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02f44-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="02f44-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02f44-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02f44-154">CommonParameters</span></span>
<span data-ttu-id="02f44-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02f44-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02f44-156">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02f44-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02f44-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02f44-157">INPUTS</span></span>

## <span data-ttu-id="02f44-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02f44-158">OUTPUTS</span></span>

### <span data-ttu-id="02f44-159">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="02f44-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="02f44-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02f44-160">NOTES</span></span>

<span data-ttu-id="02f44-161">ALIASES</span><span class="sxs-lookup"><span data-stu-id="02f44-161">ALIASES</span></span>

## <span data-ttu-id="02f44-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02f44-162">RELATED LINKS</span></span>

