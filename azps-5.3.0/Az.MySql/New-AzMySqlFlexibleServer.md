---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
ms.openlocfilehash: 1dbd998cdafc92de6541e25c2cb2bf6477e2d5b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433517"
---
# <span data-ttu-id="55996-101">New-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="55996-101">New-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="55996-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55996-102">SYNOPSIS</span></span>
<span data-ttu-id="55996-103">Cria um novo servidor flexível do MySQL</span><span class="sxs-lookup"><span data-stu-id="55996-103">Creates a new MySQL flexible server</span></span>

## <span data-ttu-id="55996-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55996-104">SYNTAX</span></span>

```
New-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> -AdministratorUserName <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-Location <String>] [-Sku <String>] [-SkuTier <String>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="55996-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55996-105">DESCRIPTION</span></span>
<span data-ttu-id="55996-106">Cria um novo servidor.</span><span class="sxs-lookup"><span data-stu-id="55996-106">Creates a new server.</span></span>

## <span data-ttu-id="55996-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55996-107">EXAMPLES</span></span>

### <span data-ttu-id="55996-108">Exemplo 1: criar um novo servidor flexível do MySql</span><span class="sxs-lookup"><span data-stu-id="55996-108">Example 1: Create a new MySql flexible server</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-Location eastus -AdministratorUserName mysqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName         SkuTier     
----            -------- ------------------ ------- ----------------------- ------------    -------------        
mysql-test      West US 2   mysqltest    5.7      10240                  Standard_B1ms   Burstable
```



### <span data-ttu-id="55996-109">Exemplo 2: criar um novo servidor flexível do MySql com a configuração padrão</span><span class="sxs-lookup"><span data-stu-id="55996-109">Example 2: Create a new MySql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-AdministratorUserName mysqltest -AdministratorLoginPassword $password

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName         SkuTier     
----            -------- ------------------ ------- ----------------------- ------------    -------------        
mysql-test      West US 2   mysqltest    5.7      131072                  Standard_B1ms   Burstable
```

<span data-ttu-id="55996-110">Crie um servidor MySql com valores padrão.</span><span class="sxs-lookup"><span data-stu-id="55996-110">Create MySql server with default values.</span></span>
<span data-ttu-id="55996-111">Os valores padrão de Location são West US 2, SKU é Standard_B1ms, o nível de SKU é intermitente e o tamanho do armazenamento é 10GiB.</span><span class="sxs-lookup"><span data-stu-id="55996-111">The default values of location is West US 2, Sku is Standard_B1ms, Sku tier is Burstable, and storage size is 10GiB.</span></span>

## <span data-ttu-id="55996-112">OS</span><span class="sxs-lookup"><span data-stu-id="55996-112">PARAMETERS</span></span>

### <span data-ttu-id="55996-113">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="55996-113">-AdministratorLoginPassword</span></span>
<span data-ttu-id="55996-114">A senha do administrador.</span><span class="sxs-lookup"><span data-stu-id="55996-114">The password of the administrator.</span></span>
<span data-ttu-id="55996-115">No mínimo 8 caracteres e no máximo 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="55996-115">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="55996-116">A senha deve conter caracteres de três das seguintes categorias: letras maiúsculas em inglês, letras minúsculas, números e caracteres não alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="55996-116">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="55996-117">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="55996-117">-AdministratorUserName</span></span>
<span data-ttu-id="55996-118">Nome de usuário de administrador do servidor.</span><span class="sxs-lookup"><span data-stu-id="55996-118">Administrator username for the server.</span></span>
<span data-ttu-id="55996-119">Uma vez definido, ele não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="55996-119">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="55996-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55996-120">-AsJob</span></span>
<span data-ttu-id="55996-121">Executar o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="55996-121">Run the command as a job.</span></span>

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

### <span data-ttu-id="55996-122">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="55996-122">-BackupRetentionDay</span></span>
<span data-ttu-id="55996-123">Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="55996-123">Backup retention days for the server.</span></span>
<span data-ttu-id="55996-124">A contagem de dias está entre 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="55996-124">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="55996-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55996-125">-DefaultProfile</span></span>
<span data-ttu-id="55996-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55996-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55996-127">-Local</span><span class="sxs-lookup"><span data-stu-id="55996-127">-Location</span></span>
<span data-ttu-id="55996-128">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="55996-128">The location the resource resides in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55996-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="55996-129">-Name</span></span>
<span data-ttu-id="55996-130">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="55996-130">The name of the server.</span></span>

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

### <span data-ttu-id="55996-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="55996-131">-NoWait</span></span>
<span data-ttu-id="55996-132">Executar o comando de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="55996-132">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="55996-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55996-133">-ResourceGroupName</span></span>
<span data-ttu-id="55996-134">O nome do grupo de recursos que contém o recurso, você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="55996-134">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="55996-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="55996-135">-Sku</span></span>
<span data-ttu-id="55996-136">O nome do SKU, geralmente, a camada + família + núcleos, por exemplo Standard_B1ms Standard_D2ds_v4.</span><span class="sxs-lookup"><span data-stu-id="55996-136">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55996-137">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="55996-137">-SkuTier</span></span>
<span data-ttu-id="55996-138">Camada de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="55996-138">Compute tier of the server.</span></span>
<span data-ttu-id="55996-139">Valores aceitos: estourável, GeneralPurpose, memória otimizada.</span><span class="sxs-lookup"><span data-stu-id="55996-139">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="55996-140">Padrão: intermitente.</span><span class="sxs-lookup"><span data-stu-id="55996-140">Default: Burstable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55996-141">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="55996-141">-StorageInMb</span></span>
<span data-ttu-id="55996-142">Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="55996-142">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="55996-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55996-143">-SubscriptionId</span></span>
<span data-ttu-id="55996-144">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="55996-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="55996-145">-Marca</span><span class="sxs-lookup"><span data-stu-id="55996-145">-Tag</span></span>
<span data-ttu-id="55996-146">Metadados específicos do aplicativo na forma de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="55996-146">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="55996-147">-Versão</span><span class="sxs-lookup"><span data-stu-id="55996-147">-Version</span></span>
<span data-ttu-id="55996-148">Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="55996-148">Server version.</span></span>

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

### <span data-ttu-id="55996-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="55996-149">-Confirm</span></span>
<span data-ttu-id="55996-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55996-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55996-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55996-151">-WhatIf</span></span>
<span data-ttu-id="55996-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="55996-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55996-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55996-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55996-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55996-154">CommonParameters</span></span>
<span data-ttu-id="55996-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55996-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55996-156">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55996-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55996-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55996-157">INPUTS</span></span>

## <span data-ttu-id="55996-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55996-158">OUTPUTS</span></span>

### <span data-ttu-id="55996-159">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20200701Preview. IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="55996-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="55996-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55996-160">NOTES</span></span>

<span data-ttu-id="55996-161">ALIASES</span><span class="sxs-lookup"><span data-stu-id="55996-161">ALIASES</span></span>

## <span data-ttu-id="55996-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55996-162">RELATED LINKS</span></span>

