---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F4FE79DB-B481-49BD-A33B-7C642A136890
online version: ''
schema: 2.0.0
ms.openlocfilehash: 588fcf73c258364e41117eed05c62de7eaa231e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945973"
---
# <span data-ttu-id="1017e-101">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1017e-101">New-AzureSqlDatabase</span></span>

## <span data-ttu-id="1017e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1017e-102">SYNOPSIS</span></span>
<span data-ttu-id="1017e-103">Cria um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="1017e-103">Creates an Azure SQL Database.</span></span>

## <span data-ttu-id="1017e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1017e-104">SYNTAX</span></span>

### <span data-ttu-id="1017e-105">ByConnectionContext</span><span class="sxs-lookup"><span data-stu-id="1017e-105">ByConnectionContext</span></span>
```
New-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-Collation <String>] [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1017e-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="1017e-106">ByServerName</span></span>
```
New-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Collation <String>]
 [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1017e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1017e-107">DESCRIPTION</span></span>
<span data-ttu-id="1017e-108">O cmdlet **New-AzureSqlDatabase** cria um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="1017e-108">The **New-AzureSqlDatabase** cmdlet creates an Azure SQL Database.</span></span>
<span data-ttu-id="1017e-109">Você pode especificar o servidor usando um contexto de conexão de servidor de banco de dados SQL do Azure que você cria usando o cmdlet **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="1017e-109">You can specify the server by using an Azure SQL Database server connection context that you create using the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="1017e-110">Ou, se você especificar o nome do servidor, o cmdlet usará as informações atuais da assinatura do Azure para autenticar a solicitação de acesso ao servidor.</span><span class="sxs-lookup"><span data-stu-id="1017e-110">Or, if you specify the server name, the cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

<span data-ttu-id="1017e-111">Quando você cria um novo banco de dados especificando um servidor de banco de dados SQL do Azure, o cmdlet **New-AzureSqlDatabase** cria um contexto de conexão temporário usando o nome do servidor especificado e as informações atuais da assinatura do Azure para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="1017e-111">When you create a new database by specifying an Azure SQL Database server, the **New-AzureSqlDatabase** cmdlet creates a temporary connection context using the specified server name and the current Azure subscription information to perform the operation.</span></span>

## <span data-ttu-id="1017e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1017e-112">EXAMPLES</span></span>

### <span data-ttu-id="1017e-113">Exemplo 1: criar um banco de dados</span><span class="sxs-lookup"><span data-stu-id="1017e-113">Example 1: Create a database</span></span>
```
PS C:\> $Database01 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="1017e-114">Esse comando cria um banco de dados SQL do Azure chamado Database1, para o contexto de conexão do servidor do banco de dados SQL do Azure $Context.</span><span class="sxs-lookup"><span data-stu-id="1017e-114">This command creates an Azure SQL Database named Database1, for the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="1017e-115">Exemplo 2: criar um banco de dados na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="1017e-115">Example 2: Create a database in the current subscription</span></span>
```
PS C:\> $Database01 = New-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="1017e-116">Este exemplo cria um banco de dados chamado Database1, no servidor de banco de dados SQL do Azure especificado chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="1017e-116">This example creates a database named Database1, in the specified Azure SQL Database server named lpqd0zbr8y.</span></span>
<span data-ttu-id="1017e-117">O cmdlet usa as informações de assinatura atuais do Azure para autenticar a solicitação de acesso ao servidor.</span><span class="sxs-lookup"><span data-stu-id="1017e-117">The cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

## <span data-ttu-id="1017e-118">OS</span><span class="sxs-lookup"><span data-stu-id="1017e-118">PARAMETERS</span></span>

### <span data-ttu-id="1017e-119">-Agrupamento</span><span class="sxs-lookup"><span data-stu-id="1017e-119">-Collation</span></span>
<span data-ttu-id="1017e-120">Especifica um agrupamento para o novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1017e-120">Specifies a collation for the new database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1017e-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="1017e-121">-ConnectionContext</span></span>
<span data-ttu-id="1017e-122">Especifica o contexto de conexão de um servidor em que esse cmdlet cria um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1017e-122">Specifies the connection context of a server where this cmdlet creates a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1017e-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1017e-123">-DatabaseName</span></span>
<span data-ttu-id="1017e-124">Especifica o nome do novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1017e-124">Specifies the name of the new database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1017e-125">-Edição</span><span class="sxs-lookup"><span data-stu-id="1017e-125">-Edition</span></span>
<span data-ttu-id="1017e-126">Especifica a edição para o novo banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="1017e-126">Specifies the edition for the new Azure SQL Database.</span></span>
<span data-ttu-id="1017e-127">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="1017e-127">Valid values are:</span></span> 

- <span data-ttu-id="1017e-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1017e-128">None</span></span>
- <span data-ttu-id="1017e-129">Pela</span><span class="sxs-lookup"><span data-stu-id="1017e-129">Web</span></span>
- <span data-ttu-id="1017e-130">Empresarial</span><span class="sxs-lookup"><span data-stu-id="1017e-130">Business</span></span>
- <span data-ttu-id="1017e-131">Basic</span><span class="sxs-lookup"><span data-stu-id="1017e-131">Basic</span></span>
- <span data-ttu-id="1017e-132">Oficial</span><span class="sxs-lookup"><span data-stu-id="1017e-132">Standard</span></span>
-  <span data-ttu-id="1017e-133">Gratifica</span><span class="sxs-lookup"><span data-stu-id="1017e-133">Premium</span></span>

<span data-ttu-id="1017e-134">O valor padrão é Web.</span><span class="sxs-lookup"><span data-stu-id="1017e-134">The default value is Web.</span></span>

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

### <span data-ttu-id="1017e-135">-Force</span><span class="sxs-lookup"><span data-stu-id="1017e-135">-Force</span></span>
<span data-ttu-id="1017e-136">Permite a conclusão da ação sem solicitar confirmação ao usuário.</span><span class="sxs-lookup"><span data-stu-id="1017e-136">Allows the action to complete without prompting the user for confirmation.</span></span>

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

### <span data-ttu-id="1017e-137">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="1017e-137">-MaxSizeBytes</span></span>
<span data-ttu-id="1017e-138">Especifica o tamanho máximo do banco de dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="1017e-138">Specifies the maximum size of the database in bytes.</span></span>
<span data-ttu-id="1017e-139">Você pode especificar esse parâmetro ou o parâmetro *MaxSizeGB* .</span><span class="sxs-lookup"><span data-stu-id="1017e-139">You can specify either this parameter or the *MaxSizeGB* parameter.</span></span>
<span data-ttu-id="1017e-140">Consulte a descrição do parâmetro *MaxSizeGB* para obter os valores aceitáveis com base na edição.</span><span class="sxs-lookup"><span data-stu-id="1017e-140">See the *MaxSizeGB* parameter description for acceptable values based on edition.</span></span>

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

### <span data-ttu-id="1017e-141">-MaxSizeGB</span><span class="sxs-lookup"><span data-stu-id="1017e-141">-MaxSizeGB</span></span>
<span data-ttu-id="1017e-142">Especifica o tamanho máximo do banco de dados em gigabytes.</span><span class="sxs-lookup"><span data-stu-id="1017e-142">Specifies the maximum size of the database in gigabytes.</span></span>
<span data-ttu-id="1017e-143">Você pode especificar esse parâmetro ou o parâmetro *MaxSizeBytes* .</span><span class="sxs-lookup"><span data-stu-id="1017e-143">You can specify either this parameter or the *MaxSizeBytes* parameter.</span></span>
<span data-ttu-id="1017e-144">Os valores aceitáveis são diferentes de acordo com a edição.</span><span class="sxs-lookup"><span data-stu-id="1017e-144">The acceptable values differ based on edition.</span></span>

<span data-ttu-id="1017e-145">Valores básicos da edição: 1 ou 2</span><span class="sxs-lookup"><span data-stu-id="1017e-145">Basic Edition values: 1 or 2</span></span>

<span data-ttu-id="1017e-146">Valores de edição padrão: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 ou 250</span><span class="sxs-lookup"><span data-stu-id="1017e-146">Standard Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, or 250</span></span>

<span data-ttu-id="1017e-147">Valores da edição Premium: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400 ou 500</span><span class="sxs-lookup"><span data-stu-id="1017e-147">Premium Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, or 500</span></span>

<span data-ttu-id="1017e-148">Valores da edição da Web: 1 ou 5</span><span class="sxs-lookup"><span data-stu-id="1017e-148">Web Edition values: 1 or 5</span></span>

<span data-ttu-id="1017e-149">Valores da edição para empresas: 10, 20, 30, 40, 50, 100 ou 150</span><span class="sxs-lookup"><span data-stu-id="1017e-149">Business Edition values: 10, 20, 30, 40, 50, 100, or 150</span></span>

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

### <span data-ttu-id="1017e-150">-Perfil</span><span class="sxs-lookup"><span data-stu-id="1017e-150">-Profile</span></span>
<span data-ttu-id="1017e-151">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="1017e-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1017e-152">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="1017e-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1017e-153">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="1017e-153">-ServerName</span></span>
<span data-ttu-id="1017e-154">Especifica o nome do servidor de banco de dados SQL do Azure que deve conter o novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1017e-154">Specifies the name of the Azure SQL Database server to contain the new database.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1017e-155">-Missão-objeto</span><span class="sxs-lookup"><span data-stu-id="1017e-155">-ServiceObjective</span></span>
<span data-ttu-id="1017e-156">Especifica um objeto que representa o novo objetivo de serviço (nível de desempenho) deste banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1017e-156">Specifies an object that represent the new service objective (performance level) for this database.</span></span>
<span data-ttu-id="1017e-157">Esse valor representa o nível dos recursos atribuídos a esse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1017e-157">This value represents the level of resources assigned to this database.</span></span>
<span data-ttu-id="1017e-158">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="1017e-158">Valid values are:</span></span> 

<span data-ttu-id="1017e-159">Básico: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c padrão (S0): f1173c43-91bd-4AAA-973C-54e79e15235b padrão (S1): 1b1ebd4d-D903-4baa-97f9-4ea675f5e928 padrão (S2): 455330e1-00CD-488b-b5fa-177c226f28b7 \* padrão (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464b-B252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="1017e-159">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928 Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 \*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="1017e-160">\* Padrão (S3) é parte da atualização de banco de dados do SQL V12 (prévia) mais recente.</span><span class="sxs-lookup"><span data-stu-id="1017e-160">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="1017e-161">Para obter mais informações, consulte o que há de novo na visualização do SQL banco de dados do Azure V12 https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .</span><span class="sxs-lookup"><span data-stu-id="1017e-161">For more information, see What's New in the Azure SQL Database V12 Previewhttps://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/.</span></span>

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

### <span data-ttu-id="1017e-162">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1017e-162">-Confirm</span></span>
<span data-ttu-id="1017e-163">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1017e-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1017e-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1017e-164">-WhatIf</span></span>
<span data-ttu-id="1017e-165">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1017e-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1017e-166">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1017e-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1017e-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1017e-167">CommonParameters</span></span>
<span data-ttu-id="1017e-168">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1017e-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1017e-169">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1017e-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1017e-170">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1017e-170">INPUTS</span></span>

## <span data-ttu-id="1017e-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1017e-171">OUTPUTS</span></span>

### <span data-ttu-id="1017e-172">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="1017e-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="1017e-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1017e-173">NOTES</span></span>
* <span data-ttu-id="1017e-174">Para excluir um banco de dados que foi criado por **New-AzureSqlDatabase** , use o cmdlet Remove-AzureSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="1017e-174">To delete a database that was created by **New-AzureSqlDatabase** , use the Remove-AzureSqlDatabase cmdlet.</span></span>

## <span data-ttu-id="1017e-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1017e-175">RELATED LINKS</span></span>

[<span data-ttu-id="1017e-176">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="1017e-176">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="1017e-177">Criar banco de dados</span><span class="sxs-lookup"><span data-stu-id="1017e-177">Create Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505701.aspx)

[<span data-ttu-id="1017e-178">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="1017e-178">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="1017e-179">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1017e-179">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="1017e-180">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="1017e-180">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="1017e-181">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1017e-181">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="1017e-182">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1017e-182">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


