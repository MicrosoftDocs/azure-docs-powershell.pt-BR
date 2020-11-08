---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 002dbbf0a5d244f992beb8a6591907a4c38ed6ae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110840"
---
# <span data-ttu-id="f22fa-101">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="f22fa-101">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="f22fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f22fa-102">SYNOPSIS</span></span>
<span data-ttu-id="f22fa-103">Habilita a autenticação do Azure AD somente para um SQL Server específico.</span><span class="sxs-lookup"><span data-stu-id="f22fa-103">Enables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="f22fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f22fa-104">SYNTAX</span></span>

### <span data-ttu-id="f22fa-105">UseResourceGroupAndServerNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f22fa-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f22fa-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f22fa-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f22fa-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f22fa-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f22fa-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f22fa-108">DESCRIPTION</span></span>
<span data-ttu-id="f22fa-109">O cmdlet **Enable-AzSqlServerActiveDirectoryOnlyAuthentication** habilita o Azure Active Directory (Azure AD) apenas requisito de autenticação para um servidor AzureSQL na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="f22fa-109">The **Enable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="f22fa-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f22fa-110">EXAMPLES</span></span>

### <span data-ttu-id="f22fa-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f22fa-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   True
```

<span data-ttu-id="f22fa-112">Esse comando habilita o Azure Active Directory (Azure AD) apenas requisito de autenticação para um servidor AzureSQL chamado Server01 que está associado a um grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="f22fa-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="f22fa-113">OS</span><span class="sxs-lookup"><span data-stu-id="f22fa-113">PARAMETERS</span></span>

### <span data-ttu-id="f22fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f22fa-114">-DefaultProfile</span></span>
<span data-ttu-id="f22fa-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f22fa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f22fa-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f22fa-116">-InputObject</span></span>
<span data-ttu-id="f22fa-117">O objeto do SQL Server a ser usado.</span><span class="sxs-lookup"><span data-stu-id="f22fa-117">The SQL server object to use.</span></span>

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

### <span data-ttu-id="f22fa-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f22fa-118">-ResourceGroupName</span></span>
<span data-ttu-id="f22fa-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f22fa-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="f22fa-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f22fa-120">-ResourceId</span></span>
<span data-ttu-id="f22fa-121">A ID do recurso da instância a ser usada</span><span class="sxs-lookup"><span data-stu-id="f22fa-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="f22fa-122">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f22fa-122">-ServerName</span></span>
<span data-ttu-id="f22fa-123">O nome do Azure SQL Server ao qual a autenticação do Azure Active Directory faz autenticação.</span><span class="sxs-lookup"><span data-stu-id="f22fa-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="f22fa-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f22fa-124">-Confirm</span></span>
<span data-ttu-id="f22fa-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f22fa-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f22fa-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f22fa-126">-WhatIf</span></span>
<span data-ttu-id="f22fa-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f22fa-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f22fa-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f22fa-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f22fa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f22fa-129">CommonParameters</span></span>
<span data-ttu-id="f22fa-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f22fa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f22fa-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f22fa-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f22fa-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f22fa-132">INPUTS</span></span>

### <span data-ttu-id="f22fa-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f22fa-133">System.String</span></span>

## <span data-ttu-id="f22fa-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f22fa-134">OUTPUTS</span></span>

### <span data-ttu-id="f22fa-135">Microsoft. Azure. Commands. Sql. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="f22fa-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="f22fa-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f22fa-136">NOTES</span></span>

## <span data-ttu-id="f22fa-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f22fa-137">RELATED LINKS</span></span>

[<span data-ttu-id="f22fa-138">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="f22fa-138">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="f22fa-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="f22fa-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="f22fa-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f22fa-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="f22fa-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f22fa-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="f22fa-142">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="f22fa-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)