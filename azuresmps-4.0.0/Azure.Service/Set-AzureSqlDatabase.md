---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 82F4DB8F-8DAF-40D2-8031-3EDBF5D08417
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6274d3851042c15791707807471ae1bc6a2733ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945865"
---
# <span data-ttu-id="75ccb-101">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="75ccb-101">Set-AzureSqlDatabase</span></span>

## <span data-ttu-id="75ccb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="75ccb-103">Define propriedades para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="75ccb-103">Sets properties for an Azure SQL Database.</span></span>

## <span data-ttu-id="75ccb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75ccb-104">SYNTAX</span></span>

### <span data-ttu-id="75ccb-105">ByNameWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="75ccb-105">ByNameWithConnectionContext</span></span>
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75ccb-106">ByObjectWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="75ccb-106">ByObjectWithConnectionContext</span></span>
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75ccb-107">ByNameWithServerName</span><span class="sxs-lookup"><span data-stu-id="75ccb-107">ByNameWithServerName</span></span>
```
Set-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75ccb-108">ByObjectWithServerName</span><span class="sxs-lookup"><span data-stu-id="75ccb-108">ByObjectWithServerName</span></span>
```
Set-AzureSqlDatabase -ServerName <String> -Database <Database> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75ccb-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75ccb-109">DESCRIPTION</span></span>
<span data-ttu-id="75ccb-110">O cmdlet **set-AzureSqlDatabase** define propriedades para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="75ccb-110">The **Set-AzureSqlDatabase** cmdlet sets properties for an Azure SQL Database.</span></span>
<span data-ttu-id="75ccb-111">Você pode especificar o banco de dados por nome ou passar um objeto do banco de dados SQL do Azure pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="75ccb-111">You can specify the database by name, or pass an Azure SQL Database object through the pipeline.</span></span>
<span data-ttu-id="75ccb-112">Você pode especificar o servidor por nome ou passar um contexto de conexão do servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="75ccb-112">You can specify the server by name, or pass an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="75ccb-113">Crie um contexto de conexão executando o cmdlet **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="75ccb-113">Create a connection context by running the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="75ccb-114">Se você especificar o servidor por nome, o cmdlet usará as informações atuais da assinatura do Azure para autenticar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="75ccb-114">If you specify the server by name, the cmdlet uses the current Azure subscription information to authenticate the request.</span></span>

## <span data-ttu-id="75ccb-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75ccb-115">EXAMPLES</span></span>

### <span data-ttu-id="75ccb-116">Exemplo 1: alterar o tamanho de um banco de dados usando um contexto de conexão</span><span class="sxs-lookup"><span data-stu-id="75ccb-116">Example 1: Change the size of a database by using a connection context</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ConnectionContext $Context -Database $Database01 -MaxSizeGB 20
```

<span data-ttu-id="75ccb-117">Este exemplo altera o tamanho do banco de dados chamado Database01 para 20 GB, no contexto de conexão do servidor de banco de dados SQL do Azure $Context.</span><span class="sxs-lookup"><span data-stu-id="75ccb-117">This example changes the size of the database named Database01 to 20 GB, in the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="75ccb-118">Exemplo 2: alterar o tamanho de um banco de dados usando um nome de servidor</span><span class="sxs-lookup"><span data-stu-id="75ccb-118">Example 2: Change the size of a database by using a server name</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ServerName "lpqd0zbr8y" -Database $Database01 -MaxSizeGB 20
```

<span data-ttu-id="75ccb-119">Este exemplo altera o tamanho do banco de dados chamado Database01 para 20 GB no servidor chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="75ccb-119">This example changes the size of the database named Database01 to 20 GB in the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="75ccb-120">OS</span><span class="sxs-lookup"><span data-stu-id="75ccb-120">PARAMETERS</span></span>

### <span data-ttu-id="75ccb-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="75ccb-121">-ConnectionContext</span></span>
<span data-ttu-id="75ccb-122">Especifica o contexto de conexão de um servidor.</span><span class="sxs-lookup"><span data-stu-id="75ccb-122">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75ccb-123">-Banco de dados</span><span class="sxs-lookup"><span data-stu-id="75ccb-123">-Database</span></span>
<span data-ttu-id="75ccb-124">Especifica um objeto que representa o banco de dados SQL do Azure que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="75ccb-124">Specifies an object that represents the Azure SQL Database that this cmdlet modifies.</span></span>

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75ccb-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="75ccb-125">-DatabaseName</span></span>
<span data-ttu-id="75ccb-126">Especifica o nome do banco de dados que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="75ccb-126">Specifies the name of the database that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ccb-127">-Edição</span><span class="sxs-lookup"><span data-stu-id="75ccb-127">-Edition</span></span>
<span data-ttu-id="75ccb-128">Especifica a nova edição para o banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="75ccb-128">Specifies the new edition for the Azure SQL Database.</span></span>
<span data-ttu-id="75ccb-129">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="75ccb-129">Valid values are:</span></span> 

