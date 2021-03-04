---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/enable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: edc6ac0a9fd98b2876bc320f392e9038fb76741a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890705"
---
# <span data-ttu-id="3acf5-101">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="3acf5-101">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="3acf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3acf5-102">SYNOPSIS</span></span>
<span data-ttu-id="3acf5-103">Habilita a autenticação somente do Azure AD para um SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3acf5-103">Enables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="3acf5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3acf5-104">SYNTAX</span></span>

### <span data-ttu-id="3acf5-105">UseResourceGroupAndServerNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3acf5-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3acf5-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3acf5-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3acf5-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3acf5-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3acf5-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3acf5-108">DESCRIPTION</span></span>
<span data-ttu-id="3acf5-109">O cmdlet **Enable-AzSqlServerActiveDirectoryOnlyAuthentication** permite que o Azure Active Directory (Azure AD) só seja requisito de autenticação para um Servidor do AzureSQL na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="3acf5-109">The **Enable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="3acf5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3acf5-110">EXAMPLES</span></span>

### <span data-ttu-id="3acf5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3acf5-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   True
```

<span data-ttu-id="3acf5-112">Esse comando habilita o Azure Active Directory (Azure AD) somente requisito de autenticação para um servidor do AzureSQL chamado Server01 associado a um grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="3acf5-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="3acf5-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3acf5-113">PARAMETERS</span></span>

### <span data-ttu-id="3acf5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3acf5-114">-DefaultProfile</span></span>
<span data-ttu-id="3acf5-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3acf5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3acf5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3acf5-116">-InputObject</span></span>
<span data-ttu-id="3acf5-117">O SQL servidor a ser usado.</span><span class="sxs-lookup"><span data-stu-id="3acf5-117">The SQL server object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3acf5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3acf5-118">-ResourceGroupName</span></span>
<span data-ttu-id="3acf5-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3acf5-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3acf5-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3acf5-120">-ResourceId</span></span>
<span data-ttu-id="3acf5-121">A id de recurso de instância a ser usada</span><span class="sxs-lookup"><span data-stu-id="3acf5-121">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3acf5-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3acf5-122">-ServerName</span></span>
<span data-ttu-id="3acf5-123">O nome do Azure SQL Server a autenticação somente do Azure Active Directory está.</span><span class="sxs-lookup"><span data-stu-id="3acf5-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3acf5-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3acf5-124">-Confirm</span></span>
<span data-ttu-id="3acf5-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3acf5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3acf5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3acf5-126">-WhatIf</span></span>
<span data-ttu-id="3acf5-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3acf5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3acf5-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3acf5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3acf5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3acf5-129">CommonParameters</span></span>
<span data-ttu-id="3acf5-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3acf5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3acf5-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3acf5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3acf5-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3acf5-132">INPUTS</span></span>

### <span data-ttu-id="3acf5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3acf5-133">System.String</span></span>

## <span data-ttu-id="3acf5-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3acf5-134">OUTPUTS</span></span>

### <span data-ttu-id="3acf5-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="3acf5-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="3acf5-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="3acf5-136">NOTES</span></span>

## <span data-ttu-id="3acf5-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3acf5-137">RELATED LINKS</span></span>

[<span data-ttu-id="3acf5-138">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="3acf5-138">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="3acf5-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="3acf5-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="3acf5-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="3acf5-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="3acf5-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="3acf5-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="3acf5-142">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="3acf5-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)