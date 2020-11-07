---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 632b7710a6055f40c6cdc6d87d4b2cf8e3e17eeb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941529"
---
# <span data-ttu-id="7e3c8-101">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="7e3c8-101">Get-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="7e3c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e3c8-102">SYNOPSIS</span></span>
<span data-ttu-id="7e3c8-103">Obtém o estado TDE de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7e3c8-103">Gets the TDE state for a database.</span></span>

## <span data-ttu-id="7e3c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e3c8-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e3c8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7e3c8-105">DESCRIPTION</span></span>
<span data-ttu-id="7e3c8-106">O cmdlet **Get-AzSqlDatabaseTransparentDataEncryption** Obtém o estado de criptografia de dados transparente (TDE) para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7e3c8-106">The **Get-AzSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="7e3c8-107">Para obter mais informações, consulte criptografia de dados transparente com o banco de dados SQL do Azure https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) na biblioteca do Microsoft Developer Network).</span><span class="sxs-lookup"><span data-stu-id="7e3c8-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="7e3c8-108">Esse cmdlet obtém o estado atual de TDE, mas a criptografia e a descriptografia podem ser operações de execução demorada.</span><span class="sxs-lookup"><span data-stu-id="7e3c8-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="7e3c8-109">Para ver o andamento da verificação de criptografia, execute o cmdlet Get-AzSqlDatabaseTransparentDataEncryptionActivity.</span><span class="sxs-lookup"><span data-stu-id="7e3c8-109">To see the encryption scan progress, run the Get-AzSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>
<span data-ttu-id="7e3c8-110">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="7e3c8-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7e3c8-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e3c8-111">EXAMPLES</span></span>

### <span data-ttu-id="7e3c8-112">Exemplo 1: obter o status de TDE de um banco de dados</span><span class="sxs-lookup"><span data-stu-id="7e3c8-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="7e3c8-113">Esse comando obtém o status de TDE para o banco de dados chamado Database01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="7e3c8-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="7e3c8-114">OS</span><span class="sxs-lookup"><span data-stu-id="7e3c8-114">PARAMETERS</span></span>

### <span data-ttu-id="7e3c8-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7e3c8-115">-DatabaseName</span></span>
<span data-ttu-id="7e3c8-116">Especifica o nome do banco de dados para o qual esse cmdlet obtém o status de TDE.</span><span class="sxs-lookup"><span data-stu-id="7e3c8-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="7e3c8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e3c8-117">-DefaultProfile</span></span>
<span data-ttu-id="7e3c8-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7e3c8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e3c8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e3c8-119">-ResourceGroupName</span></span>
<span data-ttu-id="7e3c8-120">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="7e3c8-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="7e3c8-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="7e3c8-121">-ServerName</span></span>
<span data-ttu-id="7e3c8-122">Especifica o nome do servidor que hospeda o banco de dados para o qual esse cmdlet obtém o status de TDE.</span><span class="sxs-lookup"><span data-stu-id="7e3c8-122">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="7e3c8-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7e3c8-123">-Confirm</span></span>
<span data-ttu-id="7e3c8-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e3c8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e3c8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e3c8-125">-WhatIf</span></span>
<span data-ttu-id="7e3c8-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7e3c8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e3c8-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7e3c8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e3c8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e3c8-128">CommonParameters</span></span>
<span data-ttu-id="7e3c8-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e3c8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e3c8-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e3c8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e3c8-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7e3c8-131">INPUTS</span></span>

### <span data-ttu-id="7e3c8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7e3c8-132">System.String</span></span>

## <span data-ttu-id="7e3c8-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7e3c8-133">OUTPUTS</span></span>

### <span data-ttu-id="7e3c8-134">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="7e3c8-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="7e3c8-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7e3c8-135">NOTES</span></span>

## <span data-ttu-id="7e3c8-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e3c8-136">RELATED LINKS</span></span>

[<span data-ttu-id="7e3c8-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="7e3c8-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="7e3c8-138">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="7e3c8-138">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)