- <span data-ttu-id="75ccb-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="75ccb-130">None</span></span>
- <span data-ttu-id="75ccb-131">Pela</span><span class="sxs-lookup"><span data-stu-id="75ccb-131">Web</span></span>
- <span data-ttu-id="75ccb-132">Empresarial</span><span class="sxs-lookup"><span data-stu-id="75ccb-132">Business</span></span>
- <span data-ttu-id="75ccb-133">Basic</span><span class="sxs-lookup"><span data-stu-id="75ccb-133">Basic</span></span>
- <span data-ttu-id="75ccb-134">Oficial</span><span class="sxs-lookup"><span data-stu-id="75ccb-134">Standard</span></span>
-  <span data-ttu-id="75ccb-135">Gratifica</span><span class="sxs-lookup"><span data-stu-id="75ccb-135">Premium</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ccb-136">-Force</span><span class="sxs-lookup"><span data-stu-id="75ccb-136">-Force</span></span>
<span data-ttu-id="75ccb-137">Permite a conclusão da ação sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="75ccb-137">Allows the action to complete without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ccb-138">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="75ccb-138">-MaxSizeBytes</span></span>
<span data-ttu-id="75ccb-139">Especifica o novo tamanho máximo para o banco de dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="75ccb-139">Specifies the new maximum size for the database in bytes.</span></span>
<span data-ttu-id="75ccb-140">Você pode especificar esse parâmetro ou o parâmetro *MaxSizeGB* .</span><span class="sxs-lookup"><span data-stu-id="75ccb-140">You can specify either this parameter or the *MaxSizeGB* parameter.</span></span>
<span data-ttu-id="75ccb-141">Consulte o parâmetro *MaxSizeGB* para obter valores aceitáveis com base na edição.</span><span class="sxs-lookup"><span data-stu-id="75ccb-141">See the *MaxSizeGB* parameter for acceptable values based on edition.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ccb-142">-MaxSizeGB</span><span class="sxs-lookup"><span data-stu-id="75ccb-142">-MaxSizeGB</span></span>
<span data-ttu-id="75ccb-143">Especifica o novo tamanho máximo para o banco de dados em gigabytes.</span><span class="sxs-lookup"><span data-stu-id="75ccb-143">Specifies the new maximum size for the database in gigabytes.</span></span>
<span data-ttu-id="75ccb-144">Você pode especificar esse parâmetro ou o parâmetro *MaxSizeBytes* .</span><span class="sxs-lookup"><span data-stu-id="75ccb-144">You can specify either this parameter or the *MaxSizeBytes* parameter.</span></span>
<span data-ttu-id="75ccb-145">Os valores aceitáveis são diferentes de acordo com a edição.</span><span class="sxs-lookup"><span data-stu-id="75ccb-145">The acceptable values differ based on edition.</span></span>

<span data-ttu-id="75ccb-146">Valores básicos da edição: 1 ou 2</span><span class="sxs-lookup"><span data-stu-id="75ccb-146">Basic Edition values: 1 or 2</span></span>

<span data-ttu-id="75ccb-147">Valores de edição padrão: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 ou 250</span><span class="sxs-lookup"><span data-stu-id="75ccb-147">Standard Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, or 250</span></span>

<span data-ttu-id="75ccb-148">Valores da edição Premium: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400 ou 500</span><span class="sxs-lookup"><span data-stu-id="75ccb-148">Premium Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, or 500</span></span>

<span data-ttu-id="75ccb-149">Valores da edição da Web: 1 ou 5</span><span class="sxs-lookup"><span data-stu-id="75ccb-149">Web Edition values: 1 or 5</span></span>

