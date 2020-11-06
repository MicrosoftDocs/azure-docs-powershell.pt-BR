---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D3BA6534-CAAC-41E2-8442-0606B712E2B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 30161db97a108b4a5612eb9fbf0d3d749b64a11e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610995"
---
# <span data-ttu-id="35c6c-101">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="35c6c-101">Remove-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="35c6c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="35c6c-103">Remove a auditoria de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="35c6c-103">Removes the auditing of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35c6c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35c6c-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseAuditing [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35c6c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35c6c-105">DESCRIPTION</span></span>
<span data-ttu-id="35c6c-106">O cmdlet **Remove-AzureRmSqlDatabaseAuditing** remove a auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="35c6c-106">The **Remove-AzureRmSqlDatabaseAuditing** cmdlet removes the auditing of an Azure SQL database.</span></span>
<span data-ttu-id="35c6c-107">Para usar esse cmdlet, use os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="35c6c-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="35c6c-108">Depois que você executar esse cmdlet, a auditoria do banco de dados não será executada.</span><span class="sxs-lookup"><span data-stu-id="35c6c-108">After you run this cmdlet, auditing of the database is not performed.</span></span>
<span data-ttu-id="35c6c-109">Se o comando tiver êxito e você tiver usado o parâmetro *PassThru* , o cmdlet retornará um objeto que descreve a política de auditoria atual, além dos identificadores de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="35c6c-109">If the command succeeds and you have used the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy, in addition to the database identifiers.</span></span>
<span data-ttu-id="35c6c-110">Os identificadores de banco de dados incluem, entre outros, o **ResourceGroupName** , o **nomedoservidor** e o **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="35c6c-110">Database identifiers include, but are not limited to, the **ResourceGroupName** , **ServerName** and **DatabaseName**.</span></span>

<span data-ttu-id="35c6c-111">Se você remover a auditoria de um banco de dados SQL do Azure, a detecção de ameaças também será removida.</span><span class="sxs-lookup"><span data-stu-id="35c6c-111">If you remove auditing of an Azure SQL database, threat detection is also removed.</span></span>

<span data-ttu-id="35c6c-112">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="35c6c-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="35c6c-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35c6c-113">EXAMPLES</span></span>

### <span data-ttu-id="35c6c-114">Exemplo 1: remover a auditoria de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="35c6c-114">Example 1: Remove the auditing of an Azure SQL database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="35c6c-115">Esse comando Remove a auditoria do banco de dados chamada Database01.</span><span class="sxs-lookup"><span data-stu-id="35c6c-115">This command removes the auditing of database named Database01.</span></span>
<span data-ttu-id="35c6c-116">Esse banco de dados está localizado no Server01, que é atribuído ao grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="35c6c-116">That database is located on Server01, which is assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="35c6c-117">OS</span><span class="sxs-lookup"><span data-stu-id="35c6c-117">PARAMETERS</span></span>

### <span data-ttu-id="35c6c-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="35c6c-118">-DatabaseName</span></span>
<span data-ttu-id="35c6c-119">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="35c6c-119">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="35c6c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35c6c-120">-PassThru</span></span>
<span data-ttu-id="35c6c-121">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="35c6c-121">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="35c6c-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="35c6c-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="35c6c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35c6c-123">-ResourceGroupName</span></span>
<span data-ttu-id="35c6c-124">Especifica o nome do grupo de recursos que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="35c6c-124">Specifies the name of the resource group containing the database.</span></span>

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

### <span data-ttu-id="35c6c-125">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="35c6c-125">-ServerName</span></span>
<span data-ttu-id="35c6c-126">Especifica o nome do servidor que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="35c6c-126">Specifies the name of the server containing the database.</span></span>

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

### <span data-ttu-id="35c6c-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="35c6c-127">-Confirm</span></span>
<span data-ttu-id="35c6c-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35c6c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35c6c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35c6c-129">-WhatIf</span></span>
<span data-ttu-id="35c6c-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35c6c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35c6c-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35c6c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35c6c-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35c6c-132">-DefaultProfile</span></span>
<span data-ttu-id="35c6c-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35c6c-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35c6c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35c6c-134">CommonParameters</span></span>
<span data-ttu-id="35c6c-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35c6c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35c6c-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35c6c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35c6c-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35c6c-137">INPUTS</span></span>

### <span data-ttu-id="35c6c-138">Microsoft. Azure. Commands. Sql. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="35c6c-138">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="35c6c-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35c6c-139">OUTPUTS</span></span>

### <span data-ttu-id="35c6c-140">Microsoft. Azure. Commands. Sql. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="35c6c-140">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="35c6c-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35c6c-141">NOTES</span></span>

## <span data-ttu-id="35c6c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35c6c-142">RELATED LINKS</span></span>

[<span data-ttu-id="35c6c-143">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="35c6c-143">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="35c6c-144">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="35c6c-144">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="35c6c-145">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="35c6c-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


