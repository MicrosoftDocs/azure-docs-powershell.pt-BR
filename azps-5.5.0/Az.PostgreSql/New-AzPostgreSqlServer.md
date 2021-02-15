---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
ms.openlocfilehash: ed7b8e9db63adb92af6aaae1f780fd1aca7f0022
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114999"
---
# <span data-ttu-id="ca344-101">New-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="ca344-101">New-AzPostgreSqlServer</span></span>

## <span data-ttu-id="ca344-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca344-102">SYNOPSIS</span></span>
<span data-ttu-id="ca344-103">Cria um novo servidor.</span><span class="sxs-lookup"><span data-stu-id="ca344-103">Creates a new server.</span></span>

## <span data-ttu-id="ca344-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca344-104">SYNTAX</span></span>

```
New-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-Version <ServerVersion>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ca344-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca344-105">DESCRIPTION</span></span>
<span data-ttu-id="ca344-106">Cria um novo servidor.</span><span class="sxs-lookup"><span data-stu-id="ca344-106">Creates a new server.</span></span>

## <span data-ttu-id="ca344-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ca344-107">EXAMPLES</span></span>

### <span data-ttu-id="ca344-108">Exemplo 1: Criar um novo servidor PostgreSql</span><span class="sxs-lookup"><span data-stu-id="ca344-108">Example 1: Create a new PostgreSql server</span></span>
```powershell
PS C:\> New-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -Location eastus -AdministratorUserName pwsh -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="ca344-109">Esses cmdlets criam um novo servidor PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="ca344-109">These cmdlets create a new PostgreSql server.</span></span>

## <span data-ttu-id="ca344-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca344-110">PARAMETERS</span></span>

### <span data-ttu-id="ca344-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="ca344-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="ca344-112">A senha do administrador.</span><span class="sxs-lookup"><span data-stu-id="ca344-112">The password of the administrator.</span></span>
<span data-ttu-id="ca344-113">Mínimo de 8 caracteres e máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ca344-113">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="ca344-114">A senha deve conter caracteres de três das seguintes categorias: letras maiúsculas em inglês, letras minúsculas em inglês, números e caracteres não alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="ca344-114">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="ca344-115">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="ca344-115">-AdministratorUserName</span></span>
<span data-ttu-id="ca344-116">Nome de usuário do administrador para o servidor.</span><span class="sxs-lookup"><span data-stu-id="ca344-116">Administrator username for the server.</span></span>
<span data-ttu-id="ca344-117">Depois de definido, ele não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="ca344-117">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="ca344-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca344-118">-AsJob</span></span>
<span data-ttu-id="ca344-119">Execute o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="ca344-119">Run the command as a job.</span></span>

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

### <span data-ttu-id="ca344-120">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="ca344-120">-BackupRetentionDay</span></span>
<span data-ttu-id="ca344-121">Backup de dias de retenção para o servidor.</span><span class="sxs-lookup"><span data-stu-id="ca344-121">Backup retention days for the server.</span></span>
<span data-ttu-id="ca344-122">A contagem de dias está entre 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="ca344-122">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="ca344-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca344-123">-DefaultProfile</span></span>
<span data-ttu-id="ca344-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca344-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca344-125">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="ca344-125">-GeoRedundantBackup</span></span>
<span data-ttu-id="ca344-126">Habilitar a redundância geográfica ou não para backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="ca344-126">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca344-127">-Local</span><span class="sxs-lookup"><span data-stu-id="ca344-127">-Location</span></span>
<span data-ttu-id="ca344-128">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="ca344-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="ca344-129">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="ca344-129">-MinimalTlsVersion</span></span>
<span data-ttu-id="ca344-130">Defina a versão TLS mínima para conexões com o servidor quando a SSL estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="ca344-130">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="ca344-131">O padrão é valores TLSEnforcementDisabled.accepted: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span><span class="sxs-lookup"><span data-stu-id="ca344-131">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca344-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca344-132">-Name</span></span>
<span data-ttu-id="ca344-133">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="ca344-133">The name of the server.</span></span>

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

### <span data-ttu-id="ca344-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ca344-134">-NoWait</span></span>
<span data-ttu-id="ca344-135">Execute o comando assíncrona.</span><span class="sxs-lookup"><span data-stu-id="ca344-135">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="ca344-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca344-136">-ResourceGroupName</span></span>
<span data-ttu-id="ca344-137">O nome do grupo de recursos que contém o recurso, Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="ca344-137">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ca344-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="ca344-138">-Sku</span></span>
<span data-ttu-id="ca344-139">O nome da sKU, normalmente, tier + família + cores, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="ca344-139">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="ca344-140">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="ca344-140">-SslEnforcement</span></span>
<span data-ttu-id="ca344-141">Habilita a imposição ssl ou não quando se conecta ao servidor.</span><span class="sxs-lookup"><span data-stu-id="ca344-141">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca344-142">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="ca344-142">-StorageAutogrow</span></span>
<span data-ttu-id="ca344-143">Habilitar o Crescimento Automático do Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ca344-143">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca344-144">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="ca344-144">-StorageInMb</span></span>
<span data-ttu-id="ca344-145">Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="ca344-145">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="ca344-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca344-146">-SubscriptionId</span></span>
<span data-ttu-id="ca344-147">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca344-147">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="ca344-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="ca344-148">-Tag</span></span>
<span data-ttu-id="ca344-149">Metadados específicos do aplicativo na forma de pares de valor-chave.</span><span class="sxs-lookup"><span data-stu-id="ca344-149">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="ca344-150">-Versão</span><span class="sxs-lookup"><span data-stu-id="ca344-150">-Version</span></span>
<span data-ttu-id="ca344-151">Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="ca344-151">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca344-152">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ca344-152">-Confirm</span></span>
<span data-ttu-id="ca344-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca344-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca344-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca344-154">-WhatIf</span></span>
<span data-ttu-id="ca344-155">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ca344-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca344-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca344-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca344-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca344-157">CommonParameters</span></span>
<span data-ttu-id="ca344-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca344-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca344-159">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca344-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca344-160">Entradas</span><span class="sxs-lookup"><span data-stu-id="ca344-160">INPUTS</span></span>

## <span data-ttu-id="ca344-161">Saídas</span><span class="sxs-lookup"><span data-stu-id="ca344-161">OUTPUTS</span></span>

### <span data-ttu-id="ca344-162">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="ca344-162">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="ca344-163">Notas</span><span class="sxs-lookup"><span data-stu-id="ca344-163">NOTES</span></span>

<span data-ttu-id="ca344-164">Aliases</span><span class="sxs-lookup"><span data-stu-id="ca344-164">ALIASES</span></span>

## <span data-ttu-id="ca344-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca344-165">RELATED LINKS</span></span>

