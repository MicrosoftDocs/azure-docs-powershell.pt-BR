---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 692D0B64-95EB-4D36-975F-65674B3B2F8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 3e43a61c95120b0f07f89e3f3fb64aab2dee8dff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430825"
---
# <span data-ttu-id="417ba-101">Remove-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="417ba-101">Remove-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="417ba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="417ba-102">SYNOPSIS</span></span>
<span data-ttu-id="417ba-103">Remove a auditoria de um SQL Server.</span><span class="sxs-lookup"><span data-stu-id="417ba-103">Removes the auditing of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="417ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="417ba-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerAuditing [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="417ba-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="417ba-105">DESCRIPTION</span></span>
<span data-ttu-id="417ba-106">O cmdlet **Remove-AzureRmSqlServerAuditing** remove a auditoria de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="417ba-106">The **Remove-AzureRmSqlServerAuditing** cmdlet removes the auditing of an Azure SQL server.</span></span>
<span data-ttu-id="417ba-107">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName* e *ServerName* para identificar o servidor.</span><span class="sxs-lookup"><span data-stu-id="417ba-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="417ba-108">Após executar esse cmdlet, a auditoria dos bancos de dados no Azure SQL Server não é realizada.</span><span class="sxs-lookup"><span data-stu-id="417ba-108">After you run this cmdlet, auditing of the databases on the Azure SQL server is not performed.</span></span>
<span data-ttu-id="417ba-109">Se o comando for bem-sucedido e você especificar o parâmetro *PassThru* , o cmdlet retornará um objeto que descreve a política de auditoria atual e os identificadores do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="417ba-109">If the command succeeds, and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy and the Azure SQL server identifiers.</span></span>
<span data-ttu-id="417ba-110">Os identificadores de servidor incluem **ResourceGroupName** e **nomedoservidor**.</span><span class="sxs-lookup"><span data-stu-id="417ba-110">Server identifiers include the **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="417ba-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="417ba-111">EXAMPLES</span></span>

### <span data-ttu-id="417ba-112">Exemplo 1: remover a auditoria de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="417ba-112">Example 1: Remove the auditing of an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlServerAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="417ba-113">Esse comando Remove a auditoria de todos os bancos de dados localizados em Server01 no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="417ba-113">This command removes the auditing of all the databases located on Server01 in resource group.</span></span>

## <span data-ttu-id="417ba-114">OS</span><span class="sxs-lookup"><span data-stu-id="417ba-114">PARAMETERS</span></span>

### <span data-ttu-id="417ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="417ba-115">-DefaultProfile</span></span>
<span data-ttu-id="417ba-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="417ba-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="417ba-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="417ba-117">-PassThru</span></span>
<span data-ttu-id="417ba-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="417ba-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="417ba-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="417ba-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="417ba-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="417ba-120">-ResourceGroupName</span></span>
<span data-ttu-id="417ba-121">Especifica o nome do grupo de recursos ao qual o SQL Server do Azure está atribuído.</span><span class="sxs-lookup"><span data-stu-id="417ba-121">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="417ba-122">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="417ba-122">-ServerName</span></span>
<span data-ttu-id="417ba-123">Especifica o nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="417ba-123">Specifies the name of the Azure SQL server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="417ba-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="417ba-124">-Confirm</span></span>
<span data-ttu-id="417ba-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="417ba-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="417ba-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="417ba-126">-WhatIf</span></span>
<span data-ttu-id="417ba-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="417ba-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="417ba-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="417ba-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="417ba-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="417ba-129">CommonParameters</span></span>
<span data-ttu-id="417ba-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="417ba-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="417ba-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="417ba-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="417ba-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="417ba-132">INPUTS</span></span>

### <span data-ttu-id="417ba-133">System. String</span><span class="sxs-lookup"><span data-stu-id="417ba-133">System.String</span></span>

## <span data-ttu-id="417ba-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="417ba-134">OUTPUTS</span></span>

### <span data-ttu-id="417ba-135">Microsoft. Azure. Commands. Sql. Auditing. Model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="417ba-135">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="417ba-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="417ba-136">NOTES</span></span>

## <span data-ttu-id="417ba-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="417ba-137">RELATED LINKS</span></span>

[<span data-ttu-id="417ba-138">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="417ba-138">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="417ba-139">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="417ba-139">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="417ba-140">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="417ba-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


