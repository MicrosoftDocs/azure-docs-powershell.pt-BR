---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: e5460fcbc48d36dab6309891247315f0539ff7ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261451"
---
# <span data-ttu-id="0fc0d-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="0fc0d-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="0fc0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0fc0d-102">SYNOPSIS</span></span>
<span data-ttu-id="0fc0d-103">Obtém a autenticação do Azure AD somente para um SQL Server específico.</span><span class="sxs-lookup"><span data-stu-id="0fc0d-103">Gets Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="0fc0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0fc0d-104">SYNTAX</span></span>

### <span data-ttu-id="0fc0d-105">UseResourceGroupAndServerNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0fc0d-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fc0d-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fc0d-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fc0d-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fc0d-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fc0d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0fc0d-108">DESCRIPTION</span></span>
<span data-ttu-id="0fc0d-109">O cmdlet **Get-AzSqlServerActiveDirectoryOnlyAuthentication** obtém somente requisitos de autenticação do Azure Active Directory (Azure AD) para um servidor AzureSQL na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="0fc0d-109">The **Get-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="0fc0d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0fc0d-110">EXAMPLES</span></span>

### <span data-ttu-id="0fc0d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0fc0d-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   True
```

<span data-ttu-id="0fc0d-112">Este comando obtém o Azure Active Directory (Azure AD) apenas requisito de autenticação para um servidor AzureSQL chamado Server01 que está associado a um grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="0fc0d-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="0fc0d-113">OS</span><span class="sxs-lookup"><span data-stu-id="0fc0d-113">PARAMETERS</span></span>

### <span data-ttu-id="0fc0d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fc0d-114">-DefaultProfile</span></span>
<span data-ttu-id="0fc0d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0fc0d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fc0d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fc0d-116">-InputObject</span></span>
<span data-ttu-id="0fc0d-117">O objeto do SQL Server a ser usado.</span><span class="sxs-lookup"><span data-stu-id="0fc0d-117">The SQL server object to use.</span></span>

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

### <span data-ttu-id="0fc0d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fc0d-118">-ResourceGroupName</span></span>
<span data-ttu-id="0fc0d-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0fc0d-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="0fc0d-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fc0d-120">-ResourceId</span></span>
<span data-ttu-id="0fc0d-121">A ID do recurso da instância a ser usada</span><span class="sxs-lookup"><span data-stu-id="0fc0d-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="0fc0d-122">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="0fc0d-122">-ServerName</span></span>
<span data-ttu-id="0fc0d-123">O nome do Azure SQL Server ao qual a autenticação do Azure Active Directory faz autenticação.</span><span class="sxs-lookup"><span data-stu-id="0fc0d-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="0fc0d-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0fc0d-124">-Confirm</span></span>
<span data-ttu-id="0fc0d-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fc0d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fc0d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fc0d-126">-WhatIf</span></span>
<span data-ttu-id="0fc0d-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0fc0d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fc0d-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0fc0d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fc0d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fc0d-129">CommonParameters</span></span>
<span data-ttu-id="0fc0d-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fc0d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fc0d-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fc0d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fc0d-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0fc0d-132">INPUTS</span></span>

### <span data-ttu-id="0fc0d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0fc0d-133">System.String</span></span>

## <span data-ttu-id="0fc0d-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0fc0d-134">OUTPUTS</span></span>

### <span data-ttu-id="0fc0d-135">Microsoft. Azure. Commands. Sql. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="0fc0d-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="0fc0d-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0fc0d-136">NOTES</span></span>

## <span data-ttu-id="0fc0d-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0fc0d-137">RELATED LINKS</span></span>

[<span data-ttu-id="0fc0d-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="0fc0d-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="0fc0d-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="0fc0d-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="0fc0d-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="0fc0d-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="0fc0d-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="0fc0d-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="0fc0d-142">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="0fc0d-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)