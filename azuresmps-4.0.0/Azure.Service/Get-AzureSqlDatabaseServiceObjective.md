---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A2C22A8A-EF50-4BE3-82DF-5ED6F69C00CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 457775a74fb7921a3c8b6b5e635bd7df7e704faa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945568"
---
# <span data-ttu-id="1e6dd-101">Get-AzureSqlDatabaseServiceObjective</span><span class="sxs-lookup"><span data-stu-id="1e6dd-101">Get-AzureSqlDatabaseServiceObjective</span></span>

## <span data-ttu-id="1e6dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e6dd-102">SYNOPSIS</span></span>
<span data-ttu-id="1e6dd-103">Obtém objetivos de serviço para um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="1e6dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e6dd-104">SYNTAX</span></span>

### <span data-ttu-id="1e6dd-105">ByConnectionContext (padrão)</span><span class="sxs-lookup"><span data-stu-id="1e6dd-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabaseServiceObjective -Context <IServerDataServiceContext>
 [-ServiceObjective <ServiceObjective>] [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e6dd-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="1e6dd-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseServiceObjective -ServerName <String> [-ServiceObjective <ServiceObjective>]
 [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1e6dd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1e6dd-107">DESCRIPTION</span></span>
<span data-ttu-id="1e6dd-108">O cmdlet **Get-AzureSqlDatabaseServiceObjective** Obtém objetivos de serviço para um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-108">The **Get-AzureSqlDatabaseServiceObjective** cmdlet gets service objectives for an Azure SQL Database server.</span></span>
<span data-ttu-id="1e6dd-109">Os objetivos do serviço são chamados de níveis de desempenho.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-109">Service objectives are referred to as performance levels.</span></span>
<span data-ttu-id="1e6dd-110">Se você não especificar um objetivo de serviço, esse cmdlet retornará todos os objetivos de serviço válidos para o servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-110">If you do not specify a service objective, this cmdlet returns all valid service objectives for the specified server.</span></span>

<span data-ttu-id="1e6dd-111">Este cmdlet se aplica a camadas de serviço básicas, padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-111">This cmdlet applies to Basic, Standard, and Premium service tiers.</span></span>

## <span data-ttu-id="1e6dd-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e6dd-112">EXAMPLES</span></span>

### <span data-ttu-id="1e6dd-113">Exemplo 1: obter todos os objetivos do serviço usando um contexto de conexão</span><span class="sxs-lookup"><span data-stu-id="1e6dd-113">Example 1: Get all the service objectives by using a connection context</span></span>
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -Context $Context
```

<span data-ttu-id="1e6dd-114">Esse comando obtém todos os objetivos de serviço do servidor que o contexto de conexão $Context especifica.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-114">This command gets all the service objectives for the server that the connection context $Context specifies.</span></span>

### <span data-ttu-id="1e6dd-115">Exemplo 2: obter todos os objetivos do serviço usando um nome de servidor</span><span class="sxs-lookup"><span data-stu-id="1e6dd-115">Example 2: Get all the service objectives by using a server name</span></span>
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -ServerName "Server01"
```

<span data-ttu-id="1e6dd-116">Esse comando obtém todos os objetivos de serviço do servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-116">This command gets all the service objectives for the server named Server01.</span></span>

## <span data-ttu-id="1e6dd-117">OS</span><span class="sxs-lookup"><span data-stu-id="1e6dd-117">PARAMETERS</span></span>

### <span data-ttu-id="1e6dd-118">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1e6dd-118">-Context</span></span>
<span data-ttu-id="1e6dd-119">Especifica o contexto de conexão de um servidor.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-119">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e6dd-120">-Perfil</span><span class="sxs-lookup"><span data-stu-id="1e6dd-120">-Profile</span></span>
<span data-ttu-id="1e6dd-121">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1e6dd-122">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1e6dd-123">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="1e6dd-123">-ServerName</span></span>
<span data-ttu-id="1e6dd-124">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-124">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="1e6dd-125">-Missão-objeto</span><span class="sxs-lookup"><span data-stu-id="1e6dd-125">-ServiceObjective</span></span>
<span data-ttu-id="1e6dd-126">Especifica um objeto que representa o objetivo do serviço que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-126">Specifies an object that represents the service objective that this cmdlet gets.</span></span>
<span data-ttu-id="1e6dd-127">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="1e6dd-127">Valid values are:</span></span> 

- <span data-ttu-id="1e6dd-128">Básico: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c</span><span class="sxs-lookup"><span data-stu-id="1e6dd-128">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span></span>
- <span data-ttu-id="1e6dd-129">Padrão (S0): f1173c43-91bd-4AAA-973C-54e79e15235b</span><span class="sxs-lookup"><span data-stu-id="1e6dd-129">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span></span>
- <span data-ttu-id="1e6dd-130">Padrão (S1): 1b1ebd4d-D903-4baa-97f9-4ea675f5e928</span><span class="sxs-lookup"><span data-stu-id="1e6dd-130">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span></span>
- <span data-ttu-id="1e6dd-131">Padrão (S2): 455330e1-00CD-488b-b5fa-177c226f28b7</span><span class="sxs-lookup"><span data-stu-id="1e6dd-131">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span></span>
- <span data-ttu-id="1e6dd-132">\* Padrão (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40</span><span class="sxs-lookup"><span data-stu-id="1e6dd-132">\*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span></span>
- <span data-ttu-id="1e6dd-133">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="1e6dd-133">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="1e6dd-134">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="1e6dd-134">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="1e6dd-135">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span><span class="sxs-lookup"><span data-stu-id="1e6dd-135">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span></span>
- <span data-ttu-id="1e6dd-136">Premium (P3): a7c4c615-cfb1-464b-B252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="1e6dd-136">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="1e6dd-137">\* Padrão (S3) é parte da atualização de banco de dados do SQL V12 (prévia) mais recente.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-137">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="1e6dd-138">Para obter mais informações, consulte o [que há de novo no Azure SQL Database V12 Preview](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) ( `https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/` ) na biblioteca do Azure.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-138">For more information, see [What's New in the Azure SQL Database V12 Preview](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) (`https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/`) in the Azure library.</span></span>

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e6dd-139">-Imobjecname</span><span class="sxs-lookup"><span data-stu-id="1e6dd-139">-ServiceObjectiveName</span></span>
<span data-ttu-id="1e6dd-140">Especifica o nome de um objetivo de serviço a obter.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-140">Specifies the name of a service objective to get.</span></span>
<span data-ttu-id="1e6dd-141">Os valores válidos são: Basic, S0, S1, S2, S3, P1, P2 e P3.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-141">Valid values are: Basic, S0, S1, S2, S3, P1, P2, and P3.</span></span>

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

### <span data-ttu-id="1e6dd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e6dd-142">CommonParameters</span></span>
<span data-ttu-id="1e6dd-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e6dd-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e6dd-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e6dd-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1e6dd-145">INPUTS</span></span>

### <span data-ttu-id="1e6dd-146">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. FileObject</span><span class="sxs-lookup"><span data-stu-id="1e6dd-146">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective</span></span>

## <span data-ttu-id="1e6dd-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1e6dd-147">OUTPUTS</span></span>

### <span data-ttu-id="1e6dd-148">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\></span><span class="sxs-lookup"><span data-stu-id="1e6dd-148">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\></span></span>

## <span data-ttu-id="1e6dd-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1e6dd-149">NOTES</span></span>

## <span data-ttu-id="1e6dd-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e6dd-150">RELATED LINKS</span></span>

[<span data-ttu-id="1e6dd-151">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="1e6dd-151">Azure SQL Database</span></span>](https://msdn.microsoft.com/library/ee336279.aspx)

[<span data-ttu-id="1e6dd-152">Obter objetivo do nível de serviço</span><span class="sxs-lookup"><span data-stu-id="1e6dd-152">Get Service Level Objective</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505709.aspx)

[<span data-ttu-id="1e6dd-153">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="1e6dd-153">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="1e6dd-154">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="1e6dd-154">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


