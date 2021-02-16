---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 4fcceb8c268f025ac3898ebf01f5b77a9bab54a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116343"
---
# <span data-ttu-id="e53d8-101">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e53d8-101">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="e53d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e53d8-102">SYNOPSIS</span></span>
<span data-ttu-id="e53d8-103">Remove um administrador do Azure AD para SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e53d8-103">Removes an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="e53d8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e53d8-104">SYNTAX</span></span>

```
Remove-AzSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e53d8-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e53d8-105">DESCRIPTION</span></span>
<span data-ttu-id="e53d8-106">O cmdlet **Remove-AzSqlServerActiveDirectoryAdministrator** remove um administrador do Azure Active Directory (Azure AD) para o AzureSQL Server na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="e53d8-106">The **Remove-AzSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="e53d8-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e53d8-107">EXAMPLES</span></span>

### <span data-ttu-id="e53d8-108">Exemplo 1: Remover um administrador</span><span class="sxs-lookup"><span data-stu-id="e53d8-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="e53d8-109">Esse comando remove o administrador do Azure AD para o servidor chamado Server01 associado ao grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="e53d8-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="e53d8-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e53d8-110">PARAMETERS</span></span>

### <span data-ttu-id="e53d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e53d8-111">-DefaultProfile</span></span>
<span data-ttu-id="e53d8-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e53d8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e53d8-113">-Forçar</span><span class="sxs-lookup"><span data-stu-id="e53d8-113">-Force</span></span>
<span data-ttu-id="e53d8-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e53d8-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e53d8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e53d8-115">-ResourceGroupName</span></span>
<span data-ttu-id="e53d8-116">Especifica o nome do grupo de recursos ao qual o SQL Server é atribuído.</span><span class="sxs-lookup"><span data-stu-id="e53d8-116">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="e53d8-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e53d8-117">-ServerName</span></span>
<span data-ttu-id="e53d8-118">Especifica o nome do SQL Server para o qual este cmdlet remove um administrador.</span><span class="sxs-lookup"><span data-stu-id="e53d8-118">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

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

### <span data-ttu-id="e53d8-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e53d8-119">-Confirm</span></span>
<span data-ttu-id="e53d8-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e53d8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e53d8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e53d8-121">-WhatIf</span></span>
<span data-ttu-id="e53d8-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e53d8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e53d8-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e53d8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e53d8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e53d8-124">CommonParameters</span></span>
<span data-ttu-id="e53d8-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e53d8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e53d8-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e53d8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e53d8-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="e53d8-127">INPUTS</span></span>

### <span data-ttu-id="e53d8-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e53d8-128">System.String</span></span>

## <span data-ttu-id="e53d8-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="e53d8-129">OUTPUTS</span></span>

### <span data-ttu-id="e53d8-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="e53d8-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="e53d8-131">Notas</span><span class="sxs-lookup"><span data-stu-id="e53d8-131">NOTES</span></span>

## <span data-ttu-id="e53d8-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e53d8-132">RELATED LINKS</span></span>

[<span data-ttu-id="e53d8-133">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e53d8-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="e53d8-134">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e53d8-134">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="e53d8-135">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="e53d8-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


