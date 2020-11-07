---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 333b2d2e8bab14798e7c5809590814e4a189b555
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773531"
---
# <span data-ttu-id="b9de8-101">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b9de8-101">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="b9de8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9de8-102">SYNOPSIS</span></span>
<span data-ttu-id="b9de8-103">Remove um administrador do Azure AD para SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b9de8-103">Removes an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="b9de8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9de8-104">SYNTAX</span></span>

```
Remove-AzSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9de8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9de8-105">DESCRIPTION</span></span>
<span data-ttu-id="b9de8-106">O cmdlet **Remove-AzSqlServerActiveDirectoryAdministrator** remove um administrador do Azure Active Directory (Azure AD) para AzureSQL Server na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="b9de8-106">The **Remove-AzSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="b9de8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9de8-107">EXAMPLES</span></span>

### <span data-ttu-id="b9de8-108">Exemplo 1: remover um administrador</span><span class="sxs-lookup"><span data-stu-id="b9de8-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="b9de8-109">Esse comando Remove o administrador do Azure AD do servidor chamado Server01 associado à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b9de8-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="b9de8-110">OS</span><span class="sxs-lookup"><span data-stu-id="b9de8-110">PARAMETERS</span></span>

### <span data-ttu-id="b9de8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9de8-111">-DefaultProfile</span></span>
<span data-ttu-id="b9de8-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b9de8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9de8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b9de8-113">-Force</span></span>
<span data-ttu-id="b9de8-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b9de8-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b9de8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9de8-115">-ResourceGroupName</span></span>
<span data-ttu-id="b9de8-116">Especifica o nome do grupo de recursos ao qual o SQL Server está atribuído.</span><span class="sxs-lookup"><span data-stu-id="b9de8-116">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="b9de8-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="b9de8-117">-ServerName</span></span>
<span data-ttu-id="b9de8-118">Especifica o nome do SQL Server para o qual esse cmdlet Remove um administrador.</span><span class="sxs-lookup"><span data-stu-id="b9de8-118">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

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

### <span data-ttu-id="b9de8-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b9de8-119">-Confirm</span></span>
<span data-ttu-id="b9de8-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9de8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9de8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9de8-121">-WhatIf</span></span>
<span data-ttu-id="b9de8-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b9de8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9de8-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9de8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9de8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9de8-124">CommonParameters</span></span>
<span data-ttu-id="b9de8-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9de8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9de8-126">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9de8-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9de8-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9de8-127">INPUTS</span></span>

### <span data-ttu-id="b9de8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b9de8-128">System.String</span></span>

## <span data-ttu-id="b9de8-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9de8-129">OUTPUTS</span></span>

### <span data-ttu-id="b9de8-130">Microsoft. Azure. Commands. Sql. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="b9de8-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="b9de8-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9de8-131">NOTES</span></span>

## <span data-ttu-id="b9de8-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9de8-132">RELATED LINKS</span></span>

[<span data-ttu-id="b9de8-133">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b9de8-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="b9de8-134">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b9de8-134">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="b9de8-135">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="b9de8-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


