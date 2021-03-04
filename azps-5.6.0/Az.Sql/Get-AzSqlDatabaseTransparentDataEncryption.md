---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 1b045b97df1dbbc704f3288cf2075caa16f30bd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901416"
---
# <span data-ttu-id="fa42a-101">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="fa42a-101">Get-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="fa42a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa42a-102">SYNOPSIS</span></span>
<span data-ttu-id="fa42a-103">Obtém o estado TDE de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fa42a-103">Gets the TDE state for a database.</span></span>

## <span data-ttu-id="fa42a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fa42a-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa42a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fa42a-105">DESCRIPTION</span></span>
<span data-ttu-id="fa42a-106">O cmdlet **Get-AzSqlDatabaseTransparentDataEncryption** obtém o estado de Criptografia de Dados Transparentes (TDE) para um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="fa42a-106">The **Get-AzSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="fa42a-107">Para obter mais informações, consulte Transparent Data Encryption with Azure SQL Database https://msdn.microsoft.com/library/dn948096 ( in the Microsoft Developer Network https://msdn.microsoft.com/library/dn948096) Library.</span><span class="sxs-lookup"><span data-stu-id="fa42a-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="fa42a-108">Este cmdlet obtém o estado atual do TDE, mas a criptografia e a descriptografia podem ser operações de longa duração.</span><span class="sxs-lookup"><span data-stu-id="fa42a-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="fa42a-109">Para ver o progresso da verificação de criptografia, execute o cmdlet Get-AzSqlDatabaseTransparentDataEncryptionActivity de criptografia.</span><span class="sxs-lookup"><span data-stu-id="fa42a-109">To see the encryption scan progress, run the Get-AzSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>
<span data-ttu-id="fa42a-110">Esse cmdlet também é suportado pelo serviço SQL Server Banco de Dados de Extensão no Azure.</span><span class="sxs-lookup"><span data-stu-id="fa42a-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="fa42a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa42a-111">EXAMPLES</span></span>

### <span data-ttu-id="fa42a-112">Exemplo 1: Obter status TDE para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="fa42a-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="fa42a-113">Este comando obtém o status do TDE para o banco de dados chamado Database01 no servidor chamado server01.</span><span class="sxs-lookup"><span data-stu-id="fa42a-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="fa42a-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fa42a-114">PARAMETERS</span></span>

### <span data-ttu-id="fa42a-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fa42a-115">-DatabaseName</span></span>
<span data-ttu-id="fa42a-116">Especifica o nome do banco de dados para o qual este cmdlet obtém o status TDE.</span><span class="sxs-lookup"><span data-stu-id="fa42a-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="fa42a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa42a-117">-DefaultProfile</span></span>
<span data-ttu-id="fa42a-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="fa42a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa42a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa42a-119">-ResourceGroupName</span></span>
<span data-ttu-id="fa42a-120">Especifica o nome do grupo de recursos ao qual o banco de dados é atribuído.</span><span class="sxs-lookup"><span data-stu-id="fa42a-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="fa42a-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fa42a-121">-ServerName</span></span>
<span data-ttu-id="fa42a-122">Especifica o nome do servidor que hospeda o banco de dados para o qual este cmdlet obtém o status TDE.</span><span class="sxs-lookup"><span data-stu-id="fa42a-122">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="fa42a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa42a-123">-Confirm</span></span>
<span data-ttu-id="fa42a-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa42a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa42a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa42a-125">-WhatIf</span></span>
<span data-ttu-id="fa42a-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fa42a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa42a-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fa42a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa42a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa42a-128">CommonParameters</span></span>
<span data-ttu-id="fa42a-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa42a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa42a-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa42a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa42a-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa42a-131">INPUTS</span></span>

### <span data-ttu-id="fa42a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="fa42a-132">System.String</span></span>

## <span data-ttu-id="fa42a-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fa42a-133">OUTPUTS</span></span>

### <span data-ttu-id="fa42a-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="fa42a-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="fa42a-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="fa42a-135">NOTES</span></span>

## <span data-ttu-id="fa42a-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa42a-136">RELATED LINKS</span></span>

[<span data-ttu-id="fa42a-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="fa42a-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="fa42a-138">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="fa42a-138">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)