<span data-ttu-id="75ccb-150">Valores da edição para empresas: 10, 20, 30, 40, 50, 100 ou 150</span><span class="sxs-lookup"><span data-stu-id="75ccb-150">Business Edition values: 10, 20, 30, 40, 50, 100, or 150</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ccb-151">-NewDatabaseName</span><span class="sxs-lookup"><span data-stu-id="75ccb-151">-NewDatabaseName</span></span>
<span data-ttu-id="75ccb-152">Especifica o novo nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="75ccb-152">Specifies the new name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ccb-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75ccb-153">-PassThru</span></span>
<span data-ttu-id="75ccb-154">Retorna o banco de dados SQL do Azure atualizado.</span><span class="sxs-lookup"><span data-stu-id="75ccb-154">Returns the updated Azure SQL Database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ccb-155">-Perfil</span><span class="sxs-lookup"><span data-stu-id="75ccb-155">-Profile</span></span>
<span data-ttu-id="75ccb-156">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="75ccb-156">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="75ccb-157">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="75ccb-157">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ccb-158">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="75ccb-158">-ServerName</span></span>
<span data-ttu-id="75ccb-159">Especifica o nome do servidor que contém o banco de dados que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="75ccb-159">Specifies the name of the server that contains the database that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75ccb-160">-Missão-objeto</span><span class="sxs-lookup"><span data-stu-id="75ccb-160">-ServiceObjective</span></span>
<span data-ttu-id="75ccb-161">Especifica um objeto que representa o novo objetivo de serviço (nível de desempenho) para esse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="75ccb-161">Specifies an object representing the new service objective (performance level) for this database.</span></span>
<span data-ttu-id="75ccb-162">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="75ccb-162">Valid values are:</span></span> 

- <span data-ttu-id="75ccb-163">Básico: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c</span><span class="sxs-lookup"><span data-stu-id="75ccb-163">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span></span>
- <span data-ttu-id="75ccb-164">Padrão (S0): f1173c43-91bd-4AAA-973C-54e79e15235b</span><span class="sxs-lookup"><span data-stu-id="75ccb-164">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span></span>
- <span data-ttu-id="75ccb-165">Padrão (S1): 1b1ebd4d-D903-4baa-97f9-4ea675f5e928</span><span class="sxs-lookup"><span data-stu-id="75ccb-165">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span></span>
- <span data-ttu-id="75ccb-166">Padrão (S2): 455330e1-00CD-488b-b5fa-177c226f28b7</span><span class="sxs-lookup"><span data-stu-id="75ccb-166">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span></span>
- <span data-ttu-id="75ccb-167">\* Padrão (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40</span><span class="sxs-lookup"><span data-stu-id="75ccb-167">\*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span></span>
- <span data-ttu-id="75ccb-168">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="75ccb-168">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="75ccb-169">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span><span class="sxs-lookup"><span data-stu-id="75ccb-169">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span></span>
- <span data-ttu-id="75ccb-170">Premium (P3): a7c4c615-cfb1-464b-B252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="75ccb-170">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="75ccb-171">\* Padrão (S3) é parte da atualização de banco de dados do SQL V12 (prévia) mais recente.</span><span class="sxs-lookup"><span data-stu-id="75ccb-171">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="75ccb-172">Para obter mais informações, consulte o que há de novo na visualização do SQL banco de dados do Azure V12 https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .</span><span class="sxs-lookup"><span data-stu-id="75ccb-172">For more information, see What's New in the Azure SQL Database V12 Previewhttps://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/.</span></span>

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ccb-173">-Sincronizar</span><span class="sxs-lookup"><span data-stu-id="75ccb-173">-Sync</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ccb-174">-Confirme</span><span class="sxs-lookup"><span data-stu-id="75ccb-174">-Confirm</span></span>
<span data-ttu-id="75ccb-175">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75ccb-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ccb-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75ccb-176">-WhatIf</span></span>
<span data-ttu-id="75ccb-177">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="75ccb-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75ccb-178">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75ccb-178">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ccb-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75ccb-179">CommonParameters</span></span>
<span data-ttu-id="75ccb-180">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75ccb-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75ccb-181">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75ccb-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75ccb-182">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75ccb-182">INPUTS</span></span>

### <span data-ttu-id="75ccb-183">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="75ccb-183">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="75ccb-184">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75ccb-184">OUTPUTS</span></span>

### <span data-ttu-id="75ccb-185">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="75ccb-185">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="75ccb-186">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75ccb-186">NOTES</span></span>

## <span data-ttu-id="75ccb-187">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75ccb-187">RELATED LINKS</span></span>

[<span data-ttu-id="75ccb-188">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="75ccb-188">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="75ccb-189">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="75ccb-189">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="75ccb-190">Atualizar banco de dados</span><span class="sxs-lookup"><span data-stu-id="75ccb-190">Update Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505718.aspx)

[<span data-ttu-id="75ccb-191">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="75ccb-191">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="75ccb-192">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="75ccb-192">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="75ccb-193">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="75ccb-193">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="75ccb-194">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="75ccb-194">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


