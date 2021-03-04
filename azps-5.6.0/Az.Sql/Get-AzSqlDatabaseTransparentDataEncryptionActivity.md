---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: 0bdfa7ddf86beef3b9db26ff36a1953a1b574fd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901415"
---
# <span data-ttu-id="b68a0-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="b68a0-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="b68a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b68a0-102">SYNOPSIS</span></span>
<span data-ttu-id="b68a0-103">Obtém o progresso de uma verificação TDE de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b68a0-103">Gets the progress of a TDE scan of a database.</span></span>

## <span data-ttu-id="b68a0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b68a0-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b68a0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b68a0-105">DESCRIPTION</span></span>
<span data-ttu-id="b68a0-106">O cmdlet **Get-AzSqlDatabaseTransparentDataEncryptionActivity** obtém o progresso de uma verificação TDE (Criptografia de Dados Transparentes) de um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b68a0-106">The **Get-AzSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="b68a0-107">Se nenhum intervalo de criptografia estiver sendo executado, esse cmdlet retornará uma lista vazia.</span><span class="sxs-lookup"><span data-stu-id="b68a0-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="b68a0-108">Para obter mais informações, consulte Transparent Data Encryption with Azure SQL Database https://msdn.microsoft.com/library/dn948096 ( in the Microsoft Developer Network https://msdn.microsoft.com/library/dn948096) Library.</span><span class="sxs-lookup"><span data-stu-id="b68a0-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="b68a0-109">Esse cmdlet também é suportado pelo serviço SQL Server Banco de Dados de Extensão no Azure.</span><span class="sxs-lookup"><span data-stu-id="b68a0-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b68a0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b68a0-110">EXAMPLES</span></span>

### <span data-ttu-id="b68a0-111">Exemplo 1: Obter atividade TDE para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="b68a0-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="b68a0-112">Esse comando obtém a atividade TDE do banco de dados chamado database01 no servidor chamado server01.</span><span class="sxs-lookup"><span data-stu-id="b68a0-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="b68a0-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b68a0-113">PARAMETERS</span></span>

### <span data-ttu-id="b68a0-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b68a0-114">-DatabaseName</span></span>
<span data-ttu-id="b68a0-115">Especifica o nome do banco de dados para o qual este cmdlet obtém atividade de criptografia TDE.</span><span class="sxs-lookup"><span data-stu-id="b68a0-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="b68a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b68a0-116">-DefaultProfile</span></span>
<span data-ttu-id="b68a0-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b68a0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b68a0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b68a0-118">-ResourceGroupName</span></span>
<span data-ttu-id="b68a0-119">Especifica o nome do grupo de recursos ao qual o banco de dados é atribuído.</span><span class="sxs-lookup"><span data-stu-id="b68a0-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="b68a0-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b68a0-120">-ServerName</span></span>
<span data-ttu-id="b68a0-121">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="b68a0-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="b68a0-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b68a0-122">-Confirm</span></span>
<span data-ttu-id="b68a0-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b68a0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b68a0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b68a0-124">-WhatIf</span></span>
<span data-ttu-id="b68a0-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b68a0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b68a0-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b68a0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b68a0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b68a0-127">CommonParameters</span></span>
<span data-ttu-id="b68a0-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b68a0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b68a0-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b68a0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b68a0-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b68a0-130">INPUTS</span></span>

### <span data-ttu-id="b68a0-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b68a0-131">System.String</span></span>

## <span data-ttu-id="b68a0-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b68a0-132">OUTPUTS</span></span>

### <span data-ttu-id="b68a0-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="b68a0-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="b68a0-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="b68a0-134">NOTES</span></span>

## <span data-ttu-id="b68a0-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b68a0-135">RELATED LINKS</span></span>

[<span data-ttu-id="b68a0-136">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="b68a0-136">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="b68a0-137">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="b68a0-137">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)


