---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: cb3cf5ee27afff0f95d1d649ec955a136cb76dba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111345"
---
# <span data-ttu-id="fe09d-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="fe09d-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="fe09d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe09d-102">SYNOPSIS</span></span>
<span data-ttu-id="fe09d-103">Obtém o progresso de uma verificação TDE de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fe09d-103">Gets the progress of a TDE scan of a database.</span></span>

## <span data-ttu-id="fe09d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe09d-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe09d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe09d-105">DESCRIPTION</span></span>
<span data-ttu-id="fe09d-106">O cmdlet **Get-AzSqlDatabaseTransparentDataEncryptionActivity** obtém o progresso de uma verificação de Criptografia de Dados Transparentes (TDE) de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="fe09d-106">The **Get-AzSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="fe09d-107">Se nenhum intervalo de criptografia estiver em execução, esse cmdlet retornará uma lista vazia.</span><span class="sxs-lookup"><span data-stu-id="fe09d-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="fe09d-108">Para obter mais informações, consulte Criptografia de Dados Transparentes com o Banco de Dados SQL do Azure https://msdn.microsoft.com/library/dn948096 ( na Biblioteca de Rede do Desenvolvedor da https://msdn.microsoft.com/library/dn948096) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fe09d-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="fe09d-109">Esse cmdlet também é suportado pelo serviço Banco de Dados de Extensão do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="fe09d-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="fe09d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fe09d-110">EXAMPLES</span></span>

### <span data-ttu-id="fe09d-111">Exemplo 1: Obter atividade TDE para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="fe09d-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="fe09d-112">Esse comando obtém a atividade TDE do banco de dados chamado banco de dados01 no servidor denominado servidor01.</span><span class="sxs-lookup"><span data-stu-id="fe09d-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="fe09d-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe09d-113">PARAMETERS</span></span>

### <span data-ttu-id="fe09d-114">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="fe09d-114">-DatabaseName</span></span>
<span data-ttu-id="fe09d-115">Especifica o nome do banco de dados para o qual este cmdlet obtém atividade de criptografia TDE.</span><span class="sxs-lookup"><span data-stu-id="fe09d-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="fe09d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe09d-116">-DefaultProfile</span></span>
<span data-ttu-id="fe09d-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="fe09d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe09d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe09d-118">-ResourceGroupName</span></span>
<span data-ttu-id="fe09d-119">Especifica o nome do grupo de recursos ao qual o banco de dados é atribuído.</span><span class="sxs-lookup"><span data-stu-id="fe09d-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="fe09d-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fe09d-120">-ServerName</span></span>
<span data-ttu-id="fe09d-121">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="fe09d-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="fe09d-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fe09d-122">-Confirm</span></span>
<span data-ttu-id="fe09d-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe09d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe09d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe09d-124">-WhatIf</span></span>
<span data-ttu-id="fe09d-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fe09d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe09d-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fe09d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe09d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe09d-127">CommonParameters</span></span>
<span data-ttu-id="fe09d-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe09d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe09d-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe09d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe09d-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="fe09d-130">INPUTS</span></span>

### <span data-ttu-id="fe09d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="fe09d-131">System.String</span></span>

## <span data-ttu-id="fe09d-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="fe09d-132">OUTPUTS</span></span>

### <span data-ttu-id="fe09d-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="fe09d-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="fe09d-134">Notas</span><span class="sxs-lookup"><span data-stu-id="fe09d-134">NOTES</span></span>

## <span data-ttu-id="fe09d-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe09d-135">RELATED LINKS</span></span>

[<span data-ttu-id="fe09d-136">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="fe09d-136">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="fe09d-137">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="fe09d-137">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)


