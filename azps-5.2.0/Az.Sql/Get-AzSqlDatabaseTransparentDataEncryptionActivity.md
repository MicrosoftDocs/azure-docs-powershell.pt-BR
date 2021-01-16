---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: cb3cf5ee27afff0f95d1d649ec955a136cb76dba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264333"
---
# <span data-ttu-id="ef120-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="ef120-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="ef120-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef120-102">SYNOPSIS</span></span>
<span data-ttu-id="ef120-103">Obtém o progresso de uma verificação de TDE de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ef120-103">Gets the progress of a TDE scan of a database.</span></span>

## <span data-ttu-id="ef120-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef120-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef120-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ef120-105">DESCRIPTION</span></span>
<span data-ttu-id="ef120-106">O cmdlet **Get-AzSqlDatabaseTransparentDataEncryptionActivity** Obtém o progresso de uma verificação de criptografia de dados transparente (TDE) de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ef120-106">The **Get-AzSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="ef120-107">Se não houver criptografia span em execução, esse cmdlet retornará uma lista vazia.</span><span class="sxs-lookup"><span data-stu-id="ef120-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="ef120-108">Para obter mais informações, consulte criptografia de dados transparente com o banco de dados SQL do Azure https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) na biblioteca do Microsoft Developer Network).</span><span class="sxs-lookup"><span data-stu-id="ef120-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="ef120-109">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="ef120-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ef120-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef120-110">EXAMPLES</span></span>

### <span data-ttu-id="ef120-111">Exemplo 1: obter a atividade do TDE para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="ef120-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="ef120-112">Esse comando obtém a atividade TDE do banco de dados chamado database01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="ef120-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="ef120-113">OS</span><span class="sxs-lookup"><span data-stu-id="ef120-113">PARAMETERS</span></span>

### <span data-ttu-id="ef120-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ef120-114">-DatabaseName</span></span>
<span data-ttu-id="ef120-115">Especifica o nome do banco de dados para o qual esse cmdlet se obtém TDE atividade de criptografia.</span><span class="sxs-lookup"><span data-stu-id="ef120-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="ef120-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef120-116">-DefaultProfile</span></span>
<span data-ttu-id="ef120-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ef120-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef120-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef120-118">-ResourceGroupName</span></span>
<span data-ttu-id="ef120-119">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="ef120-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ef120-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ef120-120">-ServerName</span></span>
<span data-ttu-id="ef120-121">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="ef120-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="ef120-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ef120-122">-Confirm</span></span>
<span data-ttu-id="ef120-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef120-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef120-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef120-124">-WhatIf</span></span>
<span data-ttu-id="ef120-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ef120-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef120-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ef120-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef120-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef120-127">CommonParameters</span></span>
<span data-ttu-id="ef120-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef120-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef120-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef120-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef120-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ef120-130">INPUTS</span></span>

### <span data-ttu-id="ef120-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ef120-131">System.String</span></span>

## <span data-ttu-id="ef120-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ef120-132">OUTPUTS</span></span>

### <span data-ttu-id="ef120-133">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="ef120-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="ef120-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ef120-134">NOTES</span></span>

## <span data-ttu-id="ef120-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef120-135">RELATED LINKS</span></span>

[<span data-ttu-id="ef120-136">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="ef120-136">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="ef120-137">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="ef120-137">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)


