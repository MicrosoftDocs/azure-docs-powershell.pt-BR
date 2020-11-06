---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: ca3ee787e577eabc9e889cbb471fcf3a00a4736c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602394"
---
# <span data-ttu-id="edf27-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="edf27-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="edf27-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="edf27-102">SYNOPSIS</span></span>
<span data-ttu-id="edf27-103">Modifica a propriedade TDE de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="edf27-103">Modifies TDE property for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edf27-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="edf27-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edf27-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="edf27-105">DESCRIPTION</span></span>
<span data-ttu-id="edf27-106">O cmdlet **set-AzureRmSqlDatabaseTransparentDataEncryption** modifica a propriedade de criptografia de dados transparente (TDE) de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="edf27-106">The **Set-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="edf27-107">Para obter mais informações, consulte criptografia de dados transparente com o banco de dados SQL do Azure https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) na biblioteca do Microsoft Developer Network).</span><span class="sxs-lookup"><span data-stu-id="edf27-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>

<span data-ttu-id="edf27-108">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="edf27-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="edf27-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="edf27-109">EXAMPLES</span></span>

### <span data-ttu-id="edf27-110">Exemplo 1: habilitar o TDE para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="edf27-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="edf27-111">Esse comando habilita TDE para o banco de dados chamado Database01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="edf27-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="edf27-112">OS</span><span class="sxs-lookup"><span data-stu-id="edf27-112">PARAMETERS</span></span>

### <span data-ttu-id="edf27-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="edf27-113">-DatabaseName</span></span>
<span data-ttu-id="edf27-114">Especifica o nome do banco de dados que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="edf27-114">Specifies the name of the database that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edf27-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edf27-115">-ResourceGroupName</span></span>
<span data-ttu-id="edf27-116">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="edf27-116">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edf27-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="edf27-117">-ServerName</span></span>
<span data-ttu-id="edf27-118">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="edf27-118">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edf27-119">-Estado</span><span class="sxs-lookup"><span data-stu-id="edf27-119">-State</span></span>
<span data-ttu-id="edf27-120">Especifica o valor da propriedade TDE.</span><span class="sxs-lookup"><span data-stu-id="edf27-120">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="edf27-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="edf27-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="edf27-122">Possibilita</span><span class="sxs-lookup"><span data-stu-id="edf27-122">Enabled</span></span> 
- <span data-ttu-id="edf27-123">Ativo</span><span class="sxs-lookup"><span data-stu-id="edf27-123">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edf27-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="edf27-124">-Confirm</span></span>
<span data-ttu-id="edf27-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edf27-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edf27-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edf27-126">-WhatIf</span></span>
<span data-ttu-id="edf27-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="edf27-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edf27-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="edf27-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edf27-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edf27-129">-DefaultProfile</span></span>
<span data-ttu-id="edf27-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="edf27-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edf27-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edf27-131">CommonParameters</span></span>
<span data-ttu-id="edf27-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edf27-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edf27-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edf27-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edf27-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="edf27-134">INPUTS</span></span>

## <span data-ttu-id="edf27-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="edf27-135">OUTPUTS</span></span>

### <span data-ttu-id="edf27-136">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="edf27-136">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="edf27-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="edf27-137">NOTES</span></span>

## <span data-ttu-id="edf27-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="edf27-138">RELATED LINKS</span></span>

[<span data-ttu-id="edf27-139">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="edf27-139">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="edf27-140">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="edf27-140">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="edf27-141">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="edf27-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


